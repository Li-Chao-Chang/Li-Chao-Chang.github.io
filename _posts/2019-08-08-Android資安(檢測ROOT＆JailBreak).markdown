---
layout: post
title:  "Android資安-檢測ROOT＆JailBreak(越獄)"
date:   2019-08-08 15:40:42 +0800
categories: jekyll update
---
**C# Xamarin Android寫法**  
{% highlight ruby %}
public static bool CheckRoot()  
{  
    List<string> pathList = new List<string>  
    {  
      "/sbin",  
      "/system/bin",  
      "/system/xbin",  
      "/data/local/xbin",  
      "/data/local/bin",  
      "/system/sd/xbin",  
      "/system/bin/failsafe",  
      "/data/local"
    };
    try 
    {
        foreach (var path in pathList)
        {
            var fullPath = Path.Combine(path, "su");
            if (File.Exists(fullPath))
            {
                return true;
            }
        }
    }
    catch(Exception ex)
    {
        return false;
    }
    return false;          
}
{% endhighlight %}  

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
