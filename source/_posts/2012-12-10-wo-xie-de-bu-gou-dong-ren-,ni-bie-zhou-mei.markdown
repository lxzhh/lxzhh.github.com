---
layout: post
title: "我写的不够动人，你别皱眉"
date: 2012-12-10 14:05
comments: true
categories: 
categories: [IOS, 工作, SDK]
---

>支蜡烛耐烧，然而烧不出好的作品，根本没意义。
									

公司的论坛 [火龙果社区](http://www.huolonger.com)

顺便测试一下 `IOS 代码`
	
{% codeblock lang:objc %}
__block NSString *stringValue;
dispatch_sync(dispatch_get_main_queue(), ^{
        // __block variables aren't automatically retained
        // so we'd better make sure we have a reference we can keep
        stringValue = [[textField stringValue] copy];
});
[stringValue autorelease];
// use stringValue in the background now
{% endcodeblock %}


