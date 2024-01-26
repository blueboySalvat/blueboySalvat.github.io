# 基本知识
 - 如果值为若干单词，则要给值加引号
 - 多个声明之间使用分号`;`分开
 - CSS对大小不敏感，如果涉及到与html文档一起使用时，class与id名称对大小写敏感
```css
/* 这是注释 */
选择器 {
      样式名称1: 样式值1;
      样式名称2: 样式值2;
}
```
# 行内样式
>
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>innerline_css</title>
	</head>

	
	<body>
		<p style = "color:red;">hello world</p>
		<p style = "color:green">hello css</p>
	</body>
</html>
```

# 内部样式
>无法对多个文件同时进行自定义设置
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>inner_css</title>
		<style>
			.c1 {
				color:red;
				border:1px solid black;
				text-align:center;
			}
			.c2 {
				color:blue;
				border:1px solid black;
				text-align:center;

			}
		</style>
	</head>

	
	<body>
		<p class = "c1">hello world</p>
		<p class = "c2">hello css</p>
	</body>
</html>
```

# 外部样式
>可以对多个文件同时进行自定义样式设置

```css
.c1 {
	color:red;
	border:1px solid black;
	text-align:center;
}
.c2 {
	color:blue;
	border:1px solid black;
	text-align:center;

}
```
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>css_link</title>
		<link href = "./css/css.css" rel = "stylesheet" type = "text/css" >
	</head>

	
	<body>
		<p class = "c1">hello world</p>
		<p class = "c2">hello css</p>
	</body>
</html>
```
# 优先级 : 
如外部 CSS/内部 CSS/行内 CSS 引入时存在先后顺序，从上往下阅读，后出现的会覆盖前面的样式。（在有相同属性时会覆盖其值）
行内样式的优先级最高。（无论什么顺序，这都是离着标签最近的。）
浏览器自带的样式优先级最低。

# CSS 选择器
## 元素选择器
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>css_link</title>
		<style>
			p {
				text-align:center;
				color:red;			
				}
		</style>
	</head>
	
	<body>
		<p>hello world</p>
		<p>hello css</p>
	</body>
</html>
```

## ID 选择器
> 一个页面内的每个 ID 是唯一的
```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>css_link</title>
		<style>
			#id1 {
				text-align:center;
				color:red;			
			}
			#id2 {
				text-align:right;
				color:green;			
			}
		</style>
	</head>
	
	<body>
		<p id = "id1">hello ID_CHOICE</p>
		<p id = "id2">hello ID_CHHHHH</p>
	</body>
</html>
```

## 类选择器
>Class 的属性可以有多个，样式之间叠加，使用空格分隔。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>class_choice</title>
		<style>
			.c1 {
				text-align:center;		
			}
			.c2 {
				color:green;			
			}
			.c3 {
				background-color:pink;			
			}

		</style>
	</head>
	
	<body>
		<p class = "c1">hello CLASS_CHOICE</p>
		<p class = "c2">hello CLASS_CHHHHH</p>
		<p class = "c3">hello CLASS_CCCCCC</p>
		<p class = "c1 c2 c3">hello CLASS_SSSSSS</p>
	</body>
</html>
```
## 分组选择器
>对不同选择器放在同一组，统一设置样式。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>class_choice</title>
		<style>
			.c1 {
				text-align:center;		
			}
			.c2 {
				color:green;			
			}
			.c3 {
				background-color:pink;			
			}
			#id1 {
				text-align:center;
				color:red;			
			}
			#id2 {
				text-align:right;
				color:green;			
			}
			#id3 {
				text-align:lefg;
				color:green;			
			}
			p {
				text-align:center;
				color:red;			
			}
			/* 分组选择器 */
			c1,c2,id1,id2,p {
				text-decoration:underline;
			}


		</style>
	</head>
	
	<body>
		<p>hello element_choice</p>
		<p>hello css</p>

		<p id = "id1">hello ID_CHOICE</p>
		<p id = "id2">hello ID_CHHHHH</p>
		<h3 id = "id3">hello ID_CHHHHH</h3>

		<p class = "c1">hello CLASS_CHOICE</p>
		<p class = "c2">hello CLASS_CHHHHH</p>
		<h3 class = "c3">hello CLASS_CCCCCC</h3>
	</body>
</html>
```

## 通用选择器
>一般用于全局的统一样式设置（清除浏览器自带的默认样式）

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>class_choice</title>
		<style>
			.c1 {
				text-align:center;		
			}
			.c2 {
				color:green;			
			}
			.c3 {
				background-color:pink;
			}
			/*用于清除浏览器的默认样式*/
			* {
				margin:0px;
				padding:0px;
			}
		</style>
	</head>
	
	<body>
		<p class = "c1">hello UNIVERSAL</p>
		<p class = "c2">hello UNNNNNNNN</p>
		<h3 class = "c3">hello UNIIIIII</h3>
	</body>
</html>
```
## 组合选择器
### 后代选择器
>div p 选择父元素 div 之后的所有 p 元素

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>class_choice</title>
		<style>
			.c1 {
				text-align:center;		
			}
			.c2 {
				color:green;			
			}
			.c3 {
				background-color:pink;
			}
			/*后代选择器。选中了div标签后的所有p标签*/
			div p {
				background-color:red;
			}
		</style>
	</head>
	
	<body>
		<div>
			<p class = "c1">hello UNIVERSAL</p>
			<p class = "c2">hello UNNNNNNNN</p>
			<h3 class = "c3">hello UNIIIIII</h3>
			<div>
				<p>i am here!</p>
			</div>
		</div>

	</body>
</html>
```
### 子代选择器
>div >p 选择父元素是 p 的所有的元素。
只有第一级的才会被选择，第二级的不会被选择。

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset = "utf-8">
		<title>son_selector</title>
		<style>
			.c1 {
				text-align:center;		
			}
			.c2 {
				color:green;			
			}
			.c3 {
				background-color:pink;
			}
			/*子代选择器。选中了div标签后的儿子p标签*/
			div>p {
				background-color:green;
			}
		</style>
	</head>
	
	<body>
		<div>
			<p class = "c1">hello UNIVERSAL</p>
			<p class = "c2">hello UNNNNNNNN</p>
			<h3 class = "c3">hello UNIIIIII</h3>
			<div>
				<ul>
					<li><p>i am here!</p></li>
				</ul>
			</div>
		</div>

	</body>
</html>
```