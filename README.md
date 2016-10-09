#Syntax guide
Here’s an overview of Markdown syntax that you can use anywhere on GitHub.com or in your own text files.

MENTION USERNAME: @ouyangzhigang `@ouyangzhigang`     

##段落和换行
一个 **Markdown** 段落是由一个或多个连续的文本行组成，它的前后要有一个以上的空行（空行的定义是显示上看起来像是空的，便会被视为空行。比方说，若某一行只包含空格和制表符，则该行也会被视为空行）。普通段落不该用空格或制表符来缩进。

`「由一个或多个连续的文本行组成」`这句话其实暗示了 **Markdown** 允许段落内的强迫换行（插入换行符），这个特性和其他大部分的 *text-to-HTML* 格式不一样（包括 _Movable Type_ 的_「Convert Line Breaks」_选项），其它的格式会把每个换行符都转成` <br />` 标签。

如果你确实想要依赖 **Markdown** 来插入 `<br />` 标签的话，在插入处先按入两个以上的空格然后回车。

的确，需要多费点事（多加空格）来产生 `<br />` ，但是简单地`「每个换行都转换为 <br />」`的方法在 **Markdown** 中并不适合， **Markdown** 中 *email* 式的 `区块引用` 和多段落的 `列表` 在使用换行来排版的时候，不但更好用，还更方便阅读。



##header
* `#` (开放式) <br> 
* `#...#` （闭合式） <br> 
* `#` \ `##` \ `###` \ `####` \ `#####` \ `######`（h1-h6） <br>

**Markdown** 支持两种标题的语法，类 _Setext_ 和类 _atx_ 形式。

类 _Setext_ 形式是用底线的形式，利用 `=` （最高阶标题）和 `-` （第二阶标题），例如：

任何数量的 `=` 和 `-` 都可以有效果。

类 _Atx_ 形式则是在行首插入 1 到 6 个 `#` ，对应到标题 1 到 6 阶，例如：

你可以选择性地「闭合」类 `atx` 样式的标题，这纯粹只是美观用的，若是觉得这样看起来比较舒适，你就可以在行尾加上 `#`，而行尾的 `#` 数量也不用和开头一样

##strong
* 斜体强调
`*...*` || `_..._`<br>
* 粗体强调
`**...**` || `__...__`

##block
`>`  一级<br>
>
* >一级

`>>` 两级<br>
>>
* >>两级

`>>>` 三级<br>
>>>
* >>>三级

引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等：
> ## 这是一个标题。
> 
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
> 
> 给出一些例子代码：
> 
>```
>return shell_exec("echo $input | $markdown_script");
>```

任何像样的文本编辑器都能轻松地建立 email 型的引用。例如在 BBEdit 中，你可以选取文字后然后从选单中选择增加引用阶层。

##list
**Markdown** 支持有序列表和无序列表。

无序列表使用`星号`、`加号`或是`减号`作为列表标记：

`*`
*   Red
*   Green
*   Blue

`+`
等同于：

+   Red
+   Green
+   Blue


`-`
也等同于：

-   Red
-   Green
-   Blue

有序列表则使用数字接着一个英文句点：

1.  Bird
2.  McHale
3.  Parish

##code-block
和程序相关的写作或是标签语言原始码通常会有已经排版好的代码区块，通常这些区块我们并不希望它以一般段落文件的方式去排版，而是照原来的样子显示，Markdown 会用 `<pre>` 和 `<code>` 标签来把代码区块包起来。

`<pre><code><div class="footer">
    &copy; 2004 Foo Corporation
</div>`

要在 Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以，例如，下面的输入：
* 4个空格
    这是一个4个空格代码区域块
    
* 1个制表符

在代码区块里面， & 、 < 和 > 会自动转成 HTML 实体，这样的方式让你非常容易使用 Markdown 插入范例用的 HTML 原始码，只需要复制贴上，再加上缩进就可以了，剩下的 Markdown 都会帮你处理，例如：

    <div class="footer">
        © 2004 Foo Corporation
    </div>
会被转换为：

<pre><code><div class="footer">
    &copy; 2004 Foo Corporation
</div>
</code></pre>
    
##partition line
分隔线:你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：

```
* * *

***

*****

- - -

你可以在一行中用三个以上的`星号`、`减号`、`底线`来建立一个分隔线，行内不能有其他东西。你也可以在`*`或是`-`中间插入空格。下面每种写法都可以建立分隔线：

* *
这是分隔线1

***
这是分隔线2

*****
这是分割线3

- - -
这是分割线4

---------------------------------------
这是分割线5

```


##Strikethrough
=================================
Any word wrapped with two tildes (like ~~this~~) will appear crossed out.

`~~this~~`

~~this~~

##Tables

You can create tables by assembling a list of words and dividing them with hyphens `-` (for the first row), and then separating each column with a pipe `|`
```
        First Header | Second Header
        ------------ | -------------
        Content from cell 1 | Content from cell 2
        Content in the first column | Content in the second column
```        
    
First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

##IMAGE
```
If you want to embed images, this is how you do it:

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

```

If you want to embed images, this is how you do it:

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)



##SHA references

Any reference to a commit’s SHA-1 hash will be automatically converted into a link to that commit on GitHub.

```    
    16c999e8c71134401a78d4d46435517b2271d6ac
    mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
    mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
```    

16c999e8c71134401a78d4d46435517b2271d6ac

mojombo@16c999e8c71134401a78d4d46435517b2271d6ac

mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac


##Automatic linking for URLs
    
    Any URL (like http://www.github.com/) will be automatically converted into a clickable link.

Any URL (like http://www.github.com/) will be automatically converted into a clickable link.


##Extras

```
GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!

But I have to admit, tasks lists are my favorite:

- [x] This is a complete item
- [ ] This is an incomplete item

When you include a task list in the first comment of an Issue, you will see a helpful progress bar in your list of issues. It works in Pull Requests, too!

And, of course emoji! :sparkles: :camel: :boom:
```


GitHub supports many extras in Markdown that help you reference and link to people. If you ever want to direct a comment at someone, you can prefix their name with an @ symbol: Hey @kneath — love your sweater!

But I have to admit, tasks lists are my favorite:

- [x] This is a complete item
- [ ] This is an incomplete item

When you include a task list in the first comment of an Issue, you will see a helpful progress bar in your list of issues. It works in Pull Requests, too!

And, of course emoji! :sparkles: :camel: :boom:






