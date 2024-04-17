# Firefox-customized 火狐改造之路
## Preface
>   2024年4月突然想对浏览器右键标签进行删减，网上一顿搜索和请教，可以禁止默认右键菜单然后自己写一个代替。
>
>   但这并不符合我的本意，且并不是我一个不懂任何编程、尚未接触过前端的新手能轻易解决的，虽然网上有现成的代码。
>
>   然后小众软件论坛的网友推荐我使用火狐浏览器。

FireFox的界面全是HTML、css和JavaScript，加之其开源

可以对浏览器进行任意的修改，

正好之前看了点HTML，算是见过一次面了

HTML是一个人的肉体，css是ta的衣服，js是决定行为的想法
## 起步：用户自定义样式
>    样式这个东西，其实我一开始接触扩展和脚本的时候就遇到过，但没有使用。
>
 >   扩展能达到相同的效果，且用起来更方便，完全是傻瓜操作，就是点击一个又一个按钮
>
 >   现在看来，那时候样式已经没落了
>
 >   就像曾经的火狐浏览器，巅峰时也曾坐拥八九成的市场

现阶段主要是2个文件，`userChrome.css`和`userContent.css`

- userChrome.css是专门用来定制 Firefox〖自身的界面〗,比如浏览器的地址栏、搜索栏、快捷菜单、滚动条……
  
 -  userContent.css是专门用来定制 Firefox 浏览的网站的界面，包括内置的新标签页、扩展页面、设置页面或者网络上的网页
   
> Firefox 自 69 版本以后，为了更快的启动速度，默认不会去寻找定义样式的 userChrome.css 和 userContent.css,需要手动开启这一功能。
1. 在 Firefox 的地址栏访问 `about:config`，打开Preferences(配置)界面，忽略警告，在接下来的界面搜索
   
         toolkit.legacyUserProfileCustomizations.stylesheets

   并将这一项目设置为 `true`

   
   ![323168785-c7592ae8-73e2-48de-8418-6bd0198c809a](https://github.com/san-ren/Firefox-customized/assets/86779955/2fa04aef-ba8f-4031-bd28-7eca3bd33e2a)

   
> 此处可进行许多浏览器设置界面没有的设置
>
 >   详见：我的 Firefox 配置选项（Preferences） - 知乎 https://zhuanlan.zhihu.com/p/108157877?highligh=CPU

2.访问 `about:support`，打开配置文件夹，新建`chrome`文件夹，以后所有的css和js都放在这里面

  userChrome.css和userContent.css也是在这里，两个文件默认没有，需自行创建

  
![323173940-21a66279-b38c-4ffe-9375-a573612d0f2b](https://github.com/san-ren/Firefox-customized/assets/86779955/e0a59312-feaf-4fa6-92eb-64fec02b2906)

> 这里就不得不说一说，火狐支持保存多个配置文件，就像windows的账户、手机分身、应用多开
>
> 详见火狐官方文档：
>
> 管理用户配置文件 | Firefox 帮助 https://support.mozilla.org/zh-CN/kb/%E7%AE%A1%E7%90%86%E7%94%A8%E6%88%B7%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6

走到这一步，就可以去网上下载别人分享的样式，放到chrome文件夹，重启浏览器就生效了


> 可以通过`about:support`页面右侧的“清除启动缓存”按钮重启，方便快捷
> 
> ![323180446-1b09d97e-3c5a-4502-a411-b2a4be32be86](https://github.com/san-ren/Firefox-customized/assets/86779955/dcd6f77c-2b09-4086-9549-3d29394e6179)

列几个样式获取途径：

- [FirefoxCSS Store](https://firefoxcss-store.github.io/): 已3年未增录，但其中主题有二三十个。每个主题有不同的作者，他们会更新
- [FirefoxCSS on Reddit](https://www.reddit.com/r/FirefoxCSS/?rdt=37190&onetap_auto=true&one_tap=true)：Reddit上的一个社区，汇聚了大量的FirefoxCSS爱好者
- [firefox-csshacks](https://github.com/MrOtherGuy/firefox-csshacks)：[MrOtherGuy](https://github.com/MrOtherGuy)收集的一些userstyle，部分css已2~4年未更新，估计也是弃用了，毕竟火狐不断添加新功能，自带的功能就没必要额外操作了
- GitHub Topics：[firefoxcss ](https://github.com/topics/firefoxcss)或[userchrome](https://github.com/topics/userchrome)之类的
- 另有针对特定网站的样式，可搭配样式扩展[Stylus](https://github.com/openstyles/stylus/)使用，网站[UserStyles.world](https://userstyles.world/explore) 或[UserStyles.org Archive](https://uso.kkx.one/)，更多内容可见[奶大的文章](https://www.runningcheese.com/userstyles)
## 进阶：自定义用户脚本
 JavaScript 可以添加一些浏览器没有的功能，



























参考：

Firefox 浏览器个性化定制指南 · 云原生实验室 https://icloudnative.io/posts/customize-firefox/

美化网页，2023 年度最喜欢 Stylish 样式 - 奔跑中的奶酪 https://www.runningcheese.com/userstyles

我的 Firefox 配置选项（Preferences） - 知乎 https://zhuanlan.zhihu.com/p/108157877?highligh=CPU
