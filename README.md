# wjw - 问卷网（wenjuan.com）自动化程序
![问卷网 Logo](https://s1.wenjuan.com/assets/images/business/new-login/blue-login.png )

> 为 [问卷网](https://www.wenjuan.com) 量身打造的自动化答题脚本，支持多种题型自动识别与答题策略生成。


## 📌 简介

这是一个基于 [Tampermonkey](https://www.tampermonkey.net/ ) / [Violentmonkey](https://violentmonkey.github.io/ ) / [ScriptCat](https://scriptcat.org/zh-CN/) 的用户脚本，旨在帮助用户 **快速完成问卷网上的调查问卷**。该脚本可以：

- 自动识别问卷中的常见题型，并显示在网页上，防止题型错误
- 支持自定义答题策略（比例分配、随机选择、固定答案等）
- 自动点击“继续答题”、“重新开始”等功能按钮
- 显示友好的提示信息（Toast 样式）


## 📦 功能列表

| 题型 | 支持情况 | 说明 |
|------|----------|------|
| 单选题 | ✅ | 按指定比例或随机选择 |
| 多选题 | ✅ | 支持概率控制是否勾选 |
| 填空题 | ✅ | 可配置多个文本选项随机填写 |
| 评分题（默认样式） | ✅ | 支持权重分布选择 |
| 星级评分 | ✅ | 支持随机或指定评分 |
| 矩阵评分 | ✅ | 支持每行独立设置评分策略 |
| 评价题 | ✅ | 按比例选择评分项 |
| 排序题 | ❌ | 新增中...  |



## 🛠 安装方法


1. 安装 [Tampermonkey](https://www.tampermonkey.net/) 或 [Violentmonkey](https://violentmonkey.github.io/) 或 [ScriptCat](https://scriptcat.org/zh-CN/)
2. 打开此脚本地址 或 直接复制代码
3. 点击安装 或 新建脚本，粘贴代码
4. 刷新问卷网页面，脚本将自动运行


## 💡 使用说明
作为示例演示，代码为该[示例问卷](https://www.wenjuan.com/s/UZBZJv1Y6b/)提供了处处初始代码，安装完成后请打开[示例问卷](https://www.wenjuan.com/s/UZBZJv1Y6b/)以确认脚本可以正常工作。
你可以在主函数中修改以下部分来调整答题逻辑：

```js
const q11es = [
    () => multiple(2, [50, 50, 50, 50]),     // 第2题，多选题，各选项概率相同
    () => blank(3, ["你好", "世界"]),        // 第3题，填空题，随机填入一个值
    () => scoreDefault(4, [1, 2, 3, 4, 3]),  // 第4题，评分题，按比例随机打分
    // 更多示例请查阅代码...
];
```



## 📜 使用许可

本项目采用 [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/ ) 国际许可协议。

这意味着：

- ✅ **可以自由分享和修改** 本项目代码；
- ⚠️ **必须署名原作者（zemelee）**；
- ❌ **禁止任何商业用途**；
- ⚠️ 如需用于商业场景，请联系作者获取授权。

欢迎用于学习、研究和个人使用。


## 📝 贡献指南

欢迎贡献更多题型支持、优化答题策略、修复 bug！

请提交 PR 到本仓库，或提出 Issue 进行讨论。

## 🤝 相关支持

- GitHub: [@zemelee/wjw](https://github.com/Zemelee/wjw )
- 微信公众号：做实验的研究牲
-  QQ交流群：93164446 | 850281779 | 774326264 | 427847187
- 一个可以刷问卷的网站：http://sugarblack.top
- 视频教程：预计5月底上线~

## 🚀 致谢

感谢 [问卷网](https://www.wenjuan.com) 提供平台  
感谢 [Tampermonkey](https://www.tampermonkey.net/ ) / [Violentmonkey](https://violentmonkey.github.io/ ) / [ScriptCat](https://scriptcat.org/zh-CN/) 提供的用户脚本支持环境
