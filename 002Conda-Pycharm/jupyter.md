## 1.修改文件默认存储路径
1）在打算存放文件的位置先新建一个文件夹，最好是英文的
2）复制文件地址备用
3）打开Anaconda Prompt，找到配置文件路径:
```
jupyter notebook --generate-config
``` 
4）修改配置文件
```
C:\Users\HS\.jupyter\jupyter_notebook_config.py
```
根据路径以记事本的方式打开上述文件
文件内搜索并找到 # c.NotebookApp.notebook_dir = ''
去掉该行前面的“#”，注意：这行前面也不能有空格
然后将新的路径填在单引号中，保存配置文件

5）修改图标属性
在开始菜单找到Jupyte Notebook快捷键
右击选择更多，打开文件位置
找到对应的Jupyte Notebook快捷图标
右击选择属性/目标，去掉后面的 "%USERPROFILE%/"
然后点击应用/确定

6）重新启动Jupyter Notebook即可　　



## 2.jupter的四种模式
1）编辑模式--绿色--enter键
2）命令模式--蓝色--esc键 

3）markdown模式:esc+m
4）code模式:esc+y


## 3.常用快捷键

1）命令模式下
```
A: 在上面插入代码块
B: 在下面插入代码块
D,D: 删除选中单元 按两下
X: 剪切选择的代码块
C: 复制选择的代码块
V: 粘贴到下面


上: 选择上面的代码块
下: 选择下面的代码块


Ctrl-Enter: 运行选中的代码块
Shift-Enter: 运行选中代码块,并跳转下一行
Alt-Enter:运行选中代码块，并插入新的一行

```

2）编辑模式下
```
Ctrl-D: 删除整行

Ctrl-上: 跳到单元格起始处
Ctrl-下: 跳到单元格最后
Ctrl-左: 跳到单词左边
Ctrl-右: 跳到单词右边

Ctrl-]: 缩进 
Ctrl-[: 取消缩进

Tab: 代码完成或缩进
Shift-Tab: 工具提示

Ctrl-/: 评论 注释

Ctrl-D: 删除整行
Ctrl-U: 撤销选择
```

## 4.魔法函数
使用魔法函数可以简单的实现一些单纯python要很麻烦才能实现的功能
```
%：行魔法函数，只对本行代码生效。

%%：Cell魔法函数，在整个Cell中生效，必须放于Cell首行。

%lsmagic：列出所有的魔法函数

%magic查看各个魔法函数的说明

```

## 5.使用技巧
1）使用分号可以阻止该行函数的结果输出
2）库、方法或变量前加上 ?获得快速语法说明
3）按tab键查看提示信息或者补全命令

4）解除cell只会显示最后一个输出结果的限制
```python
#法1：使用print()命令

#法2：通过ipython包
from IPython.core.interactiveshell import InteractiveShell
InteractiveShell.ast_node_interactivity = "all"
```
5）显示单元格行号
esc--进入命令模式，Shift+L

6）添加引号
选中引用文字，按’或”即可

7）复制/粘贴若干个cell
Ctrl+shift 选中，ctrl+c,ctrl+v


## 6.常见报错
1）jupyter notebook启动出错:
>Bad config encountered during initialization:/ No such notebook dir:

**解决方案：**
重新修改文件默认存储路径即可