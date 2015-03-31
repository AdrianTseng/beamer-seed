# beamer-seed

支持中文的 Latex Beamer 演示文稿模板

## 使用方法

- 在Linux下直接运行 **make.sh**
- 在任意操作系统下使用 latex 编辑器打开目录并使用 xelatex 编译器编译。

## 注意事项

- 如果在linux中报错，出现无法找到字体的问题：请将**/some_path/tex/latex/ctex/fontset/ctex-xecjk-winfonts.def**修改为：

    % ctex-xecjk-winfonts.def: Windows 的 xeCJK 字体设置，默认为六种中易字体
    % vim:ft=tex
    \setCJKmainfont[BoldFont={SimHei},ItalicFont={KaiTi}]
      {SimSun}
    \setCJKsansfont{SimHei}
    \setCJKmonofont{FangSong}
    \setCJKfamilyfont{zhsong}{SimSun}
    \setCJKfamilyfont{zhhei}{SimHei}
    \setCJKfamilyfont{zhkai}{KaiTi}
    \setCJKfamilyfont{zhfs}{FangSong}
    % \setCJKfamilyfont{zhli}{LiSu}
    % \setCJKfamilyfont{zhyou}{YouYuan}
    \newcommand*{\songti}{\CJKfamily{zhsong}} % 宋体
    \newcommand*{\heiti}{\CJKfamily{zhhei}}   % 黑体
    \newcommand*{\kaishu}{\CJKfamily{zhkai}}  % 楷书  
    \newcommand*{\fangsong}{\CJKfamily{zhfs}} % 仿宋
    % \newcommand*{\lishu}{\CJKfamily{zhli}}    % 隶书
    % \newcommand*{\youyuan}{\CJKfamily{zhyou}} % 幼圆
    \endinput
