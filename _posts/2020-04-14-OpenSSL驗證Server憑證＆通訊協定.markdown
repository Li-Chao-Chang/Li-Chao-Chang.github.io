---
layout: post
title:  "OpenSSL指令驗證Server憑證＆通訊協定"
date:   2020-04-14 16:00:21 +0800
categories: jekyll update
---
<font color="#0473E2" id='1'>OpenSSL指令</font>  
-驗證   
{% highlight ruby %}
openssl s_client -connect xxx.com.tw:443 -servername Hostname
{% endhighlight %}  
![圖片1](https://github.com/Li-Chao-Chang/Blog/raw/master/_posts/images/20200414/pic1.jpg)  
![圖片2](https://github.com/Li-Chao-Chang/Blog/raw/master/_posts/images/20200414/pic2.jpg)  
-HandShake過程  
{% highlight ruby %}
openssl s_client -connect xxx.com.tw:443 -servername Hostname -state
{% endhighlight %}  
![圖片3](https://github.com/Li-Chao-Chang/Blog/raw/master/_posts/images/20200414/pic3.jpg) 

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
