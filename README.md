# API_ML_AI

# PRD文档初稿

&nbsp;

Target release（发布日期） | 2018-11-25
:---|:---
Epic（史诗名称） | 球员人脸识别
Document Status（文件现状） | 进行中
Document owner（文件的主人） | 何俊添
Designer（领头的设计师） | 何俊添
Developer（领头的开发者） | 何俊添
QA（领头的测试者） | 何俊添

&nbsp;

## Goals:（目标）
实现对输入图像进行人脸识别并输出球员的基本信息

&nbsp;

## Background and strategic fit（背景和战略契合处）
- 背景：很多时候人们在网上看到某张球员图片想要知道图片里的人是谁，一时间又找不到人去问，只能去发帖子求助，而且往往等到帖子沉下去也得不到答案。
- 战略契合处：针对上述情况，我的产品将会帮助人们通过一张球员的图片去识别图里的球员是谁，并且附带一些基本信息（如：身高、体重、年龄、场上位置等）

&nbsp;

## Assumptions:（假设）
用户使用此主要功能时，主要是在使用平板电脑的情境下。每次只能输入一张图片，图片必须包含完整的脸部。

&nbsp;

## Requirements（需求）
User story | Title | Importance | Note
---|---|---|---
用户在网上看到某张球员图片想要知道图片里的人是谁 | 球员人脸识别 | must have | 使用百度人脸识别API并进行人脸对比

&nbsp;

## User interaction and design（使用者交互及设计）
输入球员图片--->检测与数据库中球员图片对比的可信度（相似度）--->识别出球员--->输出球员基本信息（身高、体重、年龄、场上位置等）

&nbsp;

## Questions（问题）
如何根据输入的图片识别出图里的球员是谁？如何根据图片里的球员调出这个球员的相关信息？

&nbsp;

## Not doing（不做）
球员的表情分析