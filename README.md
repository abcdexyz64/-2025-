# 业余无线电考试模拟训练系统  
*A structured training tool for Amateur Radio A/B/C License Examination*

本项目提供一个稳定、可扩展的业余无线电考试训练工具，支持多种训练模式与题库管理方式。整体逻辑参考业余电台的操作方式（模式切换、确认流程、信息规范化），注重可用性与可维护性。

## Features（项目特性）

### 📚 题库管理
- 内置 A/B/C 级题库与全集题库  
- 支持导入自定义 `.txt` 格式题库  
- 自动识别题库目录下的 `photo/` 图片目录  
- 若不存在，自动使用 `TK/photo` 作为默认路径  

### 📝 题目展示
- 显示题号 `[J]`、章节 `[P]`、内部编号 `[I]`  
- 完整呈现题干与选项  
- 自动加载 `[F]` 图片字段  
- 支持 `.jpg/.png/.jpeg`，宽度自动限制在 600px  

### 🎓 学习模式
- 顺序模式：按题库顺序逐题练习（自动显示正确答案）  
- 模拟考试模式：随机抽题、计时、评分、错题回顾  

### 🔍 智能搜索
- 关键字搜索：题干、选项、编号全面匹配  
- 章节搜索：支持部分章节匹配  
- 编号搜索（呼号前缀匹配）  
- 大小写不敏感  
- 字符近似匹配（1/l/I、0/O 等）  
- 搜索状态可返回  

### ✔️ 答题交互
- 自动识别单选/多选题  
- 清除选择  
- 上一题 / 下一题  
- 支持键盘快捷键  

### 🖥 界面功能
- 工具栏：导入、顺序练习、模拟考试、搜索  
- 状态栏：显示当前模式、题目进度  

## Project Structure（项目结构）

TK/
├── main.py
├── requirements.txt
├── README.md
└── TK/
    ├── A.txt
    ├── B.txt
    ├── C.txt
    ├── All.txt
    └── photo/

## Question Bank Format（题库格式）

[J]题号
[P]章节号
[I]内部编号
[Q]问题内容
[T]正确答案
[A]选项A
[B]选项B
[C]选项C
[D]选项D
[F]图片文件名（可选）

## Installation（安装步骤）

pip install -r requirements.txt
python main.py

## Source of Question Bank（题库来源与勘误）

题库来源：http://www.bjwxdxh.org.cn/

勘误：《总题库附图标记.pdf》第六行左数第二张图片名  
原为 `LK060`，正确应为 `LK0603`

## Version Status
- A/B/C/All 内置题库  
- 顺序模式  
- 模拟考试  
- 图片加载  
- 三类搜索  
- 近似匹配  
- 返回功能  
- 单选/多选支持  
