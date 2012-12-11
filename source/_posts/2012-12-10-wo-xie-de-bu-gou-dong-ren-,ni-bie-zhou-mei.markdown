---
layout: post
title: "我写的不够动人，你别皱眉"
date: 2012-12-10 14:05
comments: true
categories: 
categories: [IOS, 工作, SDK]
---

>支蜡烛耐烧，然而烧不出好的作品，根本没意义。
									

顺便推荐一下我们公司的论坛 [火龙果社区](http://www.huolonger.com)

测试一下 `IOS SDK`
	
{% codeblock lang:objc %}
double delayInSeconds = 0.5;
            dispatch_time_t popTime = dispatch_time(DISPATCH_TIME_NOW, delayInSeconds * NSEC_PER_SEC);
            dispatch_after(popTime, dispatch_get_main_queue(), ^(void){
                //[JCPopoverController setUserInteraction:NO];
                TweetComposeViewController *tweetComposeViewController = [[TweetComposeViewController alloc] init];
                tweetComposeViewController.completionHandler = completionHandler;
                UINavigationController *tweetNavigationController = [[UINavigationController alloc] initWithRootViewController:tweetComposeViewController];
                [self presentModalViewController:tweetNavigationController animated:YES];
                [tweetComposeViewController release];
                [tweetNavigationController release];
            });
{% endcodeblock %}


