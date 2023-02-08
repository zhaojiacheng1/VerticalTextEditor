<font face="楷体">

# 竖排文本编辑器
---
## 一、编辑器框架设计

&emsp;竖排文本编辑器项目旨在设计一款专门编辑竖排文本的编辑器，用以解决目前编辑器普遍竖排编辑效果差的问题，其设计思路与其他文本编辑器并没有根本上的不同。

### 1、界面是否采用robbon？

### 2、风格与word类似，采用界面和纸张页面分开的处理方法
&emsp;整体上讲，编辑器的纸张只有一页，纸张页面模式设计如下：
> `卷轴模式`：纸张页面高度可以自由设置，且设置后固定不变，但是宽度只给一行的宽度，且随着编辑文本的增加，宽度随之增加。<div align = "center">![卷轴模式](./image/卷轴模式.svg)
图1 纸张页面卷轴模式</div>

> `折页模式`：纸张页面高度和宽度可以自由设置，且设置后固定不变；折页模式下增添折线设置，用以表示折痕所在位置，并虚线表示。若折页宽度为0，或小于纸张宽度与左页边距之差，则折痕虚线不显示。<div align = "center">![折页模式](image/折页模式.svg)
图2 纸张页面折页模式</div>

### 3、页眉页脚是否需要？
&emsp;不需要

### 4、对于语言的支持？
&emsp;暂定为支持中文即可。

### 5、软件对于文本的处理
&emsp;文本存储的数据结构（文本、文本渲染设置）以段落分界。

### 6、软件对于光标的处理

### 7、软件内部引擎的划分怎么处理，是否分为编辑和渲染两个大引擎
&emsp;暂时分为编辑和渲染两大引擎

### 8、古文中支持的眉批、夹注、尾注功能

### 9、编写相关文档
&emsp;需求调研和分析阶段：`功能列表`或者`用例图`，`软件需求说明书`。
&emsp;系统设计阶段：`系统总体设计`、`系统架构规划`、`定义系统边界`、`划分系统模块`、`类详细设计`、`实现函数设计`、`界面实现设计`、`数据库设计`：`界面设计说明书`、`软件设计说明书`、`数据库设计说明书`、`技术方案选型说明书`。
&emsp;实现阶段：`单元测试报告`、`代码`和`单元测试脚本`。
&emsp;测试阶段：`项目测试计划`、`项目测试用例`、`项目测试报告`、`评审报告`。

---
## 附：标准的软件开发过程及各步骤需要编写的文档

### 一、标准的软件开发过程

&emsp;软件开发的标准过程包括六个阶段，而六个阶段需要编写的各类文件达14种之多，在每个阶段需要编写哪些文档，以及这些文件的主要内容如下：
#### 1.可行性与计划研究阶段
> - `可行性分析报告`：在可行性研究与计划阶段内，要确定该软件的开发目标和总的要求，要进行可行性分析、投资-收益分析、制定开发计划，并完成应编制的文件。
> - `项目开发计划`：编制项目开发计划的目的是用文件的形式，把对于在开发过程中各项工作的负责人员、开发进度、所需经费预算、所需软、硬件条件等问题作出的安排记载下来，以便根据本计划开展和检查本项目的开发工作。

#### 2.需求分析阶段
> - `软件需求说明书`：软件需求说明书的编制是为了使用户和软件开发者双方对该软件的初始规定有一个共同的理解，使之成为整个开发工作的基础。内容包括对功能的规定、对性能得规定等。
> - `数据要求说明书`：数据要求说明书得编制目的是为了向整个开发时期提供关于被处理数据得描述和数据采集要求的技术信息。
> - `初步的用户手册`：用户手册的编制是要使用非专门术语的语言，充分得描述该软件系统所具有的功能及基本使用方法。使用户（或潜在用户）通过本手册能够了解该软件的用途，并且能够确定在什么情况下，如何使用它。

#### 3.设计阶段
> - `概要设计说明书`：概要设计说明书又可称系统设计说明书，这里所说的系统是指程序系统。编制的目的是说明对程序系统的设计考虑，包括程序系统的基本处理流程、程序系统的组织结构、模块划分、功能分配、接口设计。运行设计、数据结构设计和出错处理设计等，为程序的详细设计提供基础。
> - `详细设计说明书`：详细设计说明书又可称程序设计说明书。编制目的是说明一个软件系统各个层次中的每一个程序（每个模块或子程序）的设计考虑，如果一个软件系统比较简单，层次很少，本文件可以不单独编写，有关内容合并入概要设计说明书。
> - `数据库设计说明书`：数据库设计说明书的编制目的是对于设计中的数据库的所有标识、逻辑结构和物理结构作出具体的设计规定。
> - `测试设计初稿`：这里所说的测试，主要是指整个程序系统的组装测试和确认测试。本文件的编制是为了提供一个对该软件的测试计划，包括对每项测试活动的内容、进度安排、设计考虑、测试数据的整理方法及评价准则。

#### 4.实现阶段
> - `模块开发卷宗`（开始编写）：模块开发卷宗是在模块开发过程中逐步编写出来的，每完成一个模块或一组密切相关的模块的复审时编写一份，应该把所有的模块开发卷宗汇集在一起。编写的目的是记录和汇总低层次开发的进度和结果，以便于对整个模块开发工作的管理和复审，并为将来的维护提供非常有用的技术信息。
> - `用户手册`完工
> - `操作手册`：操作手册的编制是为了向操作人员提供该软件每一个运行的具体过程和有关知识，包括操作方法的细节。
> - `测试计划终稿`

#### 5.测试阶段
> - `模块开发卷宗`（此阶段内必须完成）
> - `测试分析报告`：测试分析报告的编写是为了把组装测试和确认测试的结果、发现及分析写成文件加以记载。
> - `项目开发总结报告`：项目开发总结的编制是为了总结本项目开发工作的经验，说明实际取得的开发结果以及对整个开发工作的各个方面的评价

#### 6.运行与维护阶段
&emsp;开发进度月报的编制是及时向有关管理部门汇报项目开发的进展和情况，以便及时发现和处理开发过程中出现的问题。一般地，开发进度月报是以项目组为单位每月编写。如果被开发的软件系统规模比较大，整个工程项目被划分给若干个分项目组承担，开发进度月报将以分项目组为单位按月编写。

&emsp;对于一项软件而言，有些文件的编写工作可能要若干个阶段中延续进行。

&emsp;鉴于软件开发是具有创造性的脑力劳动，也鉴于不同软件在规模上和复杂程度上差别极大，本指南认为在文件编制过程中应允许一定的灵活性，并不是14种文件每种都必须编写。

</font>