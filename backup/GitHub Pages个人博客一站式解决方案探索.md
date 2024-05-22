曾几何时，也利用[hexo](https://github.com/hexojs/hexo)、[hugo](https://github.com/gohugoio/hugo)等优秀框架搭建基于GitHub Pages的个人博客，结果却是无疾而终。最近，又在考虑重启个人博客的记录，因此对之前的博客折腾之路进行了反思，总结了下面两个主要问题：
- 自己本身没有坚持记录个人所思所想
- 上述框架对于我而言有个缺点是无法做到随时撰写随时保存随时上传

因此，在决定重启个人博客基建调研的时候，专门针对上述两个问题来查找方案。
- 针对问题一：首先内心给予自己心理暗示，需要利用notes或flomo等文本记录工具，将日常的阅读、播客、论文、感想等个人输出相关的内容随时记录，并在周末的时候做好整理与总结。
- 针对问题二：经过一番调研，决定采用[Gmeek](https://github.com/Meekdai/Gmeek)的模版框架，将issues作为文章发布的窗口并利用actions进行一站式发布。

再使用Gmeek的过程中，结合个人需求进行了定制[camelshang/Gmeek](https://github.com/camelshang/Gmeek)，相比原框架的主要修改为
- 原框架利用[xpinyin](https://github.com/lxneng/xpinyin)将issue标题转换为拼音，会出现将“重新”转化为“zhong-xin”等简单错误，因此改为基于[pypinyin](https://github.com/mozillazg/python-pinyin)的转化
- 原框架未能较好支持google网站收录以及分析的验证，增加了相关参数和配置
- 原框架修改footer不是很灵活，增加了参数并配置了[busuanzi](https://www.bing.com/search?q=busuanzi&qs=n&form=QBRE&=%25eManage%20Your%20Search%20History%25E&sp=-1&lq=0&pq=busuanzi&sc=10-8&sk=&cvid=A2400E00E5F04FF2BDA87CCC5ACCF61E&ghsh=0&ghacc=0&ghpl=)

和我有类似需求的朋友，可以参考[camelshang/Gmeek](https://github.com/camelshang/Gmeek)在config.py里对google-site-verification、search_script、footer_script进行配置。至此，个人需求基本被满足。