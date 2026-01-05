# 香港科技大学（广州）中文简历 LaTeX 模板

<div align="center">
  <img width="98%" src="cv.png" alt="简历预览"/>
</div>

> 📖 **Language / 语言**: [English](README_EN.md) | 简体中文

## 📋 目录

- [简介](#简介)
- [预览](#预览)
- [主要特性](#主要特性)
- [快速开始](#快速开始)
- [使用说明](#使用说明)
- [自定义配置](#自定义配置)
- [常见问题](#常见问题)
- [致谢](#致谢)
- [许可证](#许可证)

## 简介

本模板是专为香港科技大学（广州）学生设计的中文简历 LaTeX 模板，采用学校官方配色方案，提供专业、简洁的简历排版效果。

## 预览

模板采用 HKUST(GZ) 官方蓝色主题（RGB: 0, 71, 122），包含页眉页脚装饰条、校徽水印等视觉元素，呈现专业的学术简历风格。

## 主要特性

- ✅ **官方配色**：采用 HKUST(GZ) 官方蓝色主题
- ✅ **无需图片依赖**：使用 TikZ 代码绘制页眉页脚，无需手动制作背景图
- ✅ **字体兼容**：支持 Overleaf 和本地 TeX 发行版，自动适配字体
- ✅ **图标丰富**：集成 FontAwesome5 图标库
- ✅ **易于定制**：模块化设计，方便修改配色和布局

## 快速开始

### 编译环境要求

- **编译器**：XeLaTeX（必须）
- **推荐平台**：
  - 在线：[Overleaf](https://www.overleaf.com/)
  - 本地：VS Code + LaTeX Workshop 插件

### 编译步骤

1. 克隆或下载本仓库
2. 使用 XeLaTeX 编译 `main.tex`
3. 生成 PDF 简历文件

## 使用说明

### 文件结构

```
HKUST-GZ-Resume/
├── main.tex              # 主文件，编辑简历内容
├── settings.tex          # 配置文件，设置颜色、字体等
├── images/               # 图片资源文件夹
│   ├── avatar.png        # 个人证件照（推荐比例 3:4）
│   ├── UST-GZ_white_tc_L_PNG.png    # 校名 Logo（页眉使用）
│   └── in_UST-GZ_4C_en-C_PNG.png    # 校徽（水印使用）
└── README.md             # 说明文档
```

### 图片准备

在 `images` 文件夹中准备以下图片：

| 文件名 | 用途 | 要求 |
|--------|------|------|
| `avatar.png` | 个人证件照 | 推荐比例 3:4，清晰正面照 |
| `UST-GZ_white_tc_L_PNG.png` | 校名 Logo | 白色文字或透明底，用于页眉 |
| `in_UST-GZ_4C_en-C_PNG.png` | 校徽 | 用于正文中心的透明水印 |

**注意**：本模板已废弃 `header.png` 和 `footer.png`，页眉页脚由代码自动生成。

## 自定义配置

### 修改配色

在 `settings.tex` 中找到颜色定义：

```latex
\definecolor{HKUST_GZ}{RGB}{0,71,122}
```

修改 RGB 数值即可更换主题色。例如：
- 深蓝色：`{0, 51, 102}`
- 深红色：`{139, 0, 0}`

### 修改栏目标题

在 `main.tex` 中找到对应的 `\section{...}` 命令，修改文字内容即可。

示例：
```latex
\section{\makebox[0.4em][c]{\faLaptopCode}\quad 项目与实习经历}
```

### 更换图标

模板使用 FontAwesome5 图标库。查阅图标代码：[FontAwesome 图标库](https://fontawesome.com/v5/search?m=free)

常用图标示例：
- `\faGithub` - GitHub
- `\faEnvelope` - 邮箱
- `\faPhone` - 电话
- `\faPython` - Python
- `\faLaptopCode` - 编程

## 常见问题

### Q1: 图标无法显示怎么办？

**A**: 确保已正确加载 FontAwesome5 宏包。检查 `settings.tex` 中是否包含：
```latex
\usepackage{fontawesome5}
```

### Q2: 编译报错"缺少字体"？

**A**: 本模板已优化字体兼容性，默认使用 Fandol 系列字体。如仍有问题，请确认：
- 使用 XeLaTeX 编译器
- 更新 TeX 发行版到最新版本

### Q3: 如何调整页眉页脚高度？

**A**: 在 `settings.tex` 中找到 TikZ 绘图代码，修改相应的坐标参数即可。

### Q4: 可以用于英文简历吗？

**A**: 可以，但需要调整字体设置。建议使用英文专用模板以获得更好效果。

## 致谢

本模板基于开源社区的优秀项目二次开发而成，特此感谢：

### 原型模板
- **华中科技大学 HUST-CV 模板**  
  项目地址：[lessiYin/HUST-Resume-LaTeX-Template](https://github.com/lessiYin/HUST-Resume-LaTeX-Template)

### 上游基础模板
华科版本基于以下三个优秀模板修改：
- 北师大 BNUCV 模板（GitHub: LeyuDame/BNUCV）
- 西北工业大学 NPU-CV 模板（Overleaf: npu-cv）
- 武汉大学 WHU-CV 模板（小红书 @虎生）

### 本次修改内容

针对香港科技大学（广州）进行了以下适配：

1. **配色调整**：将"华科红"替换为"科广蓝"（RGB: 0, 71, 122），符合 HKUST(GZ) 官方视觉识别系统
2. **结构优化**：废弃外部图片依赖，改用 TikZ 代码绘制页眉页脚，降低使用门槛
3. **字体兼容**：优化字体设置，增加 Overleaf 和本地 TeX 发行版兼容性
4. **本地化内容**：预置"人工智能学域"、"信息枢纽"等示例，替换校徽引用逻辑

### 维护者

本模板由 **HKUST(GZ) 学生非官方组织** 维护和更新，不代表香港科技大学（广州）官方立场。

## 许可证

本项目继承原项目的开源协议，欢迎自由使用和修改。如果本模板对您有帮助，欢迎 Star ⭐ 支持！

---

<div align="center">
  <strong>祝你的简历能助你拿到心仪的 Offer！</strong><br>
  Make HKUST(GZ) Great Again!
</div>
