# CHBIM

Chinese Historic Building Information Modeling — 基于中国古代营造体系的 BIM 组织方法

## 项目简介

本项目目标是搭建一个易用的系统，使人们能够轻松地参考《营造法式》等中国传统营造体系制作可参数化的 BIM 模型，并储存具体的项目信息。项目包含理论研究与开源软件开发两部分。

**核心思路：** 将传统营造知识（材份制、地盘分槽、侧样举折等）编码为形式化的规则与参数体系，基于 OpenCascade (OCCT) 实现参数化几何建模，最终形成面向中国古代木构建筑的 BIM 工具链。

## 项目结构

```
chbim/
├── research-notes/        研究笔记与文献
│   ├── encoding/          基于"缝"的构件编码体系
│   ├── parametric/        基于《营造法式》的参数化体系
│   ├── yingzao-fashi/     《营造法式》文献综述
│   ├── hbim/              BIM/HBIM 现有研究综述
│   ├── software-analysis/ 现有软件综述（Revit/SolidWorks/FreeCAD）
│   ├── case-studies/      案例研究
│   │   └── wanfodian/     山西平遥镇国寺万佛殿
│   └── feedback/          反馈记录
├── docs/                  项目文档
├── dev-notes/             开发日志与技术备忘
│   ├── cpp/               C++ 学习笔记
│   └── occt/              OpenCASCADE 方法积累
├── prototypes/            软件原型设计
│   ├── mvp/               最小可行方案
│   └── features/          主要功能设计
├── presets/               类型学预设与族（数据层）
│   ├── song-style/        宋式预设模板
│   ├── qing-style/        清式预设模板
│   └── general-style/     通用预设模板
├── src/                   源代码
│   ├── core/              核心数据结构与规则引擎
│   │   ├── encoding/      构件编码系统
│   │   ├── joinery/       榫卯系统
│   │   ├── types/         类型学与族管理
│   │   └── rules/         规则引擎
│   ├── geometry/          OCCT 几何建模层
│   │   ├── shapes/        基础几何形状
│   │   ├── assemblies/    装配关系（几何约束）
│   │   └── relations/     点线面几何关系
│   ├── parametric/        参数化生成（材份制 → 几何）
│   │   ├── cai-fen/       材份制参数系统
│   │   └── generators/    参数 → 几何生成器
│   ├── properties/        属性系统（Revit 属性 + 设计树）
│   ├── io/                导入/导出
│   └── app/               应用层（查看、编辑、验证等）
├── tests/                 测试
│   ├── unit/              单元测试
│   └── integration/       集成测试
└── assets/                图表与示意图
```

## 开源协议

- **源代码**（`src/`）：[GNU LGPL-3.0](LICENSE)
- **研究笔记与文档**（`research-notes/`、`docs/`、`dev-notes/`、`prototypes/`、`presets/`）：[CC BY-SA 4.0](LICENSE-DOCS)

## 进度

项目处于初始规划阶段。

- [ ] 《营造法式》关键章节的形式化编码
- [ ] 核心数据结构设计
- [ ] OCCT 几何原型
- [ ] 案例验证

