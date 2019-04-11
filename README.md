# intellij-idea 配置

开发人员天天都要面对 IDE 工具（能用记事本加编译软件大神级别的除外），就比如我现在从事 Java 开发工作，天天要面对 [IntelliJ IDEA](https://www.jetbrains.com/idea/)   
<img src="https://raw.githubusercontent.com/itlad/intellij-idea/master/.assets/idea.png" alt="IntelliJ IDEA" width="111"/>  
但是我在使用中发现该软件在 Mac/Linux 中渲染的效果比 Windows 中好，因为我是个完美控，所以就有了这篇文章的出现。废话不多说，先看看效果：

![主界面](https://raw.githubusercontent.com/itlad/intellij-idea/master/.assets/主界面.png)  
![代码视图](https://raw.githubusercontent.com/itlad/intellij-idea/master/.assets/代码视图.png)  

## 安装配置
* **克隆我的仓库**
从我的 [GitHub](https://github.com/itlad/intellij-idea) 克隆相关的文件到本地
```git
git clone https://github.com/itlad/intellij-idea.git
cd intellij-idea
```

* **字体安装**
拷贝fonts目录下的字体到 IntelliJ IDEA 的安装目录的 **jre64\lib\fonts** 下。以我这里为例则拷贝到 C:\Program Files\JetBrains\IntelliJ IDEA 2019.1\jre64\lib\fonts 目录。其实之前是可以直接安装字体后重启 IntelliJ IDEA 也能行，但是不知从什么时候安装的字体在字体列表中找不到了，所以以这个方法能正常设置。

* **导入配置**
打开 IntelliJ IDEA 软件，依次点击 **File -> Import Settings** ，然后在弹出的对话框中找到下载的 [settings.zip]() 文件并单击 OK 按钮完成导入。此时会提示重启 IntelliJ IDEA ，单机重启即可。

* **修改 Maven 配置（不用maven的跳过）**
打开 **File -> Settings -> Build.Execution,Deployment -> Build Tools -> Maven** 设置选项中，根据个人的Maven安装配置相应的选项

## 插件安装
按照上面的步骤已经能配置焕然一新的界面和字体效果。但是对于我 Java 开发人员来说，还要安装一些插件来辅助能使我们的工作效率事半功倍。下面介绍一下我常用的插件，当然如果你有其他更好的选择请@我并留言具体的插件，我会不定期更新。

### .ignore
生成各种ignore文件，一键创建git ignore文件的模板。  
**使用方式：** project explorer => 项目目录 => 右键 => New => .ignore

### lombok
支持lombok的各种注解，从此不用写getter setter这些 可以把注解还原为原本的java代码 非常方便  
**使用方式：** @Data、@Getter、@Setter

### Alibaba Java Coding Guidelines
阿里巴巴出品的java代码规范插件，可以扫描整个项目 找到不规范的地方 并且大部分可以自动修复  

### GsonFormat
一键根据json文本生成java类 非常方便  
**使用方式：** 编辑器 => Alt+S 或 Alt+Insert => GsonFomat

###  Maven Helper
一键查看maven依赖，查看冲突的依赖，一键进行exclude依赖  
**使用方式：**打开项目的pom.xml文件，在文件编辑器的左下方，会看到两个tab，一个是“Text”，另一个是“Dependency Analyzer”

### VisualVM Launcher
运行java程序的时候启动visualvm，方便查看jvm的情况 比如堆内存大小的分配，某个对象占用了多大的内存，jvm调优必备工具  
**使用方式：** 选择入口函数 => Run With VisualVM ... 或 Debug With VisualVM ...

### GenerateAllSetter
一键调用一个对象的所有set方法并且赋予默认值 在对象字段多的时候非常方便  
**使用方式：** 创建对象实例变量 => 选中变量 => 右键 => generate all setter

### MyBatisCodeHelperPro
mybatis代码自动生成插件，大部分单表操作的代码可自动生成 减少重复劳动 大幅提升效率  
**使用方式：**
		1.mapper文件（即表对应的dao）与xml文件自由切换，方便代码评审； 
		2.自动代码生成功能提高开发效率，mysql数据库创建好表结构，写完 pojo（注意字段类型要统一用对象类型！）,即可生成 xml、mapper、service ； 
		3.mapper的命名规则比较统一，可提高代码风格一致性； 
		4.使用方法结合：Alt + insert 快捷键

### Rainbow Brackets
彩虹颜色的括号 看着很舒服 敲代码效率变高

### Translation
最好用的翻译插件，功能很强大，界面很漂亮

### CamelCase
将不是驼峰格式的名称，快速转成驼峰格式，安装好后，选中要修改的名称  
**使用方式：** shift+alt+u

### CodeGlance
在编辑区的右侧显示的代码地图。

### AceJump
AceJump其实是一款能够代替鼠标的软件，只要安装了这款插件，可以在代码中跳转到任意位置。
按快捷键进入 AceJump 模式后（默认是 Ctrl+J），再按任一个字符，插件就会在屏幕中这个字符的所有出现位置都打上标签，你只要再按一下标签的字符，就能把光标移到该位置上。换言之，你要移动光标时，眼睛一直看着目标位置就行了，根本不用管光标的当前位置

### Markdown support
安装这个插件之后，打开.md文件就可以通过一个支持md的视图查看和编辑内容。一般用于写README.md文件

### FindBugs-IDEA 
潜在 Bug 检查

### GenerateSerialVersionUID
利用 IntelliJ IDEA 自动生成serialVersionUID。进入Default Settings，在Inspections设置页面中，勾选Serializable class without 'serialVersionUID'，并且还可以在Severity中设置提示级别，如Warning、Error等，默认为Warning，也建议选择Warning级别的提示。创建一个类并实现Serializable接口，然后按alt+Enter键，即可收到提示，然后选择SerialVersionUID

### Solarized Theme
一个还不错的主题插件