# API_ML_AI

# PRD文档

&nbsp;

Target release（发布日期） | 2018-12-08
:---|:---
Epic（史诗名称） | 球员人脸识别
Document Status（文件现状） | 进行中
Document owner（文件的主人） | 何俊添
Designer（领头的设计师） | 何俊添
Developer（领头的开发者） | 何俊添
QA（领头的测试者） | 何俊添

&nbsp;

## Goals（目标）
通过球员人脸识别等相应的功能为球迷在平时看球时提供帮助，提高看球体验

&nbsp;

## Background and strategic fit（背景和战略契合处）
- 背景：随着一系列体育赛事的成功举办，越来越多人关注体育赛事，享受体育赛事带来的激情（尤其是球类运动），纷纷参与到看球的行列当中，但由于球员太多而且部分球员的相貌长得较为相似，对于看球时间较短的球迷来说，分辨起来相对困难，造成看球的时候糊里糊涂的，分不清谁与谁，从而会影响到看球体验
- 战略契合处：针对上述情况，我的产品将以球员人脸识别为主，输出相关的球员信息，帮助在看球时更容易分辨出球员，提高球迷的看球体验，增添更多乐趣

&nbsp;

## Assumptions（假设）
用户使用此主要功能时，主要是在使用平板电脑的情境下。每次只能输入一张图片，图片必须包含完整的脸部。

&nbsp;

## Requirements（需求）
User story | Title | Importance | Note
---|---|---|---
用户想要了解或分辨某位球员 | 球员人脸识别及搜索、人脸库 | 十分重要 | 使用百度人脸识别API并进行人脸检测；输入图片与人脸库图片进行对比,使用百度人脸搜索API；实现人脸搜索前提要有人脸库,使用百度人脸库管理API建立人脸库
用户想要查看球员的信息数据 | 球员信息数据库 | 重要 | 需要从相关体育应用爬取数据
增加用户看球的乐趣，顺便帮助球迷增加对球员的记忆 | 看图找球员小游戏 | 一般 | /

&nbsp;

## User interaction and design（使用者交互及设计）
输入球员图片--->检测与人脸库中球员图片对比的可信度（相似度）--->识别出球员--->输出球员基本信息（身高、体重、年龄、场上位置等）
- 产品操作流程图
![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E7%90%83%E5%91%98%E8%AF%86%E5%88%AB%E6%93%8D%E4%BD%9C%E6%B5%81%E7%A8%8B.png)
- [产品原型设计](https://hejuntian.github.io/API_product_demo/start.html#g=1&p=球员识别页面)：输入

&nbsp;
![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E7%90%83%E5%91%98%E8%AF%86%E5%88%AB%E8%BE%93%E5%85%A5.jpg)
- [产品原型设计](https://hejuntian.github.io/API_product_demo/start.html#g=1&p=球员识别页面)：输出

&nbsp;
![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E7%90%83%E5%91%98%E8%AF%86%E5%88%AB%E8%BE%93%E5%87%BA.jpg)

&nbsp;

## Questions（问题）
1. 人脸库仍在尝试建立？
2. 如何根据图片里的球员调出这个球员的相关信息？

&nbsp;

## Not doing（不做）
- 球员的表情分析
- 比赛的即时赛况与数据

&nbsp;

## 清单
- [产品原型设计(不完整版)](https://hejuntian.github.io/API_product_demo/start.html#g=1&p=球员识别页面)
- [产品操作流程图](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E7%90%83%E5%91%98%E8%AF%86%E5%88%AB%E6%93%8D%E4%BD%9C%E6%B5%81%E7%A8%8B.png)
