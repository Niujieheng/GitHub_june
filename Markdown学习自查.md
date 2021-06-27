# Markdown

1.`Github Flavored Markdown, GFM `[官方文档](https://github.github.com/gfm/#what-is-github-flavored-markdown-) 

2.使⽤的 `Markdown `编辑器⽀持 `GFM`规范.

3.在 `Markdown `中实现插⼊的代码渲染后⽀持语法⾼亮.(eg.java代码)

```java
public class HelloWorld {
	public static void main(String[] args){
		System.out.println("Hello,World");
	}
}
```

4.`Markdown` 格式⽂件转换⽣成` PDF` 和` docx`   需要安装[pandoc插件](https://github.com/jgm/pandoc/releases/tag/2.14.0.2)

5.数学符号和数学公式的输入 运用LaTex/[KaTex](https://katex.org/docs/supported.html)表示     [博客](https://www.jianshu.com/p/25f0139637b7)

- 行内公式$ $

- 行间公式$$ $$

- 上标^ 下标_           eg.  `$x_i^2$`  $x_i^2$

- 括号\left(或\right) eg, `$\left(\frac{x}{y}\right)$` $\left(\frac{x}{y}\right)$

- 大括号`\{`和`\}`或者`\lbrace`和`\rbrace`  

    eg.`$\{a*b\}:a∗b$` 或`$\lbrace a*b\rbrace :a*b$`  $\lbrace a*b\rbrace :a*b$

- 尖括号`\langle` 和 `\rangle`  eg.`$\langle x \rangle$`  $\langle x \rangle$

- 上取整 `\lceil`和`\rceil`        eg.`$\lceil x \rceil$   `      $\lceil x \rceil$

- 下取整`\lfloor`和`\rfloor`     eg.`$\lfloor x \rfloor$`  $\lfloor x \rfloor$

- 求和`\sum`  会用到上标和下标  eg. `$\sum_{r=1}^n$`            $\sum_{r=1}^n$

- 积分`\int`  会用到上标和下标  eg.`$\int_{r=1}^\infty$`   $\int_{r=1}^\infty$

- 多重积分 `$\iiint$` $\iiint$

- 连乘 `\prod`    eg. `$\prod_{i=1}^{K} {a+b}$` $\prod_{i=1}^{K} {a+b}$

- 分式`\frac`(作用于后面两个组)或者`\over`(作用于前后两部分)

​          eg.`$\frac {a+c+1}{b+c+2}$`或`${a+c+1}\over {b+c+2}$`  $\frac {a+c+1}{b+c+2}$

- 根号 `\sqrt`    eg.`$\sqrt[4]{\frac xy}$`   $\sqrt[4]{\frac xy}$

6.`Markdown` 中如何输⼊⽀持单元格跨⾏合并状态的复杂表格？ 

- 简单的表格书写

​          `-:` 设置内容和标题栏居右对齐

​          `:-` 设置内容和标题栏居左对齐

​         `:-:`设置内容和标题栏居中对齐

        ```
        | 左对齐 | 右对齐 | 居中对齐 |
        | :-----| ----: | :----: |
        | 单元格 | 单元格 | 单元格 |
        | 单元格 | 单元格 | 单元格 |
        ```

| 左对齐 | 右对齐 | 居中对齐 |
| :----- | -----: | :------: |
| 单元格 | 单元格 |  单元格  |
| 单元格 | 单元格 |  单元格  |

- 复杂要用表格需要html语言 两种方法

​     HTML语言表格基础 :

​      `<table>代表表格</table>  <tr>代表表格中的一行</tr>    <td>代表表格中的一列</td>`

​      `水平单元格的合并：colspan，即使一个单元格占多行的空间`

​      `纵向单元格的合并：rowspan，即使一个单元格占多列的空间`

​     方法一：自己编写

~~~html
 ```html
 <html>
 <table>
    <tr>
       <td rowspan="2" colspan="2">真实情况</td>
       <td colspan="2">预测结果</td>
    </tr>
    <tr>
       <td>真</td>
       <td>假</td>
    </tr>
    <tr>
       <td>真</td>
       <td>TP（真正例）</td>
       <td>FN（假反例）</td>
    </tr>
    <tr>
       <td>假</td>
       <td>FP（假正例）</td>
       <td>TN（真反例）</td>
    </tr>
 </table>
 </html>
 ```
~~~



<table>
   <tr>
      <td rowspan="2" align="center">真实情况</td>
      <td colspan="2">预测结果</td>
   </tr>
   <tr>
      <td>真</td>
      <td>假</td>
   </tr>
   <tr>
      <td>真</td>
      <td>TP（真正例）</td>
      <td>FN（假反例）</td>
   </tr>
   <tr>
      <td>假</td>
      <td>FP（假正例）</td>
      <td>TN（真反例）</td>
   </tr>
</table>

​    方法二：通过网站转换 http://pressbin.com/tools/excel_to_html_table/index.html 

<table>
   <tr>
      <td colspan="6">安全1701学生名单</td>
   </tr>
   <tr>
      <td>序号</td>
      <td>姓名</td>
      <td>纸质版 毕设</td>
      <td>纸质版 开题</td>
      <td>电子版 毕设</td>
      <td>电子版 开题 </td>
   </tr>
</table>
<table>
   <tr>
      <td>中等</td>
      <td>网络空间安全学院</td>
      <td>信息安全</td>
   </tr>
   <tr>
      <td>中等</td>
      <td>网络空间安全学院</td>
      <td>信息安全</td>
   </tr>
   <tr>
      <td>良好</td>
      <td>网络空间安全学院</td>
      <td>信息安全</td>
   </tr>
   <tr>
      <td>中等</td>
      <td>网络空间安全学院</td>
      <td>信息安全</td>
   </tr>
   <tr>
      <td>中等</td>
      <td>网络空间安全学院</td>
      <td>信息安全</td>
   </tr>
   <tr>
      <td></td>
   </tr>
</table>





