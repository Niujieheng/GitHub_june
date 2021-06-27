# Google

1.使用` "关键字" `的方法进行完全匹配

2.使用`"关键字 -排除关键字"`的方法进行排除关键字搜索  逻辑非的意思

3.使用`*`进行模糊搜索

4.使用`关键字 site:网址`进行指定网站的搜索

5.使用`关键字 filetype:文件类型`进行指定文件类型的搜索 [google搜索支持的文件类型](https://support.google.com/webmasters/answer/35287?hl=en)

6.使用`inurl:关键词`查找url中包含关键词的网页

7.使用`inanchor:`指令返回的结果是导入链接锚文字中包含搜索词的页面

8.使用`intitle:关键词`指定返回的页面 title 中包含关键词

9.使用`allintitle:知乎 安全 科技`等于`intitle:知乎 intitle:安全 intitle:科技`

10.使用`link:搜索链接 `搜索所有链接到这个URL地址的网页



- 察看基本情况：
  inurl:*.asp 返回一些基本信息
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) 返回所有与该有关的url
  link:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) 返回所有与该站做了连接的站
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) filetype:txt 查找TXT文件 其他的依次内推

- 查找后台：

  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) intext:管理
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) inurl:login
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) intitle:后台

- 查看服务器使用的程序：

  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) filetype:asp
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) filetype:php
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) filetype:jsp
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) filetype:aspx

- 查看上传漏洞

  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) inurl:file
  site:[http://xx.com](https://link.zhihu.com/?target=http%3A//xx.com) inurl:load



关于GitHub上的搜索语法 [GitHub语法](https://docs.github.com/cn/github/searching-for-information-on-github/searching-on-github)    [GitHub高级搜索](https://github.com/search/advanced)

```github
org:github                 #匹配github名下的仓库
in:name test               #仓库标题搜索含有关键字test
in:descripton test         #仓库描述搜索含有关键字
in:readme test             #Readme文件搜素含有关键字
stars:>3000 test           #stars数量大于3000的搜索关键字
stars:1000..3000 test      #stars数量大于1000小于3000的搜索关键字
forks:>1000 test           #forks数量大于1000的搜索关键字
forks:1000..3000 test      #forks数量大于1000小于3000的搜索关键字
size:>=5000 test           #指定仓库大于5000k(5M)的搜索关键字
pushed:>2019-02-12 test    #发布时间大于2019-02-12的搜索关键字
created:>2019-02-12 test   #创建时间大于2019-02-12的搜索关键字
user:test                  #用户名搜素
license:apache-2.0 test    #明确仓库的 LICENSE 搜索关键字
language:java test         #在java语言的代码中搜索关键字
user:test in:name test     #组合搜索,用户名test的标题含有test的
mirror:true(false)         #是否是镜像仓库
archived:true(false)       #是否是废弃的仓库
topic:jekyll               #匹配topic中含有关键字"jekyll"的仓库
topic:5                    #匹配拥有5个topic的仓库
topic:>3                   #匹配拥有3个以上topic的仓库
is:public                  #公开的仓库
is:private                 #匹配有权限的私有仓库
repo:owner/name	           #匹配特定仓库名称。
```



