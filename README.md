# Rime 输入法配置指南

## 用法

1. 安装[Rime输入法](https://rime.im/),并注销或重启
2. 下载仓库所有配置文件到本地
3. 将下载的除字体外的所有文件覆盖到用户设定文件夹
4. 安装字体 ( font 目录)
5. 也可以在“用户文件夹”中查看
6. 右键点击rime输入法图标，点击重新部署，部署完毕即可用

用户设定文件夹在不同的系统下也有不同,如下

- Windows
  - Weasel: %APPDATA%\Rime
- Mac OS X
  - Squirrel: ~/Library/Rime
- Linux
  - iBus: ~/.config/ibus/rime
  - Fcitx: ~/.config/fcitx/rime


## 配置文件说明

- `default.custom.yaml` 设置输入法、如何切换输入法、翻页等
- `double_pinyin_flypy.custom.yaml` 双拼方案，
- `squirrel.custom.yaml` 鼠须管( Mac 版本 )设置哪些软件默认英文输入，输入法皮肤等
- `weasel.custom.yaml` 小狼毫( Win 版本 )设置哪些软件默认英文输入，输入法皮肤等
- `custom_phrase.txt` 设置快捷输入，修改完成后要重新部署才能生效

配置文件中大部分都有注释。

------

## FAQ

### 快捷键

使用 Ctrl + ` (Tab上面那个)切换输入方案。

### 如何添加词库

将词库文件拷贝到文件夹，修改 `luna_pinyin.extended.dict.yaml`文件

将词库名字加在 `import_tables` 下(注意格式)(我的另一个仓库[rime-dict](https://github.com/Iorest/rime-dict)中收集了很多词库)

重新部署即可

### 添加短语和缩写

将短语和缩写添加至`custom_phrase.txt`文件中

**输入的字母和汉字之间是 `tab`，而不是空格**

使用不会自动替换`tab`为空格的编辑器修改此文件

### Linux 环境下配置问题

Linux 环境下, rime输入法默认配置可能不在` ~/.config/ibus/rime`下,此时如果需要用户设定,需要将所有的配置文件加入用户设定文件夹(如果用 ibus,那么就是` ~/.config/ibus/rime`),否则配置可能出错.

另外,Linux 环境下输入法可能出现不生效的问题,这时可以在命令行中运行`ibus engine rime`,或可解决(使用ibus 框架时)

## 参考/致谢

1. [Mac 下调校 Rime](https://mritd.me/2019/03/23/oh-my-rime/)
2. [鼠须管 0.11 Mac 升级重装配置 2019](https://github.com/cnfeat/Rime)
3. [鼠须管配置 2019](https://placeless.net/blog/rime-squirrel-customization-2019#article)

