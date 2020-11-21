经典自动化测试大作业：

使用WALA实现静态分析，构建代码与测试代码之间的联系，得到代码的依赖图并根据代码关系图和变更信息，筛选出受变更的测试。

./Demo中的testSelection.jar文件，基本使用方法如下：

# 类级测试选择
java -jar testSelection.jar -c <project_target> <change_info>
# 方法级测试选择
java -jar testSelection.jar -m <project_target> <change_info>

其中<project_target>指向待测项目target文件夹，<change_info>指向记录变更信息的的文本文件

上述操作输出一个.dot文件，可使用graphviz将其转化成.pdf的形式