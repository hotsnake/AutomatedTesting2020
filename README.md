自动化测试——经典自动化测试大作业：

使用工具WALA完成静态分析，构建代码与测试代码之间的联系，得到代码的依赖图并根据代码关系图和变更信息，筛选出受变更的测试。

目录结构

.
├── ./Data	存放测试数据，全部采用maven构建
├── ./Demo	项目生成的jar包
├── ./Project	项目源代码
├── ./README.md
└── ./Report	存放代码依赖图
使用

# 类级测试选择
java -jar testSelection.jar -c <project_target> <change_info>
# 方法级测试选择
java -jar testSelection.jar -m <project_target> <change_info>
<project_target>是待测项目target文件，比如./Data/1-ALU/target

<change_info>是记录变更信息的的文本文件，比如./Data/1-ALU/data/change_info.txt

生成代码依赖图

运行上述代码后会得到一个.dot文件，可以使用graphviz生成pdf依赖图。比如：

dot -T pdf -o class-1-ALU.pdf class.dot