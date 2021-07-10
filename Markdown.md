[TOC]
# 一级标题
## 二级标题
### 三级标题
生成标题采用如下代码：
```markdown
# 一级标题
## 二级标题
### 三级标题
```

# 语法
## 文章结构
### 目录
生成目录采用如下代码
```markdown
[TOC]
```
### 列表
* 无序列表
  * 嵌套无序列表
  * 嵌套无序列表
* 无序列表
* 无序列表
1. 有序列表 1
   1. 嵌套有序列表 1
   2. 嵌套有序列表 2
2. 有序列表 2
3. 有序列表 3
<br>
代码如下：
```markdown
* 无序列表
  * 嵌套无序列表
  * 嵌套无序列表
* 无序列表
* 无序列表
1. 有序列表 1
   1. 嵌套有序列表 1
   2. 嵌套有序列表 2
2. 有序列表 2
3. 有序列表 3
```
### 链接
插入链接：
[百度搜索]("www.baidu.com")

<br>

采用代码如下：

```markdown
[百度搜索]("www.baidu.com")
```

### 注释
<!-- 你看不见我 -->
```markdown
<!-- 你看不见我 -->
```
==快捷键 Ctrl + / 将当前行注释和反注释==
## 外观
### 字体
效果如下：
*斜体* 或者 _斜体_
**粗体**
***加粗斜体***
~~删除线~~

<br>

采用代码如下：
```markdown
*斜体* 或者 _斜体_
**粗体**
***加粗斜体***
~~删除线~~
```
### 引用
效果如下：
> 引用内容

<br>

采用代码如下：

```markdown
> 引用内容
```
### 代码环境
效果如下：
```python{.line-numbers}
    #!/usr/bin/python3
    print("Hello, World!");
```
<br>
采用代码如下：（其中“/”是多余的）

```markdown
/```python{.line-numbers}
    #!/usr/bin/python3
    print("Hello, World!");
/```
```

行内代码引用用一对`即可
## 图表
### 图片
[超链接名称](链接地址)

![图片提示语](图片地址)

==已应用插件：快捷键Ctrl+alt+V粘贴图片==
![示例](image/2021-07-09-21-59-23.png)
###表格

| 表头 | 表头 |
| ---- | ---- |
| 内容 | 内容 |
| 内容 | 内容 |

采用代码如下：
```markdown
[超链接名称](链接地址)

![图片提示语](图片地址)

| 表头 | 表头 |
| ---- | ---- |
| 内容 | 内容 |
| 内容 | 内容 |
```
## LaTeX
本文中VS CODE插件据来自于
[这篇文章]("https://orangex4.cool/post/notes-in-markdown/#%E5%9C%A8%E7%BA%BF%E6%B5%8F%E8%A7%88")
### 插入公式 
行内公式：
$\int ^1_0 f(x)dx$
行间公式：
$$
\begin{align}
&\int ^1_0 [f(x)+g(x)]dx \\
=&\int ^1_0 f(x)dx+\int ^1_0 g(x)dx\end{align}
$$
<br>采用代码如下：

```markdown
行内公式：
$\int ^1_0 f(x)dx$
行间公式：
$$
\begin{align}
&\int ^1_0 [f(x)+g(x)]dx \\
=&\int ^1_0 f(x)dx+\int ^1_0 g(x)dx\end{align}
$$
```

### 自动补全
#### 关于下标
$$
\begin{align*}
x^{-1}\\
\alpha_1,\alpha_2,\cdots,\alpha_n
\end{align*}
$$
```
\\-1 ⇒ ^{-1}
\\comma ⇒ \alpha_1,\alpha_2,\cdots,\alpha_n
```

#### 关于分式

选中文本时:
```
x+1 + \\frac ⇒ \frac{x+1}{}
```
在自动补全之后, 按下 Tab 键可以切换到下一个位置

对于根式有类似的补全:
$$
\sqrt[n]{x+1}
$$
```
x+1 + \\sqrt ⇒ \sqrt{x+1}
x+1 + \\sqrt ⇒ \sqrt[n]{x+1}
```
#### 关于巨算符
$$\lim_{n\to \infty}x_n$$
```
\\sum ⇒ \sum_{i=1}
\\prod ⇒ \prod_{i=1}
\\lim ⇒ \lim_{x\to \infty}
```

#### 括号
$$
\begin{aligned}
    \langle x,y\rangle\\
    \{x_1,x_2,\cdots,x_n\}\\
    \left( \alpha \right)
\end{aligned}
$$
```
\\angel ⇒ \langle \rangle
\\set ⇒ \{ \}
\\bracket ⇒ \left( \right)
\\square_bracket ⇒ \left[ \right]
\\curly_bracket ⇒ \left\{ \right}
```
#### 方程组
$$
\begin{cases}
    x_{11}+x_{12}+\cdots+x_{1n}=b_1\\
    x_{11}+x_{12}+\cdots+x_{1n}=b_2\\
    \quad \cdots\\
    x_{m1}+x_{m2}+\cdots+x_{mn}=b_m
\end{cases}
$$
```
$$
\begin{cases}
    x_{11}+x_{12}+\cdots+x_{1n}=b_1\\
    x_{11}+x_{12}+\cdots+x_{1n}=b_2\\
    \quad \cdots\\
    x_{m1}+x_{m2}+\cdots+x_{mn}=b_m
