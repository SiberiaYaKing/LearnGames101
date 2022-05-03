## GAMES101学习计划(2022年的flag)

### 申明
* games101闫老师对于作业有三点要求：
    1. Work alone for regular assignments, no copy-pasting from any other sources
    2. Do not publish your code (on Github, etc.) for assignments using our skeleton code
    3. Do not post your solution online.Discussion / explanation is welcomed
* 鉴于此，我还是将库中的代码去掉吧，只留下main可执行文件，此仓库仅记录我的学习成果

### 提交流程
* 切换.gitignore
* git rm -r --cached . (先删除暂存区文件)
* 正常add commit push，push要区分是origin还是private

### 展示

#### 作业 00_Transformation 展示
* 2022.04.22完成，主要是搭环境花了很多时间
    * ![image](https://github.com/SiberiaYaKing/LearnGames101/blob/master/README_IMG/00.png)
* 坑点：环境是自己搭的，没有使用games101提供的虚拟机，作业在WSL-ubuntu环境中编译运行。虽然自己搭环境比较麻烦，但是WSL可以在Windows端编写并调试代码，使用体验上比虚拟机要好一些，关于环境的搭建可以参考：
    * [Windows Linux子系统安装：配置图形界面、中文环境](https://zhuanlan.zhihu.com/p/170210673)
    * [在Windows端用VSCode调试WSL端的C++](https://blog.csdn.net/SuGeLaInys/article/details/99934184)
    * ubuntu一些必要库的安装，如cmake, gdb, egien3, g++, opencv等，自行google有很多...

#### 作业 01_Rasterization 展示
* 2022.05.03完成，还有额外要求没达成，有空再补一下
    * ![image](https://github.com/SiberiaYaKing/LearnGames101/blob/master/README_IMG/01.png)
* 坑点：由于view变换使Z轴发生翻转，所以后面求projection变换需要注意z方向的值要翻回来，所以projection矩阵最后一行应该是“0, 0, -1, 0”，参考链接：
    * [Games101-bbs-作业1，三角形颠倒问题](https://games-cn.org/forums/topic/zuoye1sanjiaoxingdiandaowenti/)