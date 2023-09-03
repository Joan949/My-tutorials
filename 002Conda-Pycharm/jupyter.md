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
2）命令模式--灰色--esc键 
3）markdown模式:esc+m
4）code模式:esc+y


## 3.常用快捷键
1）命令模式下
```
Enter: 进入编辑模式
Y: 把代码块变成代码
M: 把代码块变成标签

A: 在上面插入代码块
B: 在下面插入代码块
D,D: 删除选中单元 按两下

X: 剪切选择的代码块
C: 复制选择的代码块

Shift-V: 粘贴到上面
V: 粘贴到下面
Z: 撤销删除

空格: 向下滚动
Shift-空格: 向上滚动

上: 选择上面的代码块
下: 选择下面的代码块

Shift-L: 在所有单元格中切换行号，并保持设置

Shift-Enter: 运行代码块, 选择下面的代码块
Ctrl-Enter: 运行选中的代码块
Alt-Enter: 运行代码块并且插入下面
```

2）编辑模式下
```
Esc: 进入命令行模式

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
## 4.常见报错
1）jupyter notebook启动出错:
>Bad config encountered during initialization:/ No such notebook dir:

**解决方案：**
重新修改文件默认存储路径即可