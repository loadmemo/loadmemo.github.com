---
layout: post
title: "hello world"
date: 2012-09-15 15:57
comments: true
categories: [octopress ,github pages]
---
# 基本语法
----------

### markdown 最好用的编辑器莫过于Mou了.

---

### block quotes

> this is a block quotes, 
>  
> > this is a nest block quotes  
> 
> you can write in multiple lines.  
> 1.	list in quotes line1  
> 2.	list in quotes line2  

---
### List

* 	this is a list line 1, this is a list line1, this is a list line1, this is a list line 1 this is a list line 1  
	>this is a list line 1 para2, quote1  
	>this is a list line 1 para3, quote2
*	list line 2  
*	list line 3

---

### code block

{% codeblock object-c example lang:objc %}
NSString *str = @"hello world";
NSLog(str);
{% endcodeblock %}

---
### Link
this is a [an example](http://www.google.com "google") inline link with tile "google"  
[**this link**](http://www.google.com) has no title  

---
<!-- more -->
### Strong

this is a **strong** example

---
### Inline Code
use `NSLog()` method  , e.g.: `NSLog(@"hello world");`

---
### Image
![Costa Rican Frog](/images/blog/hello world/Costa Rican Frog.jpg)  
above is a image example

---
### Video

<div class="video-container">
<embed src="http://player.youku.com/player.php/sid/XMTQxMTk5Njc2/v.swf" allowFullScreen="true" quality="high" width="480" height="400" align="middle" allowScriptAccess="always" type="application/x-shockwave-flash"></embed>
</div>
above is a  video example