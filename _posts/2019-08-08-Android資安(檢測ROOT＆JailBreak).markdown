---
layout: post
title:  "Android資安-檢測ROOT＆JailBreak(越獄)"
date:   2019-08-08 15:40:42 +0800
categories: jekyll update
---
今年1月份因為客戶的公司資安政策要求,所以許多APP的案子都被要求要加入檢測行動裝置是否被ROOT＆JailBreak(越獄),防止APP有個資外流的風險。  

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

完成,最後請注意越獄判斷沒有辦法100%全部阻擋!!!

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
