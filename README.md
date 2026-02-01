# ⚔️ 提瓦特幸存者 (Teyvat Survivors)

> 一个类《吸血鬼幸存者》 (Vampire Survivors) 的 Roguelite 生存割草游戏。
> **本项目为 C++ 游戏开发学习项目，核心逻辑与架构参考自 Bilibili UP主 Voidmatrix 的教程。**

![C++](https://img.shields.io/badge/Language-C++-00599C?style=flat-square&logo=c%2B%2B)
![EasyX](https://img.shields.io/badge/Library-EasyX-orange?style=flat-square)
![Genre](https://img.shields.io/badge/Genre-Roguelite-red?style=flat-square)
![Reference](https://img.shields.io/badge/Reference-Voidmatrix-pink?style=flat-square&logo=bilibili )

[UP主项目学习链接](https://www.bilibili.com/video/BV1eM4m1S74K/?spm_id_from=333.337.search-card.all.click&vd_source=82e0699084c38bc7273728d632ce1e0a)

## 📖 项目简介

本项目是一个基于 **C++** 和 **EasyX 图形库** 开发的 2D 平面生存游戏。玩家将操控角色在无尽的怪物潮中生存，通过拾取经验球升级，随机选择技能组合，构建独特的战斗流派，体验“割草”般的战斗快感。

通过复现该项目，我深入学习了游戏开发中的 **组件化架构**、**动画状态机** 以及 **资源管理** 等核心概念。

## 📢 版权与致谢 (Credits & Acknowledgements)

本项目代码逻辑基于 **Voidmatrix** 的《从零开始的C++游戏开发》系列教程编写，素材与音效版权归原作者所有。仅供个人学习与技术交流使用，不用于商业用途。

* **核心教程**: [Voidmatrix (Bilibili)](https://space.bilibili.com/397186666) - 《从零开始的C++游戏开发》
* **美术素材**:
    * [Anokolisa (itch.io)](https://anokolisa.itch.io/sidescroller-pixelart-sprites-asset-pack-forest-16x16) - 场景与基础像素画资源
    * @小苏早睡 - 部分角色与特效素材
* **音乐音效**:
    * [Pixabay](https://pixabay.com/zh/sound-effects/8bit-sample-69080/) - 8bit 风格音效
* **IP 声明**: 游戏内涉及的《原神》角色形象（如纳西妲等）版权归 *HoYoverse* 所有，本项目仅作同人编程学习展示。

---

## 🎮 游戏演示

<!-- 💡 提示：运行游戏截图后，直接把图片拖到这里，GitHub 会自动生成链接 -->
![游戏运行截图](https://via.placeholder.com/800x450?text=Please+Upload+Gameplay+Screenshot)
*(游戏画面：展示技能特效与大量怪物同屏)*

## ✨ 核心功能

* **同屏海量怪物**：优化了碰撞检测算法，支持上百个敌方单位同屏流畅运行，帧率稳定。
* **Roguelite 成长体系**：
    * 升级时随机出现 3 个技能选项（如：旋律环绕、雷电场、投掷物）。
    * 技能支持等级叠加，视觉效果与数值随等级提升。
* **智能 AI 寻路**：实现了追踪 AI，怪物会根据玩家位置自动寻路包围。
* **平滑摄像机跟随**：实现了摄像机平滑插值算法 (Lerp)，聚焦玩家视野，提升操作手感。
* **动画状态机**：封装了 `Animation` 类，支持角色待机、移动、受击等状态的流畅切换。

## 🛠️ 技术栈

* **语言**: C++ (STL)
* **图形库**: EasyX Graphics Library
* **开发环境**: Visual Studio 2022
* **架构模式**: 面向对象 (OOP) + 组件化设计 (Component-Based)

## 🚀 如何运行 (How to Run)

1.  **克隆仓库**：
    ```bash
    git clone [https://github.com/kinjo886/Cpp-Teyvat-Survivors.git](https://github.com/kinjo886/Cpp-Teyvat-Survivors.git)
    ```
2.  **打开项目**：使用 Visual Studio 打开目录下的 `.sln` 解决方案文件。
3.  **环境配置**：
    * 确保已安装 EasyX 图形库。
    * 建议在 VS 顶部选择 `Release` 和 `x64` (或 x86，视 EasyX 版本而定) 模式，以获得最佳性能。
4.  **编译运行**：点击“本地 Windows 调试器”即可开始游戏。

## 👨‍💻 作者信息

**吴俊 (Wu Jun)**
* **Email**: 23jwu2@stu.edu.cn
* **Portfolio**: [我的 GitHub 主页](https://github.com/kinjo886/JIANLI_CV)

---
*感谢您的观看！如果觉得项目不错，欢迎点一个 Star ⭐️*
