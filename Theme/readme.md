#  记录自用主题、样式
- [simpleMenuWizard](https://github.com/stonecrusher/simpleMenuWizard)：右键菜单精简

- [Simple Silver修复版](https://github.com/benzBrake/FirefoxCustomize/tree/master/UserThemes/Simple%20Silver): 大圆角，独立标签页卡片，[原版](https://github.com/CristianDragos/FirefoxThemes/tree/master/Simplify%20Silver%20Peach)3年未更新，当前标签页为浅色，辨识度低，修复版为深色
  
  ---
- [Firefox-Rounded-Corners](https://github.com/Khalylexe/Firefox-Rounded-Theme)：大圆角，独立标签页卡片，新建标签页圆角

- [TYHfox](https://github.com/tyuhao/TYHfox?tab=readme-ov-file)：大圆角，独立标签页卡片，国人制作
- [Firefox Plus](https://github.com/amnweb/firefox-plus)：仿Edge，2024新项目
- [minimal-functional-fox](https://github.com/spencerwooo/minimal-functional-fox)：大圆角，彩色、独立标签页卡片
- [MaterialFox](https://github.com/muckSponge/MaterialFox): Material 风格,标签和地址栏圆角
- [Slick-Fox](https://github.com/Etesam913/slick-fox):标签小圆角、自动隐藏地址栏，3年未更新，作者也在Reddit的FirefoxCSS社区发布

出处：https://blog.csdn.net/pjqrmhtakgn/article/details/52798822
/* 修改书签菜单栏 */
#organizeBookmarksSeparator {display: none !important;}
menuitem#subscribeToPageMenuitem {display: none !important;}
menu#subscribeToPageMenupopup {display: none !important;}
menuitem#menu_bookmarkAllTabs {display: none !important;}
#bookmarksToolbarSeparator {display: none !important;}
menu#bookmarksToolbarFolderMenu {display: none !important;}
menuitem#menu_unsortedBookmarks {display: none !important;}
menuitem#sync-setup {display: none !important;}
menuitem#sync-syncnowitem {display: none !important;}
menuitem#menu_bookmarkThisPage {display: none !important;}
 
/* 隐藏列出所有标签页按钮*/
.tabs-alltabs-button {display:none !important;} 
 
/*隐藏页面右键菜单*/
#context-forward, /*前进*/
#context-back, /*后退*/
#context-reload, /*刷新*/
#context-stop, /*停止*/
#context-selectall,/*全选*/
#context-savepage,/*网页另存为*/
#context-setDesktopBackground,/*设为桌面背景*/
#context-sep-stop, /*停止下面的分割线*/
#context-bookmarkpage, /*此页面加入书签*/
#context-sendlink, /*发送链接到*/
#context-sendpage, /*发送页面链接到*/
#context-sep-copyimage, /*复制图片下面的分割线*/
#context-saveimage, /*图片另存为*/
#context-sendimage, /*发送图片到*/
#context-setDesktopBackground, /*设置为桌面背景*/
#context-savelink, /*链接另存为*/
/*#context-openlink, 在新窗口打开链接*/
/*#context-sep-open, 打开新窗口下面的分割线*/
#context-bookmarklink, /*此链接加入书签*/
#context-sep-selectall, /*全选下面的分割线*/
/*#context-searchselect, 使用默认搜索引擎搜索关键字*/
#spell-check-enabled, /*拼写检查*/
#spell-separator, /*拼写检查分割线*/
#inspect-separator, Inspect Element分割线*/
#context-inspect /*Inspect Element*/
{display: none !important;}
 
/*修改地址栏*/
#urlbar-container { min-width: 350px !important; max-width: 350px !important;}
#feed-button {display:none !important; }
#identity-box{display:none !important;}
#urlbar-icons{display:none !important;}
#urlbar {height:25px !important;}
#urlbar {font-size: 12px !important; }
#urlbar[level] .autocomplete-textbox-container {background-color: #D0F2C4 !important;}
 
/*修改awesome bar*/
.ac-comment {font-size: 12px !important; }
.ac-url-text {font-size: 12px !important; }
 
/*开始精简界面，修改tabstoolbar, navigation bar, titlebar*/
/* Tabstrip */
#TabsToolbar {
min-height: 0 !important;
padding: 0 !important;
-moz-box-shadow: none !important;
}
 
#titlebar {position: fixed !important;} 
 
#navigator-toolbox[tabsontop="true"] > #nav-bar {border: 0px !important;}
 
/* 去除多余的按钮，这个按钮会挡住导航栏标签 */
#titlebar-buttonbox {display:none !important;}
 
/* 修改火狐按钮 */
#appmenu-button {
list-style-image:url("chrome://branding/content/icon16.png");
min-width: 50px ! important;
max-width: 50px ! important;
height: 23px !important;
margin-top: 6px !important;
padding-left: 3px !important;
padding-right: 3px !important;
padding-top: 3px !important;
/* background-color: #b4b3b3 !important; */
/* color: #b4b3b3 !important; */
/* text-shadow: 0 0 2px #333 !important; */
}
#appmenu-button .button-text {display: none !important;}
#appmenu-button dropmarker {display: none !important;}
 
/*调整menubar, nav-bar, tabstoolbar间距*/
#navigator-toolbox[tabsontop="false"] #TabsToolbar {
margin-top: 1px !important;
}
 
#toolbar-menubar,
#navigator-toolbox[tabsontop="false"] #nav-bar,
#navigator-toolbox[tabsontop="true"] #TabsToolbar {
padding-left: 50px !important; /* 用户可能需要调整这里的这个参数。75px适用于原版。85适用于Lawlietfox版。90适用于Lawlietfox版的界面小按钮。50适用于Lawlietfox版的界面小按钮+Appmenu文字修改为图标 */
}
 
#main-window[sizemode="fullscreen"] #toolbar-menubar,
#main-window[sizemode="fullscreen"] #navigator-toolbox[tabsontop="false"] #nav-bar,
#main-window[sizemode="fullscreen"] #navigator-toolbox[tabsontop="true"] #TabsToolbar {
 /* padding-top: 3px !important; */
padding-right: 0px !important;
margin-top: 6px !important;
}
 
#main-window:not([sizemode="fullscreen"]) #toolbar-menubar,
#main-window:not([sizemode="fullscreen"]) #navigator-toolbox[tabsontop="false"] #nav-bar,
#main-window:not([sizemode="fullscreen"]) #navigator-toolbox[tabsontop="true"] #TabsToolbar {
/* 如果需要拖拉标题栏移动窗口，将3px改成15px */ 
/* padding-top: 10px !important; */
margin-top: 6px !important;
padding-right: 105px !important;
}
 
/* 结束精简界 */
 
/*修改书签栏文字颜色和大小*/
#personal-bookmarks toolbarbutton.bookmark-item .toolbarbutton-text {
color: #ece1e1 !important;
text-shadow: 0 0 1px black !important;
font-size: 15px !important;
}
 
/*隐藏书签栏中书签图标*/
#personal-bookmarks toolbarbutton.bookmark-item .toolbarbutton-icon {
display: none !important;
}
 
/*修改书签栏中书签间距*/
#personal-bookmarks toolbarbutton.bookmark-item {
margin-left: 1px !important;
}
 
/*隐藏bookmarks menu button里面不需要的菜单项*/
menuitem#BMB_viewBookmarksToolbar {display: none !important;}
menuitem#BMB_viewBookmarksToolbar menuseparator {display: none !important;}
menuitem#BMB_bookmarkThisPage {display: none !important;}
menuitem#BMB_subscribeToPageMenuitem {display: none !important;}
menu#BMB_subscribeToPageMenupopup {display: none !important;}
menu#BMB_subscribeToPageMenupopup menuseparator {display: none !important;}
menuitem#BMB_unsortedBookmarks {display: none !important;}
