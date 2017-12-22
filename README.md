# bash-create-file-script-demo


##实现功能

1.`sh demo.js fileName01`可生成目录 fileName01,`sh demo.js fileName02`可生成目录 fileName02.

2.如果要生成的目录已经存在，则直接退出

3.生成的目录结构如下：
```
 ├── css
 │   └── style.css
 ├── index.html
 └── js
     └── main.js
```

4.index.html 的内容为
```
 <!DOCTYPE>
 <title>Hello</title>
 <h1>Hi</h1>
 ```
 
5.css/style.css 的内容为
```
 h1{color: red;}
 ```
 
6.js/main.js 的内容为
```
 var string = "Hello World"
 alert(string)
 ```
 
 7.当然，这些内容都可以在 demo.js 中更改。



## 使用说明

在 git bash 命令行中 输入 `sh demo.js fileName` 即可创建一个 fileName 的文件夹



## 创建过程（git bash命令行）

`touch demo.txt`

`start demo.txt`

```
if [ -d $1 ]; then
	exit 1
else
	mkdir $1
	cd $1
	mkdir css js
	echo '<!DOCTYPE>
<title>Hello</title>
<h1>Hi</h1>' > index.html
	echo 'h1{ color: red; }' > css/style.css
	echo 'var string = "Hello World"
alert(string)' > js/main.js
	echo 'success'
	exit 0
fi
```
`rm demo.txt demo.sh`

