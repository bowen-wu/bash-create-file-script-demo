# create-file-script-demo


## 使用说明

在 git bash 命令行中 输入 `sh demo.sh fileName` 即可创建一个 fileName 的文件夹，文件夹中有index.html css js 三个文件，index.html 的内容为：
```
<!DOCTYPE>
<title>Hello</title>
<h1>Hi</h1>
```
css 文件夹中有 style.css 文件，内容为：
```
h1{ color: red; }
```
js 文件夹中有 main.js 文件，内容为：
```
var string = "Hello World"
alert(string)
```
当然，这些内容都可以在 demo.sh 中更改。



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

