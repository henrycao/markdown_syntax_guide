区段元素
==========
###链接  
Markdown有两种链接方式，inline和reference，不管哪种方式，链接显示的内容都是用方括号包起来的`[link text]`  
创建一个inline的链接如下，方括号后面加圆括号：

    This link is to [google](http://www.google.com "Goooogle")
    This link is to [google](http://www.google.com)
    
This link is to [google](http://www.google.com "Goooogle")  
This link is to [google](http://www.google.com)  
第一种是在生成的html里带上了title的参数，第二种是不带参数的  
如果是要链接到同主机的资源，可以使用相对路径  

    This link is to [README](./README.md)
This link is to [README](./README.md)

创建一个reference的链接如下，方括号后面再加一个方括号标记id，然后在文件任意处将这个标记定义出来：  
