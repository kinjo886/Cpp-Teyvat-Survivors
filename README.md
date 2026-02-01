# ⚔️ 提瓦特幸存者 (Teyvat Survivors)

> 一个类《吸血鬼幸存者》 (Vampire Survivors) 的 Roguelite 生存割草游戏。
> **本项目为 C++ 游戏开发学习项目，核心逻辑与架构参考自 Bilibili UP主 Voidmatrix 的教程。**

![C++](https://img.shields.io/badge/Language-C++-00599C?style=flat-square&logo=c%2B%2B)
![EasyX](https://img.shields.io/badge/Library-EasyX-orange?style=flat-square)
![Genre](https://img.shields.io/badge/Genre-Roguelite-red?style=flat-square)
![Reference](https://img.shields.io/badge/Reference-Voidmatrix-pink?style=flat-square&logo=bilibili )

## 📖 项目简介

本项目是一个基于 C++ 和 EasyX 图形库 开发的 2D 平面生存游戏。玩家将操控角色在无尽的怪物潮中生存，摒弃传统射击游戏的瞄准操作，利用自动环绕的魔法弹幕抵御敌人，体验“割草”般的战斗快感。

通过复现该项目，我深入学习了游戏开发中的 ECS (实体组件系统) 雏形、帧动画状态机 以及 Windows GDI 透明渲染 (AlphaBlend) 等核心技术。

## 📢 版权与致谢 (Credits & Acknowledgements)

本项目代码逻辑基于 **Voidmatrix** 的《从零开始的C++游戏开发》系列教程编写，素材与音效版权归原作者所有。仅供个人学习与技术交流使用，不用于商业用途。

* **核心教程**: [Voidmatrix (Bilibili)](https://space.bilibili.com/25864506?spm_id_from=333.337.0.0) - 《从零开始的C++游戏开发》
* **美术素材**:
    * [Anokolisa (itch.io)](https://anokolisa.itch.io/sidescroller-pixelart-sprites-asset-pack-forest-16x16) - 场景与基础像素画资源
    * @小苏早睡 - 部分角色与特效素材
* **音乐音效**:
    * [Pixabay](https://pixabay.com/zh/sound-effects/8bit-sample-69080/) - 8bit 风格音效
* **IP 声明**: 游戏内涉及的《原神》角色形象（如纳西妲等）版权归 *HoYoverse* 所有，本项目仅作同人编程学习展示。

* [UP主项目学习链接](https://www.bilibili.com/video/BV1eM4m1S74K/?spm_id_from=333.337.search-card.all.click&vd_source=82e0699084c38bc7273728d632ce1e0a)

---

## 🎮 游戏演示



*(游戏画面：展示自动环绕攻击与怪物追踪)*

## ✨ 核心功能 (基于当前源码实现)

- **自动环绕攻击系统 (Auto-Orbiting Attack)：**

   - 摒弃了手动瞄准，代码中实现了基于三角函数 (sin/cos) 的动态弹道算法，魔法球会随着时间推移在玩家周围进行径向和切向波动，形成呼吸式防御圈。

- **智能 AI 寻路 (Tracking AI)：**

   - 实现了边缘生成算法，敌人从屏幕四周随机刷新。

   - 敌人实时计算与玩家的向量差，归一化后自动向玩家发起直线追踪。

- **动画状态机 (Animation FSM)：**

   - 封装了 Atlas (图集) 和 Animation (动画) 类，支持角色按帧率播放行走动画，并根据移动方向自动切换左右朝向。

- **高级渲染技术 (Advanced Rendering)：**

   - 引入 MSIMG32.LIB 库，使用 AlphaBlend 函数替代传统的 putimage，实现了完美的 PNG 透明通道混合与阴影渲染。

   - 采用双缓冲绘图 (BeginBatchDraw)，配合高精度帧率控制，彻底解决画面闪烁问题。

- **交互式 UI 框架：**

   - 封装了 Button 控件基类，支持检测鼠标悬停 (Hover)、按下 (Pushed) 和 闲置 (Idle) 状态并实时切换对应贴图。

## 🛠️ 技术栈

* **语言**: C++ (STL)
* **图形库**: EasyX Graphics Library
* **系统 API**: Windows Multimedia API (Winmm.lib), Windows GDI (MSIMG32.LIB)
* **开发环境**: Visual Studio 2022
* **架构模式**: 面向对象 (OOP)

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
