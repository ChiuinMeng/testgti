脚本

想在typora中插入一个脚本，那就是插入的图片不存在本地，而是存在云端，本地插入的只是一串链接地址。这种插入图片的方式还可延伸至插入文件（源代码等）。



2019-1-10：我发现，原来这样的技术已经有了！图床！

[极简图床](http://jiantuku.com)、微博图床、[七牛云存储](https://developer.qiniu.com/kodo/kb/1369/teach-you-how-to-use-seven-niuyun-storage)、美国TripnTale无限免费旅游网络图片相册、瑞士overpic.net免费无限网络相册

应用场景：可能你经常会用markdown写文章，那么本文的图片如何添加连接呢？

- 解决方案1 使用typora可以支持本地相对路径查看，缺点是内容如果拷贝到其他平台还需要重新更改，否则不能查看。
- 解决方案2 使用图床工具，第一次就用图片的网络地址，缺点是每次需要上传图片比较麻烦。

---------------------

2019-1-11:发现七牛云和阿里云一样啊，我就在阿里云中找有没有同样的东西，结果还真找到。下面测试一下我上传的图片。
![savanna blade](https://photo-link.oss-cn-shenzhen.aliyuncs.com/%E5%8A%A0%E6%8B%BF%E5%A4%A7%E6%A8%A1%E7%89%B9Savanna%20Blade%20-%20%E7%B2%BE%E7%81%B5.jpg)

从网址就可以看出这是阿里云的深证的oss对象存储。

[一分钟了解oss](https://promotion.aliyun.com/ntms/ossedu1.html?spm=5176.8041989.314588.1.ef79e8f6rf5FmO)

其实也可使用github能存图片，不过这样很繁杂。

typora本身能使用相对路径，但是，图片存在assets中后就不会删除。当修改md文件，不再引用该图片后，该图片依旧存在。可以尝试写一个脚本来删除这些文件。

存在云端的图片很可能会丢失，到时候，图片就无法显示。所以，把图片存到assets文件夹中也有它的好处，尤其是做归档处理的时候。

极简图床可以绑定阿里云，打开网页ctrl+v即可得图片地址（下面这张截图就是存在在阿里云的）。
![](http://photo-link.oss-cn-shenzhen.aliyuncs.com/19-1-13/1820123.jpg)



