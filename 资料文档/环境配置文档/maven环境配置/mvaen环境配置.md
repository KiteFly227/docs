# mvaen环境配置

* **windows环境配置**

  1. 新建系统变量 MAVEN_HOME，变量值：E:\Maven\apache-maven-3.3.9<img src="https://www.runoob.com/wp-content/uploads/2018/09/1536057115-1481-20151218175411912-170761788.png" alt="img" style="zoom:80%;" />
  2. 编辑系统变量 Path，添加变量值：;%MAVEN_HOME%\bin<img src="https://www.runoob.com/wp-content/uploads/2018/09/1536057115-7470-20151218175417006-1644078150.png" alt="img" style="zoom:80%;" />
  3. setting文件配置
    <localRepository>F:/repository</localRepository>
    
    <mirror>      
      <id>nexus-aliyun</id>    
      <name>nexus-aliyun</name>  
      <url>http://maven.aliyun.com/nexus/content/groups/public</url>    
      <mirrorOf>central</mirrorOf>      
    </mirror>

* **Linux环境配置**
  1. 编辑 **/etc/profile** 文件 **sudo vim /etc/profile**，在文件末尾添加如下代码：

     export MAVEN_HOME=/usr/local/apache-maven-3.3.9
     export PATH=${PATH}:${MAVEN_HOME}/bin

  2. 保存文件，并运行如下命令使环境变量生效：

     source /etc/profile

  3. 运行mvn -v 查看版本
