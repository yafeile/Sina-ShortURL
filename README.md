====================
新浪短链接生成器    
====================

该库主要用于生成新浪短链接,完美支持`http://sina.lt`所有的短链接后缀,包括:

- sina.it
- t.cn(默认)
- dwz.cn(仅供部分知名网站使用)
- qq.cn.hn(仅供社交网站使用)
- tb.cn.hn(仅供购物网站使用)
- jd.cn.hn(仅供购物网站使用)
- tinyurl.com
- qr.net
- goo.gl(仅供海外用户使用)
- is.gd(仅供海外用户使用)
- j.mp(仅供海外用户使用)
- bit.ly(仅供海外用户使用)

其使用方法如下:

```
    from sina_shorturl import generate
    url = "The given website"
    data = generate(url)
```

我们只需要从`sina_shorturl`中导入generate函数,然后将给定的网站url作为参数传入即可。默认情况下为`t.cn`,如果想生成其他的后缀,可以指定`suffix`参数。例如:

```
    data = generate(url,suffix="sina.it")
```

我们只需要在suffix参数中填上上述支持的短链接后缀即可。  
返回的结果可能如下:

```
   {
    'short_url': 'http://t.cn/xxxx', 
    'title': '关于这个站点的简单描述'
   }
```