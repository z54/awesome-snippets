# autohotkey_snippets

The ultimate automation scripting language for Windows.
> [AutoHotkey](https://www.autohotkey.com/)

文档
- [热键（鼠标、操纵杆和键盘快捷键）](http://ahkcn.sourceforge.net/docs/Hotkeys.htm)

---

经验贴
- [AutoHotkey:常用技巧分享 | 上篇 - 知乎](https://zhuanlan.zhihu.com/p/103357456)
- [AutoHotkey:常用技巧分享 | 下篇 - 知乎](https://zhuanlan.zhihu.com/p/336851826)
- [autohotkey-windows快捷键设置神器_u013332124的专栏-CSDN博客_autohotkey快捷键](https://blog.csdn.net/u013332124/article/details/80680038)
- [利用Autohotkey-Windows自定键盘映射_在非全尺寸机械键盘上实现数字小键盘_Valour -的博客-CSDN博客](https://blog.csdn.net/qq_44810075/article/details/106752028)
- [使用Autohotkey为你的键盘添加Fn层 – OWNSELF](http://www.ownself.org/blog/2020/shi-yong-autohotkey-wei-ni-de-jian-pan-tian-jia-fn-ceng.html)

```
; Notes: #==win !==Alt ^==Ctrl  +==shift ;==单行注释 /**/==多行注释
/* & 组合 < 左侧 > 右侧 */

F9::reload

; #Include another.ahk
```

```
; hello world

::hello:: ; 敲下"hello"后按space或者enter出现"Hello World", 并替换"hello"
  send Hello World
 return
```

## search

```
; ---------------- search ----------------

#c:: ; win c, google搜索剪切板
run https://www.google.com/search?q=%clipboard%
sleep, 1500
return

#g:: ; win g, github搜索剪切板
run https://github.com/search?q=%clipboard%
sleep, 1500
return

#z:: ; win z, zhihu搜索剪切板
run https://www.zhihu.com/search?type=content&q=%clipboard%
sleep, 1500
return
```

## codeblock

```
; ---------------- codeblock ----------------

::/cb::
    send ```````n``````
return
```

## cmd

```
; ---------------- cmd ----------------

::/port::
    send netstat -aon | findstr 80
return

::/ip::
    send ipconfig | findstr IPv4
return

::/sys::
    send systeminfo`n
return

::/date::
	send %A_YYYY%%A_MM%%A_DD%
return

::/time::
	send %A_Hour%:%A_Min%:%A_Sec%
return

::/when::
; Send, %A_DD%-%A_MM%-%A_YYYY% %A_Hour%:%A_Min% 
; Return
```

## debian

```
; ---------------- debian ----------------

::/uu::
	send sudo apt-get update`nsudo apt-get dist-upgrade
return
```

## regex

```
; ---------------- regex ----------------

::/recn:: ; regex cn
    send [\u4e00-\u9fa5]
return

::/reen:: ; regex en
    send [0-9a-zA-Z]
return
```
