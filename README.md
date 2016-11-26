# ConvertGitEmoji
转换原生的GitHub表情。拒绝繁琐的配置，只需要引入一个js文件即可转换原生的GitHub表情，让一个普通的网页也能萌起来。
# demo
http://gemoji.nocode.site/
# 使用方法
非常简单，只需要把convertgemojis.js文件引入到文档的底部，然后加入data-type="convertgemojis"属性就可以了。

```
<script type="text/javascript" src="convertgemojis.js" data-type="convertgemojis" data-emojis-src="" data-emojis-size=""></script>
```

> 建议在文档尾部引入js文件，因为这个的原理其实就是把<span>:</span>smile:等表情代码替换成img标签，所以需要等所有文档加载完毕才能保证不出错。

- data-emojis-src为可选属性，用于指定表情的仓库地址，默认为 http://gemoji.nocode.site/emojis/ 这个目录下储存的表情png文件（本地地址已经通过百度CDN加速），所以替换表情代码的时候会从这里下载表情。当然你也可以自己指定本地的一个地址，支持相对和绝对地址，注意地址的结尾必须以"/"结尾，否则出错。

- data-emojis-size为可选属性，用于设置表情的大小，单位是px，比如设置data-emojis-size="32px"，表示所有表情的大小为32px。

> 当然所有表情在文档中都被声明成"gemoji"类，你可以在css文件中定义特殊的表情大小：

```
 h1 .gemoji{
 	width: 100px;
 }
```

> 上面表示设置h1标签下面的所有表情大小为100px

# 关于反馈

其实网上有很多类似的东西，这个只不过是重复造了一个轮子罢了，代码很简单，就是把<span>:</span>smile:之类的代码替换为相应的img标签，让各位大牛见笑了，如果发现有什么问题欢迎Pull requests 或者 Issues

