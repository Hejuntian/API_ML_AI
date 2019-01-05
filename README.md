# API_ML_AI

# PRD文档

&nbsp;

Target release（发布日期） | 2019-01-05
:---|:---
Epic（史诗名称） | nba球员人脸识别搜索+语音解说
Document Status（文件现状） | 进行中
Document owner（文件的主人） | 何俊添
Designer（领头的设计师） | 何俊添
Developer（领头的开发者） | 何俊添
QA（领头的测试者） | 何俊添

&nbsp;

## Goals（目标）
- 通过球员人脸识别等相应的功能为球迷在平时看球时提供帮助，提高看球体验
- 通过语音解说功能让用户在如开车等情况下，既能实时了解到比赛赛况，又不用分心去看手机

&nbsp;

## Background and strategic fit（背景和战略契合处）
- 背景：随着一系列体育赛事的成功举办，越来越多人关注体育赛事，享受体育赛事带来的激情（尤其是球类运动），纷纷参与到看球的行列当中，但由于球员太多而且部分球员的相貌长得较为相似，对于看球时间较短的球迷来说，分辨起来相对困难，造成看球的时候糊里糊涂的，分不清谁与谁，从而会影响到看球体验
- 战略契合处：针对上述情况，我的产品将以球员人脸识别为主，输出相关的球员信息，帮助在看球时更容易分辨出球员，提高球迷的看球体验，增添更多乐趣；再加上语音解说功能，增加用户使用体验

&nbsp;

## Assumptions（假设）
- 用户使用此主要功能时，主要是在使用手机的情境下。
- 每次只能输入一张图片，图片必须包含完整的脸部。

&nbsp;

## Requirements（需求）
User story | Title | Importance | Note
---|---|---|---
用户想要了解或分辨某位球员 | 球员人脸识别及搜索、人脸库 | 十分重要 | 使用百度人脸识别API并进行人脸检测；输入图片与人脸库图片进行对比,使用百度人脸搜索API；实现人脸搜索前提要有人脸库,使用百度人脸库管理API建立人脸库
用户在看文字直播的同时也能听到语音解说 | 语音解说 | 重要 | 用户在不能看视频直播或文字直播的时候，如：在开车的情况下，语音解说可以让用户实时知道赛况。在文字直播的基础上加入语音合成功能实现语音解说
用户想要查看球员的信息数据 | 球员信息数据 | 重要 | 需要从相关体育应用爬取数据或某些数据服务API（但定价过高，且需要企业认证）

&nbsp;

## User interaction and design（使用者交互及设计）
- 产品架构
> ![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E4%BA%A7%E5%93%81%E6%9E%B6%E6%9E%84%E5%9B%BE.png)

- 产品操作流程
> ![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E4%BA%A7%E5%93%81%E5%8A%9F%E8%83%BD%E6%93%8D%E4%BD%9C%E6%B5%81%E7%A8%8B.png)

> 人脸识别搜索：打开“球员识别”界面--->点击“输入图片地址/选取图片”--->检测与人脸库中球员图片对比的可信度（相似度）--->识别出球员--->输出球员基本信息（身高、体重、年龄、场上位置等）

> 语音解说：打开“赛程”界面>点击“文字直播”进入“文字直播”页面--->点击“语音解说”开始使用

- [产品原型主要界面](https://hejuntian.github.io/API_product_demo/start.html#g=1&p=球员识别页面)：
> ![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E7%95%8C%E9%9D%A2%E5%8E%9F%E5%9E%8B%E6%88%AA%E5%9B%BE.png)

&nbsp;

## 用户痛点
- 球迷在观看比赛的时候，可能会对部分球员不太熟悉和了解，而且球员太多、太相似，不可能每一个都记住，有时候会分不清楚场上的球员，会影响观赛体验
- 在不能观看视频直播的情况下，单纯地看文字直播可能会有些枯燥、单调；在不能看视频直播，又难去看文字直播的情况下，（如：驾驶途中），语音解说就能够派上用场

&nbsp;

## 使用到的API
- [百度人脸搜索API](http://ai.baidu.com/tech/face/search)
- [百度语音合成API](http://ai.baidu.com/tech/speech/tts)

## AI概率性
[人脸识别准确率已达99.7%](http://www.techweb.com.cn/data/2016-09-01/2384430.shtml)，但仍需要根据不同情况去评判

&nbsp;

## 球员信息抓取
- [球员信息csv档](https://github.com/Hejuntian/API_ML_AI/blob/master/nba_players_info.csv)
> ![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E6%8A%93%E5%8F%96%E7%90%83%E5%91%98%E4%BF%A1%E6%81%AF%E6%88%AA%E5%9B%BE.png)

&nbsp;

## 代码使用
- 人脸搜索API
> ![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E4%BA%BA%E8%84%B8%E6%90%9C%E7%B4%A2%E4%BB%A3%E7%A0%81%E4%BD%BF%E7%94%A8%E6%88%AA%E5%9B%BE.png)

- 语音合成API
> ![image](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E8%AF%AD%E9%9F%B3%E5%90%88%E6%88%90%E4%BB%A3%E7%A0%81%E4%BD%BF%E7%94%A8%E6%88%AA%E5%9B%BE.png)

## 使用后风险报告
- 目前市场上已有一些电子产品有球星识别的功能，如：[vivo Jovi智慧识图识别球星](https://www.ihei5.com/vivo/2018/0625/1510.html)
- 对输入图片质量要求较高，准确率有时候不稳定，对于图片中多张面孔的识别搜索有时会不准确

&nbsp;

## API使用比较
- 人脸搜索API
  - 百度人脸搜索API：可免费调用，调用量无限制，调用速度较快，但对图片的要求较高，准确率一般，人脸库可在控制台建立
  - Face++旷视人脸查找API：可免费调用，调用量没有限制说明，但有些API参数对于试用API Key无法使用，对图片的质量要求也较高，准确率相对百度人脸搜索API较好

总体来说，综合两个人脸搜索API的优势和劣势，如果对精准度没有过多的要求，个人比较倾向百度人脸搜索API

- 语音合成API
  - 百度语音合成API：离线与在线语音合成API均可免费调用，调用量无限制，准确率可观
  - 科大讯飞语音合成API：在线语音合成API可免费调用，离线语音合成API需要付费购买使用，音色库丰富，准确率可观

总体来说，在两个语音合成API使用效果差不多的情况下，个人倾向百度语音合成API

&nbsp;

## Questions（问题）
1. 人脸库仍在建立完善
2. 在人脸注册时输入的球员信息在人脸搜索的结果中没有显示

&nbsp;

## Not doing（不做）
- 球员的表情分析
- 多张人脸搜索

&nbsp;

## 清单
- [产品原型](https://hejuntian.github.io/API_product_demo/start.html#g=1&p=球员识别页面)
- [产品架构图](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E4%BA%A7%E5%93%81%E6%9E%B6%E6%9E%84%E5%9B%BE.png)
- [产品操作流程图](https://github.com/Hejuntian/API_ML_AI/blob/master/images/%E4%BA%A7%E5%93%81%E5%8A%9F%E8%83%BD%E6%93%8D%E4%BD%9C%E6%B5%81%E7%A8%8B.png)
- [球员信息csv档](https://github.com/Hejuntian/API_ML_AI/blob/master/nba_players_info.csv)
