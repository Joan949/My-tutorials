## 1.在Pycharm中内嵌jupter

1）新建并激活环境
```
conda create -n py3.6  python=3.6
conda activate py3.6
```
2）安装ipykernel库
```
pip install ipykernel
```
3）创建jupyter内核
```
Python -m ipykernel install --name py3.6_jupyter

#查看所有jupyter内核
jupyter kernelspec list

#删除不需要的内核
jupyter kernelspec remove py_jupyter
```