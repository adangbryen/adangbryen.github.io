---
layout: post
title: "Be awesome in phpstorm"
description: "phpstorm 设置 jeffrey way 推荐方式"
category: phpstorm
tags: [phpstorm, php]
---
{% include JB/setup %}
# jeffrey way 推荐的phpstorm快捷使用方式
---

 
**参考 [视频连接](https://laracasts.com/series/how-to-be-awesome-in-phpstorm/)**
######每次换新的环境都要重新设置一下phpstorm的操作 留个记录
1. 关闭breadcrumb  command + , 打开settings search 'breadc' 关闭breadcrumb
2. 修改colors and fonts
    cd ~\Library\Performance\webide80\colors
 wget https://raw.githubusercontent.com/daylerees/colour-schemes/master/jetbrains/earthsong.icls
 下载之后 重启phpstorm  选中刚刚下载的主题
3. color ide  command+shift+a 打开 plugins 输入color 选择color ide install 然后重启
4. 快捷键 command+, * 打开keymaps 修改command+p 为open file的快捷键
                    *command + R   查看本页的结构  --> file structures
                    *command + o 查找symbol 快捷键
    这样下来 常用的>>command + i symbol >>command + o class >>command+p open file(这个跟sublime text保持一致)
5. 保持对齐  command + alt + f  reformat code
6. 自定义对齐格式  > wrappings and braces >> brace placement  >>> class declaration >>>> end of line  
                                                            >>> other >>>> next line  
                > blank lines          -- after class header  --- 1
                > others               -- 


<!--break-->
