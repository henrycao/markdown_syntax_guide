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

    This link is to [google][linktogoogle]
    [linktogoogle]: http://www.google.com "Gooogle"
    
This link is to [google][linktogoogle]
[linktogoogle]: http://www.google.com "Gooogle"

这里的title可以用三种符号分隔。  
但是如果用单引号分隔的话，存在一个已知的bug，会不生效，所以最好不用单引号。  
另外链接地址也可以用尖括号括起来，这样看的更清楚些。  

    [linktogoogle]: <http://www.google.com> "Gooogle"
    [linktogoogle]: http://www.google.com 'Gooogle'
    [linktogoogle]: http://www.google.com (Gooogle)
    
标记id支持字母，数字，空格，和标点符号，并且不区分大小写，因此下面两个标记是一样的  

    [link A]
    [link a]
    
Markdown提供自动标记功能以方便我们偷懒，方法是link后面直接跟一个方括号，但是里面没内容，这样默认就标记了一个链接标记  

    [twitter][]
    [twitter]: <www.twitter.com> "Twitter"

[twitter][]
[twitter]: <www.twitter.com> "Twitter"

显而易见，使用inline的方式会使markdwon比较好写，而reference的方式会让markdown比较好读  
因为我们可以将标记放在文章任意的位置统一处理

###强调
markdown中强调是用`*`或者`_`包围（就是斜体字），用两个`*`或者`_`会是加粗的效果  
两种符号的效果是一样的，但是以哪种开始就必须以哪种结束

    *fire in the hole*
    _fire in the hole_
    **fire in the hole**
    __fire in the hole__
    
*fire in the hole*  
_fire in the hole_  
**fire in the hole**  
__fire in the hole__  

强调也可以插入在文字中间
    
    fire in **the** hole
fire in **the** hole

注意一点，强调的`*`和`_`与文字中间不能有空格，下面这样就不对了，换句话说就是强调和引用不支持空格（废话）

    fire in ** the** hole
fire in ** the** hole  

    fire in **the ** hole
fire in **the ** hole

注意上面这个例子中前后分别有一个空格，MD把他当普通文字处理了  
如果说要手动生成文字左右带星号的，可以用反斜杠转义  

    fire in \*\*the\*\* hole
fire in \*\*the\*\* hole

###代码  
代码是左右使用反引号括起来
    
    Stephen Curry is a `great` shooter
Stephen Curry is a `great` shooter

这样用的话看上去也能当强调用  

插入反引号可以用反斜杠转义

    \`
\`

插入引用状态的反斜杠要用下面这种方式  

    `` ` ``
`` ` ``
    
    

