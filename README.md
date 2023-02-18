# 竖排文本编辑器
---
## 一、编辑器框架设计

&emsp;竖排文本编辑器项目旨在设计一款专门编辑竖排文本的编辑器，用以解决目前编辑器普遍竖排编辑效果差的问题，其设计思路与其他文本编辑器并没有根本上的不同。

### 1、界面是否采用robbon？

### 2、风格与word类似，采用界面和纸张页面分开的处理方法

&emsp;整体上讲，编辑器的纸张只有一页，纸张页面模式设计如下：
> **卷轴模式**：纸张页面高度可以自由设置，且设置后固定不变，但是宽度只给一行的宽度，且随着编辑文本的增加，宽度随之增加。<div align = "center">![卷轴模式](./image/卷轴模式.svg)
图1 纸张页面卷轴模式</div>

> **折页模式**：纸张页面高度和宽度可以自由设置，且设置后固定不变；折页模式下增添折线设置，用以表示折痕所在位置，并虚线表示。若折页宽度为0，或小于纸张宽度与左页边距之差，则折痕虚线不显示。<div align = "center">![折页模式](image/折页模式.svg)
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

> - **可行性分析报告**：在可行性研究与计划阶段内，要确定该软件的开发目标和总的要求，要进行可行性分析、投资-收益分析、制定开发计划，并完成应编制的文件。
> - **项目开发计划**：编制项目开发计划的目的是用文件的形式，把对于在开发过程中各项工作的负责人员、开发进度、所需经费预算、所需软、硬件条件等问题作出的安排记载下来，以便根据本计划开展和检查本项目的开发工作。

#### 2.需求分析阶段

> - **软件需求说明书**：软件需求说明书的编制是为了使用户和软件开发者双方对该软件的初始规定有一个共同的理解，使之成为整个开发工作的基础。内容包括对功能的规定、对性能得规定等。
> - **数据要求说明书**：数据要求说明书得编制目的是为了向整个开发时期提供关于被处理数据得描述和数据采集要求的技术信息。
> - **初步的用户手册**：用户手册的编制是要使用非专门术语的语言，充分得描述该软件系统所具有的功能及基本使用方法。使用户（或潜在用户）通过本手册能够了解该软件的用途，并且能够确定在什么情况下，如何使用它。

#### 3.设计阶段

> - **概要设计说明书**：概要设计说明书又可称系统设计说明书，这里所说的系统是指程序系统。编制的目的是说明对程序系统的设计考虑，包括程序系统的基本处理流程、程序系统的组织结构、模块划分、功能分配、接口设计。运行设计、数据结构设计和出错处理设计等，为程序的详细设计提供基础。
> - **详细设计说明书**：详细设计说明书又可称程序设计说明书。编制目的是说明一个软件系统各个层次中的每一个程序（每个模块或子程序）的设计考虑，如果一个软件系统比较简单，层次很少，本文件可以不单独编写，有关内容合并入概要设计说明书。
> - **数据库设计说明书**：数据库设计说明书的编制目的是对于设计中的数据库的所有标识、逻辑结构和物理结构作出具体的设计规定。
> - **测试设计初稿**：这里所说的测试，主要是指整个程序系统的组装测试和确认测试。本文件的编制是为了提供一个对该软件的测试计划，包括对每项测试活动的内容、进度安排、设计考虑、测试数据的整理方法及评价准则。

#### 4.实现阶段

> - **模块开发卷宗**（开始编写）：模块开发卷宗是在模块开发过程中逐步编写出来的，每完成一个模块或一组密切相关的模块的复审时编写一份，应该把所有的模块开发卷宗汇集在一起。编写的目的是记录和汇总低层次开发的进度和结果，以便于对整个模块开发工作的管理和复审，并为将来的维护提供非常有用的技术信息。
> - **用户手册**完工
> - **操作手册**：操作手册的编制是为了向操作人员提供该软件每一个运行的具体过程和有关知识，包括操作方法的细节。
> - **测试计划终稿**

#### 5.测试阶段

> - **模块开发卷宗**（此阶段内必须完成）
> - **测试分析报告**：测试分析报告的编写是为了把组装测试和确认测试的结果、发现及分析写成文件加以记载。
> - **项目开发总结报告**：项目开发总结的编制是为了总结本项目开发工作的经验，说明实际取得的开发结果以及对整个开发工作的各个方面的评价

