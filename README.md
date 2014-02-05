#IOL.cn (finished PDFs & codes)

Chinese translation for problems of the International Linguistics Olympiad (IOL)

##Overall

This page is for demonstration of the products of our translation project only. For current work, please refer to [our homepage](https://github.com/notcome/IOL.cn). 

##PDFs

We present each year's problem set as a separate folder. Take ``IOL10``, which contains the following PDF files:

``IOL10cn_IP.pdf`` (Individual contest problems.)

``IOL10cn_IS.pdf`` (Individual contest solutions.)

``IOL10cn_TP.pdf`` (Team contest problem.)

``IOL10cn_TS.pdf`` (Team contest solution.)

``IOL10cn_QR.pdf`` (Questionnaire [optional, given if included in the original file.])

##Source codes

For those who are interested in the translating/editing process, source codes are given in the corresponding folders. Still, take ``IOL10``:


``dxIOL10CN.tex`` (Chinese translation), consisting of a series of ``\def``'s:

```LaTeX
\def \thistext{中文文本}
\def \nthIOL #1{#1国际语言学奥林匹克竞赛}
\def \thisth{第十届}
\def \thisland{斯洛文尼亚}
\def \thistown{卢布尔雅那}
\def \Julyname{7月}
\def \Auguname{8月}
\def \olydates #1#2#3#4#5{#5年#2#1日 — #4#3日}
\def \leafword #1{答题纸 \##1}
\def \probword #1{题 \##1}
\def \probsing #1{#1 题目}
\def \probplur #1{#1 题目}
\def \respsing #1{#1 答案}
\def \solusing #1{#1 解答}
\def \soluplur #1{#1 解答}
```

``IOL10.tex`` ("Universal" problem matter. In actual practice some slight modifications are made to this file for greater compatibility with the Chinese translation as well as proper display of the International Phonetic Alphabet (IPA) characters.) 

``IOL10.nospace.tex`` (Chinese-specific (as the Chinese script normally does NOT contain spaces.) version of ``IOL10.tex``, which is by no means a misnomer.)

``IOL10en.tex`` (Main file):

```LaTeX
\documentclass[11pt]{article}
\usepackage{a4wide}
\usepackage{fontspec}
\usepackage{xeCJK}
% Chinese Font Selection
% 宋体 and 楷体 are free fonts. Check out our GitHub repository to see the exact versions used.
\setCJKmainfont[ItalicFont = Kaiti SC, SlantedFont = STFangsong, BoldFont = Songti SC Bold]{Songti SC}
% Chinese Font Selection
\setmainfont[BoldFont = CMUSerif-Bold]{CMUSerif-Roman}
% "‘" & "’" might be recognized as CJK characters.
% Numbers are changed to make the date nature.
\normalspacedchars{‘’“”1234567890-—/}
\input{dxIOL10CN}
% Run RemoveSpace to get IOL10.nospace.tex
\input{IOL10.nospace}

```

##Technical details

IOL problems are originally written in ``LaTeX``. For better font management and support for UTF-8 code, ``IOL.cn`` uses ``XeLaTeX``.

For typographic considerations, Chinese fonts are chosen from those provided in ``OS X Mavericks``. For copyright consideration, please do not compile/revise the source codes if you are not using ``OS X Mavericks``. We are negotiating with the font maker concerning copyright issues. 

IOL's original font for Latin letters and numerals is ``Computer Modern``. For better display of the IPA characters, we have decided to change it into ``Computer Modern Unicode``.


##Credits

Currently, document translation is mainly conducted by [Qitong Cao](https://github.com/caoqitong), whereas technical difficulties are usually resolved by [Minsheng Liu](https://github.com/notcome). 

We would like to acknowledge our gratitude toward [Ivan A Derzhanski](http://www.math.bas.bg/~iad/), who has kindly provided the English code files for our project.

IOL.cn is a non-profit project aimed at promoting the International Linguistics Olympiad and general linguistics education in China. 
