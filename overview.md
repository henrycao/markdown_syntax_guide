概述
===================  
###兼容HTML
eg: 插入html表格
<table>
  <tr>
    <td>line1</td>
    <td>row1</td>
  </tr>
  <tr>
    <td>line2</td>
    <td>row2</td>
  </tr>
</table>

在 HTML 区块标签间的 Markdown 格式语法将不会被处理。比如，你在 HTML 区块内使用 Markdown 样式的*强调*会没有效果


###特殊字符转换 
& 和 < 

这是一个版权符号 
&copy; all rights reserved

但是下面这个&就会自动转化为`AT&amp;T`

AT&T

4 < 5

markdown 会自动转化为`4 &lt; 5`