#### 6.运行与维护阶段

&emsp;开发进度月报的编制是及时向有关管理部门汇报项目开发的进展和情况，以便及时发现和处理开发过程中出现的问题。一般地，开发进度月报是以项目组为单位每月编写。如果被开发的软件系统规模比较大，整个工程项目被划分给若干个分项目组承担，开发进度月报将以分项目组为单位按月编写。

&emsp;对于一项软件而言，有些文件的编写工作可能要若干个阶段中延续进行。

&emsp;鉴于软件开发是具有创造性的脑力劳动，也鉴于不同软件在规模上和复杂程度上差别极大，本指南认为在文件编制过程中应允许一定的灵活性，并不是14种文件每种都必须编写。

---
## [附：探索LibreOffice的源代码库](https://www.libreofficechina.org/%E8%AF%91-%E6%8E%A2%E7%B4%A2libreoffice%E7%9A%84%E6%BA%90%E4%BB%A3%E7%A0%81%E5%BA%93/)

&emsp;本文介绍了LibreOffice源代码库的主要目录结构及用途，有助于您快速入门LibreOffice的代码开发。这是中文翻译，原文发表在Lanedo博客:http://www.lanedo.com/exploring-the-libreoffice-code-base/。

&emsp;**本文最初由Eilidh McAdam发表于[Lanedo博客](http://www.lanedo.com/exploring-the-libreoffice-code-base/)，由LibreOffice中文社区翻译。**

&emsp;初次查看LibreOffice源代码，您会被它庞大的代码量所吓倒。本文列出了LibreOffice代码库中一些有用的目录结构，希望有助于您入门。

### 总体布局

&emsp;LibreOffice由100多个相互依赖的模块组成，每个模块位于[LibreOffice源代码目录](https://cgit.freedesktop.org/libreoffice/core/tree/)下的一个文件夹中。请注意，除非特别注明，以下提到的所有路径都是相对于这个根目录的。每个模块一般都遵循特定的规则，至少包含以下文件或目录：
> **moduledir/README**
> - 一般包含关于该模块用途以及内容的描述。您可以在[docs.libreoffice.org](https://docs.libreoffice.org/)找到所有的LibreOffice模块以及这些模块README第一行内容的清单。
> 
> **moduledir/*.mk**
> - 各种编译可能性下的gbuild makefiles。
> 
> **moduledir/source/**
> - 源代码（一般情况下是C++）。经常会有源代码以子模块（submodules）的形式出现。

### 头文件（headers）

&emsp;您会在多个地方看到头文件，这取决于定义的接口需要的最小作用范围（Scope）。
> **[include/](https://cgit.freedesktop.org/libreoffice/core/tree/include)**
> - 模块间的头文件。
> 
> **moduledir/inc/**
> - 模块内的头文件。
> 
> **moduledir/source/submoduledir/inc/**
> - 仅某个子模块要求的头文件。

&emsp;在偶然的情况下，头文件也有可能在它们的.cxx函数实现中一同出现。

### 用户界面（UI）

&emsp;如果一个模块有关联的GUI，则主要存在两种情况。目前，将用户界面规范从老旧的.src/.hrc格式转换为基于xml的Glade/Gtk3.ui格式的工作正在进行中。
> **moduledir/uiconfig/**
> - 新的Glade风格的.ui文件。
> 
> **moduledir/source/ui/**
> - 其他的.src文件。

### 编译系统

&emsp;有一个来自2013年米兰LibreOffice年会上的非正式幻灯片，探讨了[LibreOffice的编译系统状况](https://conference.libreoffice.org/talks/2013/content/sessions/050/files/LOConf2013_gbuild.pdf)。以下部分只列出了简短的概要，该幻灯片对一些细节有更细致的描述。
> **[solenv/](https://cgit.freedesktop.org/libreoffice/core/tree/solenv)**
> - 包含编译系统的很多重要部分。
> 
> **[solenv/gbuild](https://cgit.freedesktop.org/libreoffice/core/tree/solenv/gbuild)**
> - gbuild实现。
> 
> **[solenv/bin](https://cgit.freedesktop.org/libreoffice/core/tree/solenv/bin);[solenv/bin/modules/](https://cgit.freedesktop.org/libreoffice/core/tree/solenv/bin/modules)**
> - Perl编译和打包工具。
> 
> **[scp2/](https://cgit.freedesktop.org/libreoffice/core/tree/scp2)**
> - 打包和安装的配置文件。

&emsp;当使用`./autogen.sh`以及`make`完成了LibreOffice的编译之后，一个可运行的完整安装可在以下位置找到：**instdir/program/**。在那里您可以找到`soffice.bin`以及`soffice`。前者是LibreOffice的主要二进制程序。当首次运行时，它建立用户配置文件（user profile）并退出，之后就可以再次以正常方式运行了。要避免该过程，应当使用包装程序`soffice`作为测试目的来运行LibreOffice。当以debugger模式运行LibreOffice时，应当直接使用`soffice.bin`。

### 主要部件

#### LibreOffice Writer文本文档

&emsp;由于LibreOffice在历史上属于Sun的Star分支，它的主要部件位置包含了指向该legacy的提示。比如，Writer模块包含在`sw/`目录（StarWriter）。
> **[sw/](https://cgit.freedesktop.org/libreoffice/core/tree/sw)**
> - Writer的主要模块。
> 
> **[starmath/](https://cgit.freedesktop.org/libreoffice/core/tree/starmath)**
> - 数学公式编辑器。
> 
> **[swext/](https://cgit.freedesktop.org/libreoffice/core/tree/swext)**
> - 内置的Writer扩展。

#### LibreOffice Calc电子表格

> **[sc/](https://cgit.freedesktop.org/libreoffice/core/tree/sc)**
> - Calc的主要代码。
> 
> **[chart2/](https://cgit.freedesktop.org/libreoffice/core/tree/chart2)**
> - Calc的图表实现。

#### LibreOffice Draw绘图（以及LibreOffice Impress演示文稿）

> **[sd/](https://cgit.freedesktop.org/libreoffice/core/tree/sd)**
> - Draw和Impress共用一个模块以及这里的相当大一部分代码。
> 
> **[sdext/](https://cgit.freedesktop.org/libreoffice/core/tree/sdext)**
> - Draw和Impress的扩展。

#### 仅LibreOffice Impress演示文稿

> **slideshow/**
> - Impress的幻灯片演示引擎。

### 图形模块

> **[svx/](https://cgit.freedesktop.org/libreoffice/core/tree/svx)**
> - 包含由几个主要模块共享的图形（graphics）辅助代码，尤其是Draw和Impress。
> 
> **[drawinglayer/](https://cgit.freedesktop.org/libreoffice/core/tree/drawinglayer)**
> - 为绘图对象提供了一个API。

### 文档

> **[sfx2/](https://cgit.freedesktop.org/libreoffice/core/tree/sfx2)**
> - 包含被sw，sc和sd使用的用于调用document shells的框架。该模块包含文档载入及保存处理，文档载入和保存会分别激发正确的导入（import）和导出（export）筛选器。
> 
> **[writerfilter/](https://cgit.freedesktop.org/libreoffice/core/tree/writerfilter)**
> - Writer .rtf导入筛选器，以及部分的.docx导入筛选器。
> 
> **[writerperfect/](https://cgit.freedesktop.org/libreoffice/core/tree/writerperfect)**
> - 一个Writer导入筛选器家族，包含WordPerfect，Microsoft Publisher以及Microsoft Visio文档格式导入筛选器。
> 
> **[oox/](https://cgit.freedesktop.org/libreoffice/core/tree/oox)**
> - 对微软OOXML格式解析的支持（.docx,.xlsx,etc.）

---
## [附：Writer Application Code](https://docs.libreoffice.org/sw.html)

Exact history was lost before Sept. 18th, 2000, but old source code comments show that Writer core dates back until at least November 1990.

### Module Contents

- `inc`: headers available to all source files inside the module
- `qa`: unit, slow and subsequent tests
- `sdi`
- `source`: see below
- `uiconfig`: user interface configuration
- `util`: UNO passive registration config

### Source Contents

- `core`: Writer core (document model, layout, UNO API implementation)
- `filter`: Writer internal filters
    - `ascii`: plain text filter
    - `basflt`
    - `docx`: wrapper for the UNO DOCX import filter (in writerfilter) for autotext purposes
    - `html`: HTML filter
    - `inc`: include files for filters
    - `rtf`: thin copy&paste helper around the UNO RTF import filter (in writerfilter)
    - `writer`
    - `ww8`: DOC import, DOC/DOCX/RTF export
    - `xml`: ODF import/export, subclassed from xmloff (where most of the work is done)
- `uibase`: user interface (those parts that are linked into `sw` & always loaded)
- `ui`: user interface (optional parts that are loaded on demand (`swui`))

### Core

There is a good overview documentation of basic architecture of Writer core in the OOo wiki:

- https://wiki.openoffice.org/wiki/Writer/Core_And_Layout
- https://wiki.openoffice.org/wiki/Writer/Text_Formatting

Writer specific WhichIds are defined in `sw/inc/hintids.hxx`.

The details below are mainly about details missing from the wiki pages.

### SwDoc

The central class for a document is `SwDoc`, which represents a document.

A lot of the functionality is split out into separate Manager classes, each of which implements some `IDocument*` interface; there are `SwDoc::getIDocument*()` methods to retrieve the managers.

However there are still too many members and methods in this class, many of which could be moved to some Manager or other…

### SwNodes

Basically a (fancy) array of `SwNode` pointers. There are special subclasses of `SwNode` (`SwStartNode` and `SwEndNode`) which are used to encode a nested tree structure into the flat array; the range of nodes from `SwStartNode` to its corresponding `SwEndNode` is sometimes called a “section” (but is not necessarily what the high-level document model calls a “Section”; that is just one of the possibilities).

The `SwNodes` contains the following top-level sections:

1. Empty
2. Footnote content
3. Frame / Header / Footer content
4. Deleted Change Tracking content
5. Body content

### Undo

The Undo/Redo information is stored in a `sw::UndoManager` member of `SwDoc`, which implements the `IDocumentUndoRedo` interface. Its members include a `SwNodes` array containing the document content that is currently not in the actual document but required for Undo/Redo, and a stack of SwUndo actions, each of which represents one user-visible Undo/Redo step.

There are also `ListActions` which internally contain several individual `SwUndo` actions; these are created by the StartUndo/EndUndo wrapper methods.

### Text Attributes

The sub-structure of paragraphs is stored in the `SwpHintsArray` member `SwTextNode::m_pSwpHints`. There is a base class `SwTextAttr` with numerous subclasses; the `SwTextAttr` has a start and end index and a `SfxPoolItem` to store the actual formatting attribute.

There are several sub-categories of `SwTextAttr`:

- formatting attributes: Character Styles (`SwTextCharFormat`, `RES_TXTATR_CHARFMT`) and Automatic Styles (no special class, `RES_TXTATR_AUTOFMT`): these are handled by `SwpHintsArray::BuildPortions` and MergePortions, which create non-overlapping portions of formatting attributes.
- nesting attributes: Hyperlinks (`SwTextINetFormat`, `RES_TXTATR_INETFMT`), Ruby (`SwTextRuby`, `RES_TXTATR_CJK_RUBY`) and Meta/MetaField (`SwTextMeta`, `RES_TXTATR_META/RES_TXTATR_METAFIELD`): these maintain a properly nested tree structure. The Meta/Metafield are “special” because they have both start/end and a dummy character at the start.
- misc. attributes: Reference Marks, ToX Marks
- attributes without end: Fields, Footnotes, Flys (`AS_CHAR`) These all have a corresponding dummy character in the paragraph text, which is a placeholder for the “expansion” of the attribute, e.g. field content.

### Fields

There are multiple model classes involved for fields:

- `enum SwFieldIds` enumerates the different types of fields.
- `SwFieldType` contains some shared stuff for all fields of a type. There are many subclasses of `SwFieldType`, one for each different type of field. For most types of fields there is one shared instance of this per type, which is created in `DocumentFieldsManager::InitFieldTypes()` but for some there are more than one, and they are dynamically created, see `DocumentFieldsManager::InsertFieldType()`. An example for the latter are variable fields (`SwFieldIds::GetExp/SwFieldIds::SetExp`), with one SwFieldType per variable.
- `SwXFieldMaster` is the UNO wrapper of a field type. It is a `SwClient` registered at the `SwFieldType`. Its life-cycle is determined by UNO clients outside of `sw`; it will get disposed when the `SwFieldType` dies.
- `SwFormatField` is the `SfxPoolItem` of a field. The `SwFormatField` is a `SwClient` registered at its `SwFieldType`. The `SwFormatField` owns the `SwField` of the field.
- `SwField` contains the core logic of a field. The `SwField` is owned by the `SwFormatField` of the field. There are many subclasses of `SwField`, one for each different type of field. Note that there are not many places that can Expand the field to its correct value, since for example page number fields require a View with an up to date layout; therefore the correct expansion is cached.
- `SwTextField` is the text attribute of a field. It owns the `SwFormatField` of the field (like all text attributes).
- `SwXTextField` is the UNO wrapper object of a field. It is a `SwClient` registered at the `SwFormatField`. Its life-cycle is determined by UNO clients outside of `sw`; it will get disposed when the `SwFormatField` dies.

### Lists

- `SwNumFormat` (subclass of `SvxNumFormat`) determines the formatting of a single numbering level.
- `SwNumRule` (NOT a subclass of `SvxNumRule`) is a list style, containing one `SwNumFormat` per list level. `SwNumRule::maTextNodeList` is the list of `SwTextNode` that have this list style applied.
- `SwNumberTreeNode` is a base class that represents an abstract node in a hierarchical tree of numbered nodes.
- `SwNodeNum` is the subclass of `SwNumberTreeNode` that connects it with an actual `SwTextNode` and also with a `SwNumRule`; `SwTextNode::mpNodeNum` points back in the other direction
- `SwList` represents a list, which is (mostly) a vector of `SwNodeNum` trees, one per S`wNodes` top-level section (why that?).
- `IDocumentListsAccess`, `sw::DocumentListsManager` owns all SwList instances, and maintains mappings:
    - from list-id to `SwList`
    - from list style name to `SwList` (the “default” `SwList` for that list style)
- `IDocumentListItems`, `sw::DocumentListItemsManager` contains a set of all `SwNodeNum` instances, ordered by `SwNode` index
- the special Outline numbering rule: `SwDoc::mpOutlineRule`
- `IDocumentOutlineNodes`, `sw::DocumentOutlineNodesManager` maintain a list (which is actually stored in `SwNodes::m_pOutlineNodes`) of `SwTextNodes` that either have the Outline numrule applied, or have the `RES_PARATR_OUTLINELEVEL` item set (note that in the latter case, the `SwTextNode` does not have a `SwNodeNum` and is not associated with the `SwDoc::mpOutlineRule`).
- `SwTextNodes` and paragraph styles have items/properties:
    - `RES_PARATR_OUTLINELEVEL/"OutlineLevel"` to specify an outline level without necessarily having the outline `SwNumRule` assigned
    - `RES_PARATR_NUMRULE/"NumberingStyleName"` the list style to apply; may be empty "" which means no list style (to override inherited value) Only `SwTextNode` has these items:
    - `RES_PARATR_LIST_ID/"ListId"` determines the `SwList` to which the node is added
    - `RES_PARATR_LIST_LEVEL/"NumberingLevel"` the level at which the `SwTextNode` will appear in the list
    - `RES_PARATR_LIST_ISRESTART/"ParaIsNumberingRestart"` restart numbering sequence at this `SwTextNode`
    - `RES_PARATR_LIST_RESTARTVALUE/"NumberingStartValue"` restart numbering sequence at this `SwTextNode` with this value
    - `RES_PARATR_LIST_ISCOUNTED/"NumberingIsNumber"` determines if the node is actually counted in the numbering sequence; these are different from "phantoms" because there’s still a `SwTextNode`.

Note that there is no UNO service to represent a list.

### Layout

The layout is a tree of `SwFrame` subclasses, the following relationships are possible between frames:

- You can visit the tree by following the upper, lower, next and previous pointers.
- The functionality of flowing of a frame across multiple parents (e.g. pages) is implemented in `SwFlowFrame`, which is not an `SwFrame` subclass. The logical chain of such frames can be visited using the follow and precede pointers. (“Leaf” is a term that refers to such a relationship.)
- In case a frame is split into multiple parts, then the first one is called master, while the others are called follows.