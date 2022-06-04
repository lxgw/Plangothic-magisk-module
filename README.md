> 为使已 root 的 Android 手机扩充系统字库，方便 Magisk 用户使用，特制作此外挂模块，不过囿于本人技术水平，部分操作仍然需要用户手动进行 *（如修改 fonts.xml 文件）*，如有更便捷的方法，欢迎分享。

## 模块简介

遍黑体（世界语：Planogotiko；道本语：sitelen Pankosi）是基于思源黑体进行字符扩展及补充的项目。该项目由 (@蔽芪茢)[Fitzgerald-Porthmouth-Koenigsegg] 在大约 2020 年 6 月份所开启，其最终目标是尽可能补全整个 Unicode，并制作出一部分原本没有黑体风格字符的黑体（以中日韩統一表意文字为主）。

本模块旨在实现在系统字体文件夹 `\system\fonts` 内加入 [遍黑体](https://github.com/Fitzgerald-Porthmouth-Koenigsegg/Plangothic/) 1、2 部分字体，配合修改好的 fonts.xml *（需要自己修改）* ，达到补全手机字库的目的。

## 使用前要做的修改

使用前，需检查所搭配的字体模块的 **\system\etc\fonts.xml** 文件是否有以下语句：

```xml
    <family>
        <font weight="400" style="normal">Plangothic-P1.ttf</font>
    </family>
    <family>
        <font weight="400" style="normal">Plangothic-P2.ttf</font>
    </family>
```

如果没有，请在文件末尾`</familyset>`的前一行加上以上内容。保存后，将修改后的模块与本模块一同刷入，重启，即可实现补全手机字库的目的。

如果需要让系统默认字体也支持遍黑体，则可在手机的 **\system\etc\fonts.xml** 文件上按照上面的提示修改，前提是该手机已 ROOT。

以上方法适用于 Android 7.0 及以上版本的 Android，对于 Android 5.0～6.0 的用户，可参考知乎文章：[「下载并安装使用超大字库的具体步骤」](https://zhuanlan.zhihu.com/p/26524450)。

## 模块下载

[请进入 Releases 页面下载](https://github.com/lxgw/Plangothic-magisk-module/Releases) 

Magisk 最低支持版本 20.4。

## 注意与声明

- 请按照提示仔细修改字体模块的 fonts.xml 文件，不同机型不同系统修改的文件也不尽相同（详见 [CJK 字体 Magisk 模块模板 - 兼容性调整](https://github.com/lxgw/advanced-cjk-font-magisk-module-template#%E5%85%BC%E5%AE%B9%E6%80%A7%E8%B0%83%E6%95%B4-%E4%BB%85%E4%BE%9B%E5%8F%82%E8%80%83)），因修改文件造成的手机故障本人概不负责。
- 请勿将本模块用于商业用途。

## 字体来源

[遍黑体](https://github.com/Fitzgerald-Porthmouth-Koenigsegg/Plangothic) 由 (@蔽芪茢)[Fitzgerald-Porthmouth-Koenigsegg] 主持制作，基于 [思源黑体](https://github.com/adobe-fonts/source-han-sans) 进行字符扩展及补充。 

> 本字体基于SIL Open Font License修改、补充思源黑体和发布。详见授权文件。
> 
> 遍黑体项目下所有的字体，任何个人、企业、团队皆可免费使用。但请注意，在进行二次修改时，严禁再使用“Plangothic”、“遍黑体”等名称，二次修改过后的版本亦必须以SIL Open Font License发表。
> 
> 严禁任何个人、企业、团队对该字体文件进行售卖（包括但不限于将字体文件单独售卖，与其他字体进行捆绑售卖、需付费办理特殊权限才可使用字体等行为），如您是付费获得的此字体，请立刻对其进行举报，必要时可协助相关司法机关。

## 鸣谢
- @Fitzgerald-Porthmouth-Koenigsegg 制作「遍黑体」
- @Petit-Abba 提供 Magisk 模块模板
