# CHBIM

Chinese Historic Building Information Modeling — 基于中国古代营造体系的 BIM 组织方法

## 项目简介

本项目目标是搭建一个易用的系统，使人们能够轻松地参考《营造法式》等中国传统营造体系制作可参数化的 BIM 模型，并储存具体的项目信息。项目包含理论研究与开源软件开发两部分。

**核心思路：** 将传统营造知识（材份制、地盘分槽、侧样举折等）编码为形式化的规则与参数体系，基于 OpenCascade (OCCT) 实现参数化几何建模，最终形成面向中国古代木构建筑的 BIM 工具链。

## 项目结构

```
chbim/
├── research-notes/    研究笔记与文献
│   ├── yingzao-fashi/ 《营造法式》编码与参数化转译
│   ├── hbim/          BIM/HBIM 现有研究综述
│   ├── samples/       案例测试与体系验证
│   └── references.bib 统一文献管理
├── docs/              项目文档
├── dev-notes/         开发日志与技术备忘
├── src/               源代码
│   ├── core/          核心数据结构与规则引擎
│   ├── geometry/      OCCT 几何建模层
│   ├── parametric/    参数化生成（材份制 → 几何）
│   └── io/            导入/导出
├── tests/             测试
└── assets/            图表与示意图
```

## 开源协议

- **源代码**（`src/`）：[GNU LGPL-3.0](LICENSE)
- **研究笔记与文档**（`research-notes/`、`docs/`、`dev-notes/`）：[CC BY-SA 4.0](LICENSE-DOCS)

## 进度

项目处于初始规划阶段。

- [ ] 《营造法式》关键章节的形式化编码
- [ ] 核心数据结构设计
- [ ] OCCT 几何原型
- [ ] 案例验证