\end{cases}
$$
```
#### 矩阵
$$
\begin{pmatrix}x_1\\x_2\\\vdots\\x_n\end{pmatrix}
$$

$$
\begin{pmatrix}1&1&1\\1&1&1\\1&1&1\end{pmatrix}
$$
矩阵自动补全
```\\p22matrix ⇒ \begin{pmatrix}1&1\\1&1\end{pmatrix}
\\b22matrix ⇒ \begin{bmatrix}1&1\\1&1\end{bmatrix}
\\v22matrix ⇒ \begin{vmatrix}1&1\\1&1\end{vmatrix}
\\c3vector ⇒ \begin{pmatrix}1\\1\\1\end{pmatrix}
\\r3vector ⇒ \begin{pmatrix}1&1&1\end{pmatrix}
```

### 自定义快捷键
Ctrl+Shift+P搜索open snippet directory

已经copy文件markdown.hsnips

# 云端上传笔记
## git入门
git入门参考[这篇文章](https://www.liaoxuefeng.com/wiki/896043488029600/896202815778784)

### 初始化仓库
创建一个文件夹，鼠标右键git bash here

初始化仓库
```git
$ git init
```

添加文件
```git
$ git add <filename>
```

提交改动
```git
$ git commit -m <message>
```
![图示](image/2021-07-10-11-05-12.png)git add命令实际上就是把要提交的所有修改放到暂存区（Stage），然后，执行git commit就可以一次性把暂存区的所有修改提交到分支。
### 回溯历史版本
查看版本日志
```git
git log
```

版本更改
```git
git reset --hard commit_id
```

查看命令日志
```git
git reflog
```

### 撤销修改
丢弃工作区的修改：
```
git checkout -- file
```

如果工作区的修改已经被提交，先恢复暂存区
```git
git reset HEAD <file>
git checkout -- <file>
```

查看当前状态
``` git
git status
```

查看工作区和版本库里面最新版本的区别
```git
git diff HEAD -- readme.txt
```

### 删除文件
rm删除工作区文件
此后有两种选择：
1. 继续删除操作
   此时暂存区中文件还未被删除，git rm将删除暂存区中文件。再git commit则将删除操作更新到版本库
2. 撤销删除
   $ git checkout -- test.txt
   事实上git checkout是用版本库里的版本替换工作区的版本，即“一键还原工作区”

### github远程库
根据[这篇文章](https://www.liaoxuefeng.com/wiki/896043488029600/898732864121440)进行配置

要关联一个远程库，使用命令
```git
git remote add origin git@server-name:path/repo-name.git；
```

关联一个远程库时必须给远程库指定一个名字，origin是默认习惯命名；

关联后，第一次推送master分支的所有内容
```git
git push -u origin master
```



此后，每次本地提交后，只要有必要，就可以使用命令推送最新修改
```git
it push origin master
```


