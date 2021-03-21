# java运行环境配置

* **windows环境配置**

  1. 配置JAVA_HOME 

     变量名：JAVA_HOME 

     变量值：电脑上JDK安装的绝对路径

  2. 修改Path变量，新建两条路径

     %JAVA_HOME%\bin
     %JAVA_HOME%\jre\bin

  3.  新建/修改 CLASSPATH 变量，输入/在已有的变量值后面添加：

     变量名：CLASSPATH
     变量值：.;%JAVA_HOME%\lib\dt.jar;%JAVA_HOME%\lib\tools.jar;

* **linux环境配置**

  1. 给所有用户配置java环境

     运行 vim /etc/profile 按照以下配置编辑：

     ​	#configuration java development enviroument
     ​	export JAVA_HOME=/usr/local/jdk1.8
     ​	export PATH=$JAVA_HOME/bin:$PATH 
     ​	export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar 

  2. 重新加载系统配置文件:

     source /etc/profile