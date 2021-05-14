

# HTML

## 1-HTML入门

### 1.1 HTML历史

```markdown
HTML的首个公开描述出现于一个名为HTML Tags 页面存档备份，存于互联网档案馆的文件中，由蒂姆·伯纳斯-李于1991年底提及。它描述18个元素，包括HTML初始的、相对简单的设计。它的最大特点就是支持超链接，点击链接就可以跳转到其他网页，从而构成了整个互联网。
2004年，网页超文本应用技术工作小组（WHATWG）开始开发HTML5，并在2008年与W3C共同交付，2014年10月28日完成标准化。
```

### 1.2 什么是HTML?

```markdown
# HTML是用来描述网页的一种语言
	
	HTML即超文本标记语言 -- Hyper Text Markup Language
	HTML不是编程语言，只是标记语言
	HTML使用标记标签来描述网页
	HTML文档包含HTML标签及文本内容
	HTML也叫web页面
```

## 2-HTML标签🔴

### 2.1基本模板

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
</head>
<body>

</body>
</html>
```

```markdown
# <!DOCTYPE html>
	声明文档类型的标签(html)，告诉浏览器如何解析网页

# html标签(双)
	网页的顶层容器，即标签树结构的顶层节点，也称为根元素（root element）
	其他元素都是它的子元素。
	一个网页只能有一个<html>标签。
	html标签用于显示网页所有内容
	给浏览器或搜索引擎传递信息
	lang属性，表示网页内容默认的语言。
	lang = "en " --- 代表该网页属于按一个国家或地区   en- US：英国  zh -CN：中国

# head标签(双)
	容器标签，用于放置网页的元信息，不可视化区域
	此内容不会出现在网页上，而是为网页渲染提供额外信息。
	
 1. meta标签(单) -- 设置网页的元数据，专门告诉浏览器或者搜索引擎关于网页的基本数据
  		name = ""   -- 表示元数据的名字
  		content = "" -- 表示元数据的值，核心搜索关键字，作为网页名字的补充
  		http-equiv="" -- 用来覆盖 HTTP 回应的头信息字段(与content属性一起使用)
  		charset="UTF-8" -- 字符集信息,网页文件的编码格式
  		字符集信息种类：
  			    -- gb2312:  gb国标拼音缩写
  			    -- gbk:  国家标准扩展
  			    -- gb18030
  			    -- utf-8:  全世界200多个国家和地区的语言文字
  			    
  			    
 2. link标签(单) -- 链接外部样式表(css)
 	   <link rel="stylesheet" href="css路径">
 	  
 3. title标签(双)
 	   用于指定网页的标题，会显示在浏览器窗口的标题栏。
 	   
# body标签(双)
    用于放置网页的主体内容
    是<html>的第二个子元素，紧跟在<head>后面。
```

### 2.2body中常见章节标签(H5)

```html
<body>
  <header>页眉</header>
  <main>
    <article>
      <h1>文章标题</h1>
      <p>文章内容</p>
    </article>
  </main>
  <footer>页尾</footer>
</body>
```

```markdown
# header标签(双)
	表示一篇文章或者一个区块的头部
	
# footer标签(双)
 	表示网页、文章或章节的尾部
 	
# main标签(双)
	表示页面的主体内容，一个页面只能有一个<main>标签
	<main>是顶层标签，不能放置在<header>、<footer>、<article>、<aside>、<nav>等标签之中。

# article标签(双)
	表示页面里面一段完整的内容
	
# aside标签(双)
	用来放置网页侧边栏或与网页、文章主要内容间接相关的部分
	
# section标签(双)
	表示一个含有主题的独立部分，通常用在文档里面表示一个章节
	
# nav标签(双)
	用于放置页面或文档的导航信息，往往放置在<header>里面
	
# h1~h6标签(双)
	表示文章的标题。
	按照标题的等级，一共分成六级。
	h1权重最高，在页面出现一次。
	字体大小依次减小。
```

### 2.3body中常用标签

```markdown
# div标签(双)
	一个通用标签，表示一个区块（division）
	
# p标签(双)
	一个块级元素，代表文章的一个段落（paragraph)
	
# span标签(双)
	一个通用目的的行内标签（即不会产生换行），不带有任何语义
	
# br标签(单)
	换行符，单独使用
	
# hr标签(单)
	水平线分割线,单独使用
	
# pre标签(双)
	一个块级元素，表示保留原来的格式（preformatted）
	浏览器会保留该标签内部原始的换行和空格。
	
# strong/b标签(双)
	以粗体显示内容,表示内容本身的重要性
	strong权重大于b
	
# em/i标签(双)
	以斜体显示它包含的内容,表示语气上的强调
	em权重大于i
	
# code标签(双)
	一个行内元素，表示标签内容是计算机代码，浏览器默认会以等宽字体显示
	
# a标签(双)
	用来定义超链接，使一张页面链接到另外一张页面
	属性：
		href -- 指示链接的目标地址，也用于锚点链接(id名)
		target = “_self” -- 默认当前窗口    _blank -- 新的窗口打开
	外观：
		未被访问的链接带有下划线--蓝色
		已访问的链接带有下划线--紫色
		
# img标签(单)
	img为图像标签，可以向网页中嵌入图像
	属性：
		src：用来引用图像文件的绝对路径或相对路径(URL)
			相对路径：当前位置开始寻找--范围小
			绝对路径：从根源出发--盘符出发，范围大
		alt: 规定在图像无法显示时的替代文本，解释说明
		title： 鼠标移动至图片上方显示相应文字信息
		width/height设置目的：用来占据位置，防止网页布局混乱
		
# 无序列表ul(双)
	ul标签里边只能是li标签，li标签里边可以放其他标签
	样式type：
		type = “disc” --黑心圆
		type = “circle” --空心圆
		type = “square” --方块
		
# 有序列表ol(双)
	ol标签里边只能是li标签,li标签里边可以放其他标签
	样式type：
		type = " " --- 默认是1, 还有A a i I
		
# 自定义列表dl(双)
	dt -- 列表的标题
	dd --列表标题的内容
```

## 3-行内元素  inline

```markdown
# 定义
	display:inline
    行内元素只占据它对应标签的边框所包含的空间，没有换行效果
    
# 常见行内元素
	<a>	  <b>  <span>   <img>	 <strong>	<sub>   <sup>  <buton>  <input>  <label>  <select>  <textarea>
	
# 特点
1. 多个元素可以横排显示
2. 不支持宽高和上下margin
3. 支持padding，上下padding只对自身有效，不影响其他元素
4. 行内标签不能包含块级标签(a标签除外)
5. a标签不能嵌套a标签
```

## 4-块级元素 block

```markdown
# 定义
	display:block
	块级元素占据其父元素的整个宽度，有换行效果

# 常见块级元素
	<div>  <ul>  <ol>  <li>  <dl>  <dt>  <dd>  <h1>~<h6>  <p>
	
# 特点
1. 块级标签独占一行
2. 支持宽高、padding、margin
3. 不给宽度时，默认是父亲的100%
4. 可以容纳其他块级标签和行内标签(p标签除外)
5. p标签不可以包裹块级标签
```

## 5-行内块元素(inline-block)

```markdown
# 定义
	display:inline-block
	
# 特点
1. 不支持margin：auto
2. 存在行内块间隙问题(元素之间有空隙)
		空隙是实际存在的大小，相当于字符，可以通过设置font-size：0，即可解决该问题
```

## 6-行内元素和块级元素的区别

```markdown
1. 格式上，默认情况行内元素不会换行开始，块级元素会另起一行

2. 内容上，默认情况行内元素只能包含文本和其他行内元素，而块级元素可以包含行内元素和其他块级元素

3. 属性上，在W3C盒模型属性上行内元素width、height设置无效，设置margin、padding上下不会对其他元素产生影响，左右会影响
```

## 7-元素的显示和隐藏

### display：none

- 设置display：none，让这个元素消失
- 消失不占据原本任何位置
- 连带子元素一起消失
- 元素显示：display：block

### visibility：hidden

- 元素消失，只是视觉消失，在页面中实际存在，对布局依然起作用
- 元素显示：visibility：visible

### opacity：0

- opacity值为0代表透明度为0
- 元素完全透明，视觉上消失，页面实际存在，依然对布局起作用
- 0-1之间代表透明度，值为1则元素完全显示

## 8-CSS选择器

```markdown
1. 标签选择器
	    通过标签书写样式，选择范围广
	    
2. id选择器 #
		具有唯一性
		
3. class选择器 .
		支持多个名字，每个名字间要有一个空格
		
4. 通配符选择器 *
		选中页面中所有标签
		
5. 组合选择器
	(1). 后代选择器 
		    选择器之间用空格隔开
		    
	(2). 子选择器 >
			选择属于父级里边的子元素，不能包括孙子
			
	(3). 兄弟选择器 ~
			除开自身以外的所有兄弟
			
	(4). 毗邻选择器 +
			选择自己紧挨着下一个邻居
			
	(5). 属性选择器
			选择器名[属性名 = "属性值"]{css样式}
			1.div[id] -- 选中div标签具有id属性的标签
            2.div[ class = "aaa" ] -- 选中div标签中具有class属性，并且属性值等于aaa的标签
            3.div[ class ~= "aaa"] -- 选中div标签中具有class属性，并且属性值含有aaa的标签
            4.div[ class ^="aaa"] -- 选中div标签中具有class属性，并且属性值以aaa开头的标签
            5.div[ class$="a"] -- 选中div标签中具有class属性，并且属性值以a结尾的标签
            6.div[ class *= "s"] -- 选中div标签中具有class属性，并且属性值里边包含s的标签 
		
    (6). 并集选择器 ,
    		使用逗号隔开
```

### 选择器权重问题

```markdown
# 单个选择器权重
	id选择器 > class选择器 > 标签选择器 > 通配符选择器
	
# 多个选择器权重
	1.首先以 id>class>标签
	2.其次看id数量
		(1)id数量越多，权重越大
		(2)id数一样，class数越多，权重越大
		(3)class数一样，表圈数越多，权重越大
		(4)权重一样，后来居上
```

## 9-css文本样式

### 9.1字体粗细

```markdown
1. 默认情况
		font-weight:normal
		
2. 加粗
		font-weight:bold
		font-weight：数字
```

### 9.2字体颜色

```markdown
1. 英文单词
		color:red
		
2. 十六进制
		color:#ffffff --> 缩写#fff
		
3. rgb三原色
		color:rgb(25,25,25)	 --红 绿 蓝
		
4. rgba三原色
		color:rgba(55,55,55,.4) --a为透明度0-1    
								  0：完全透明
								  1：完全显示
```

### 9.3字体大小

```markdown
1. 字体默认16px

2. 字体最小12px

3. 设置大小
		font-size:??px
```

### 9.4文本修饰

```markdown
1. 无状态
		text-decoration：none
		
2. 下划线
		text-decoration：underline
		
3. 中划线
		text-decoration：line-through
		
4. 上划线
		text-decoration：overline
```

### 9.5字体样式

- font-family：'黑体','微软雅黑'.....
- 可以有多个字体，浏览器从头开始执行，如果不执行当前字体则依次向后

自定义字体样式：

```markdown
 @font-face{
   font-family: 自定义字体名字；
   src: url(引入外部字体文件)
}
```

### 9.6文本不换行

```markdown
设置文本不换行，多余用...表示，三行代码解决！
1. white-space：nowrap
2. overflow：hidden
3. text-overflow：ellipsis
```

## 10-命名规则

1. **英文**状态下的**小写**
2. 必须由**字母、数字、连字符(-)**组成
3. **见名知意**
4. **不允许带有广告的单词**(advertising、ad、adv...)
5. 禁止出现**中文拼音和汉字**，禁止出现**单个字母和数字**
6. 禁止**驼峰**命名

## 11-标准盒模型

### 11.1content(内容)

```markdown
content = width + height
```

### 11.2padding(内边距)

```markdown
# 特点
1. 撑大盒子
2. padding区域颜色和内容区域颜色一致
3. 设置盒子边框和内容区域的距离

# 语法
1. 分样式
	    padding-top
	    padding-bottom
	    padding-left
	    padding-right
	    
2. 复合样式
		padding：x x x x
		一个值：上下左右
		两个值：上下  左右
		三个值：上  左右  下
		四个值：上 右 下 左
```

### 11.3border(边框)

```markdown
# 特点
1. 不给边框设置颜色，默认为内容字体颜色
2. 不给边框大小，默认大小为3px
3. 可以不给border颜色和大小，但必须给边框样式，否则无效

# 语法
1. 分样式 
		border-width：(边框线大小)
		border-style：(边框线样式)
					solid：实线
					dashed：虚线
					dotted：点线
					double：双实线
		border-color：(边框线颜色)

2. 复合样式
		border： 大小 样式 颜色；
	    单个边框复合样式：
	    			  border-top-width：上边框大小
	    			  border-left-style：左边框样式
	    			  border-right-color：右边框颜色
	    			  border-bottom-transparent:下边框透明，实际位置不存在
	    			  border-bottom-color-transparent：下边框颜色透明，实际位置还在
	    			  border-bottom：none：无边框
```

### 11.4margin(外边距)

```markdown
# 作用
	调整盒子和盒子之间的距离(可以有负值)
	
# 语法
1. 分样式
		margin-top
		margin-right
		margin-bottom
		margin-left
		
2. 复合样式
		margin：x x x x
			一个值：上下左右
            两个值：上下  左右
            三个值：上  左右  下
            四个值：上 右 下 左
            特殊：auto(自适应居中)
            
# 应用
1. 元素处于兄弟关系
		外边距重合问题：谁的外边距大就显示谁的外边距(塌陷)。
		解决：可以选择只给一个盒子设置margin
2. 元素处于嵌套关系
		外边距重合问题：谁的外边距大就显示谁的外边距(塌陷)。
		解决：给父亲添加padding、给父亲添加边框下、给父亲加overflow：hidden(FTB)
```

### 11.5怪异盒模型

- 怪异盒模型也称低版本IE盒子模型
- 宽高指的是：content + padding + border 
- 设置：box-sizing：border-box(可以让内容不撑大盒子)

## 12-行高(line-height)

- 行高：一行文字的最小高度

- 设置文字**行与行**之间的距离
- 行间距：两行文字之间的距离(也就是文字上边和下边的留白部分)
- 半行间距：1/2行间距
- **行高 =  字体大小 + 行间距**
- **行高 = 行高倍数字 * 字体大小**(倍数值与字体大小相乘必须为整数)
- 文字在盒子中垂直居中：line-height的高度设置为盒子高度

## 13-基线对齐

<img src =" D:\A-study\6x\基线对齐.jpg"></img>

- vartical-align：top; 文字顶部对齐(包括半行间距)
- vartical-align：text-top 文字顶部对齐
- vartical-align：baseline 默认对齐方式
- vartical-align：text-bottom 文字底部对齐
- vartical-align：bottom 文字底部对齐(包括半行间距)

作用范围：

- 行内元素(inline)
- 行内块元素(inline-block)
- **块级元素没有基线对齐问题！！！**

解决图片下方存在空隙问题？

- **设置基线对齐**(除开baseline值)
- 直接将图片设置成块级元素(display:block)

## 14-浮动

#### 本质

- 实现图文环绕效果

#### 定义

- 使元素脱离文档流，按照指定方向发生移动，遇到父级边界或者相邻浮动元素会停下来

#### 特点

- 不区分行、块、行内块元素，使用浮动直接让元素变为块级
- 支持宽高、margin、padding，但不支持margin：auto
- 不会有空隙问题(块级不存在基线对齐)

#### 影响

- 如果不给父级高度，子元素浮动会导致父级高度塌陷，塌陷导致页面布局乱
- 父元素宽度不够，子元素浮动导致浮动元素掉落，元素卡主

#### 解决

- 一般不建议给父级设置宽高，这样就定死了，不灵活

- 父级设置浮动也不建议，会导致父级的父级塌陷

- **清除浮动**

  - 语法：

      选择器 ::after{

       content: "";-----激活伪元素

       display: block;

       clear: both; ----清除左右浮动

    }

  - 双冒号是区分伪元素和伪类，伪类是单个冒号，伪元素是双冒号，也可单冒号

## 15-BFC格局

> BFC : block formatting context(块级格式化上下文)

- bfc格局相当于一个结界，可形成一个封闭空间
- 给一个元素设置bfc，则里边的元素不会影响外边元素
- bfc格局也可以用来清除浮动

#### 触发条件

- html
- **overflow：hidden！！**
- float：left / right
- display：inline-block / table-cell / table-caption
- position：absolute / fixed

## 16-背景样式🔴

> **background**,是W3C规定一个浏览器如何渲染元素的背景层，用户可以在背景层增加颜色、图片等效果

### 背景颜色

- background-color：

### 背景图片

- background-image：url( ' 图片路径 ' )

常用背景**图片格式**：

- .jpg 不支持动画，不支持透明，渐进显示，颜色丰富，有损
- .png 不支持动画，支持透明度，颜色更丰富，无损
- .gif 支持动画，256种颜色，2种透明度，渐进显示
- .webp 支持动画，高压缩率，高加载速率

### 背景平铺

- background-repeat：repeat；
  - repeat(重复)
  - no-repeat(不重复)
  - repeat-x(x轴平铺)
  - repeat-y(y轴平铺)

### 背景大小

- background-size：apx bpx；
  - 单位: px   %
  - 一个值：按比例缩放，也就是宽高相等
  - 两个值：第一个宽第二个高
  - 值为100%，则背景图填充整个盒子
  - 特殊值 cover：等比例缩放，填充覆盖整个盒子
  - 特殊值 contain：等比例缩放，直到有一条边碰到盒子边框就停止

### 背景起始位置

- background-origin：
  - 默认值：padding-box(从padding区域开始显示)
  - content-box(从内容区域开始显示，不计算padding部分)
  - border-box(从边框左上角区域开始显示)

### 背景定位

- background-position：
  - 单位：px  %
  - 值可以是负数
  - 一个值：只给一个值，另一个值默认**居中**
  - 两个值：分别代表x轴和y轴，起点位置在盒子左上角(边框算在内)
  - 关键词：top right bottom left center
    - top right -- 右上角
    - top left -- 左上角
    - right center -- 右居中
    - top -- 上居中
    - left -- 左居中
    - center -- 上下左右居中

### 背景裁剪

- background-clip：
  - padding-box -- 裁剪到padding部分，显示内边距、内容区部分图片
  - content-box -- 裁剪到内容区，只保留内容区部分图片
  - border-box -- 裁剪到边框区，显示内容区、内边距和边框部分图片

### 背景关联

- background-attachment：
  - 决定背景是 在视口中固定还是随包含它的区块滚动的
  - 值fixed -- 固定，不随内容滚动
  - 值scroll -- 随着内容一起滚动

### 背景复合样式

- background：颜色 图片 重复？定位/大小 关联
  - background：pink url("路径") no-repeat  50px 50px/100px 100px fixed;

### 多张背景图

```markdown
1. 分样式
background-images:url('路径'),url('路径');
background-repeat:no-repeat,repeat-x;
background-size: 50px 50px,100px 30px;
background-position:100px 50px,100px 100px;

2. 复合样式
background：
	url('路径') no-repeat 10px 20px/50px 50px;
	url('路径') repeat-x 30px 30px/100px 100px;
	url......
```

## 17-样式初始化

- 因为**浏览器兼容问题**，不同的浏览器对有些标签的默认值是不同的
- 如果没初始化css样式，可能会导致页面在不同浏览器上存在差异
- 初始化样式会对**SEO**有一定的影响，力求影响最小的情况下初始化
- 通配符初始化css样式，会将所有标签都初始化，加大网站的运行负荷，加载时间长
- 最好的选择是选择性逐个初始化标签

## 18-圆角和渐变色

### 圆角(border-radius)

- 单位： px  %
- 一个值：四个角相同
- 两个值：分别代表**左上角右下角**和**右上角左下角**
- 三个值：左上角、右上角左下角、右下角
- 四个值：一一对应
- 分样式：
  - border-top-left-radius：左上角
  - border-top-right-radius：右上角
  - border-bottom-left-radius：左下角
  - border-bottom-right-radius：右下角

### 渐变色

> 渐变色指两个及以上的颜色之间呈现一种平滑的过渡效果，该效果是矢量效果，不会随着页面的放大 而出现模糊。

- **渐变色是背景图片不是背景色！！！**
- 至少两种颜色

**线性渐变**

- background：linear-gradient(red,blue)
- 里边的值可以有多个，平均占据0%-100%，也就是说两个值就一人占一半

```css
div{
	width:100px;
    height:100px;
    background：linear-gradient(red,blue,green,pink);
}
```

- 也可以自定义占比 

```css
div{
	width:100px;
    height:100px;
    background：linear-gradient(red 10px,blue 50px);
}
从0-10px之间是红色，10px-50px是红到蓝的渐变，50-100px是蓝色
```

- 可以改变渐变方向
  - 默认是从上到下
  - to top：从下到上
  - to right：从左到右
  - to right bottom：到右下
  - 对角线：单位：deg，值增大顺时针，值减小逆时针

```css
//默认方向是从上到下
div{
	width:100px;
    height:100px;
    background：linear-gradient(to top,red 10px,blue 50px);//从下到上
    background：linear-gradient(45deg,red,blue);//左下到右上渐变(45度角)
} 
```

**重复线性渐变**

- repeating-linear-gradient

- 无线循环重复填充整个背景

```css
div{
	width:100px;
    height:100px;
    background：repeating-linear-gradient(red 0px,red 15px,blue 15px,blue 30px);
    //0-15红色，15-30蓝色...循环填充
}
```

**径向渐变**

- background：radial-gradient(red,blue)
- 默认由内向外散发(红到蓝)
- 设置散发形状/大小at位置

```css
div{
    width:200px;
    heigh:200px;
    border:1px solid blue;
    background-image:radial-gradient(ellipse 150px 50px at 100px 100px,red, black);
    //定义椭圆、大小为150px 50px、位置在div的100px处，由红色向黑色散发
}
```

- 关键词：
  - closest-side：指定半径的长度，圆心到最近的边渐变过程
  - farthest-side：指定半径的长度，圆心到最远的边渐变过程
  - closest-corner：指定半径的长度，圆心到最近的叫角渐变过程
  - farthest-corner：指定半径的长度，圆心到最远的叫角渐变过程

```css
div{
    width:200px;
    heigh:200px;
    border:1px solid blue;
    background-image:radial-gradient(closest-side at 50px 50px,red, black);
    background-image:radial-gradient(farthest-side at 50px 50px,red, black);
    background-image:radial-gradient(closest-corner at 50px 50px,red, black);
    background-image:radial-gradient(farthest-corner at 50px 50px,red, black);
}
```

**重复径向渐变**

- repeating-linear-gradient()

  ```css
  div{
  	width:100px;
      height:100px;
      background：repeating-radial-gradient(red 0px,red 15px,blue 15px,blue 30px);
      //0-15红色，15-30蓝色...循环填充
  }
  ```


**角向渐变**



## 19-position(定位)

### 19.1文档流？

- 浏览器在默认情况下规定一个**块元素**在父元素内排列规则：
  1. 从上到下排列
  2. 从左到右排列
  3. 一个块元素占一行

### 19.2理解定位

- 指定网页元素到页面的任何一个位置，通过定位**精确**的控制元素的位置

### 19.3相对定位

- 语法

  position：relative 

  relative -- 相对的

- 特点：

  1.参照相对没有定位前的自己
  2.**有层级**，后来居上-- 层级高
  3.**占据自己原来的位置**--在原来的文档流当中存在自己的位置
  4.**不会改变元素的特征**，行内还是行内，块级还是块级
  5.支持margin、padding、margin：auto
  6.**不脱离文档流**

### 19.4绝对定位

- 语法

  position：absolute

  absolute -- 绝对的

- 特点

  1.**脱离文档流**
  2.提升层级**不占原来的位置**，后来者居上
  3.不支持margin：auto，支持margin
  4.参照物：默认参照body，**绝对定位的元素位置相对于最近的已定位的祖先元素**
  5.行内元素支持宽高，块级元素内容撑开宽高**改变元素特性**
  6.一般配合相对定位使用--父相子绝

### 19.5固定定位

- 语法

  position：fixed

  fixed -- 固定的

- 特点

  1.参照物：**相对浏览器窗口定位**！
  2.**脱离文档流**，提升层级
  3.不支持margin：auto
  4.可以**改变元素特性**，行内->块级

### 19.6层级关系

1. z-index--可以调换两个层的上下位置关系
2. 值可为正也可为负，**值越大越在上面**，**默认为0**
3. **只能同级元素对比**
4. z-index **只对定位的元素有效**，其他元素均无效

## 20-高级选择器

### 1.状态类伪类选择器

- 伪类：一系列特殊的选择器
- 作用：用来选择不同的状态
- 语法：选择器:关键词{css样式}

1. `link`：修饰 没有被点击过 的超链接
2. `visitied`：修饰 点击过 的超链接
3. `active`：修饰鼠标点击 获取焦点时 的超链接
4. `hover`：鼠标悬停时的超链接

- 几种伪类选择器一起使用，一定要注意顺序书写：

  link -> visited -> hover -> active

### 2.结构类伪类选择器

- 语法：选择器:关键词{css样式}

1. `first-child`：选择父元素里边的第一个子元素

2. `last-child`：选择父元素里边的最后一个子元素

3. `nth-child(n/odd/even)`：选择父元素里边的第n个元素,**不指定标签类型**

   **n代表自然数，从1开始取值**

   **odd代表奇数列**

   **even代表偶数列**

   其中参数也可以是**表达式**：2n-1、3n+1....

4. `nth-last-child(n)`：选择父元素里边倒数的第n个元素

5. `nth-of-type(n)`：选择父元素内具有**指定类元素**的第n个元素

### 3.伪元素

- 定义：假的元素，表示某个元素的子元素，这个元素是逻辑上存在的，但是实际上不存在html文档时
- 在css2中伪元素用 `:` 表示
- 在css3中伪元素用`::`表示，目的在于区分伪类
- 伪元素使用`content`属性**激活**
- 伪元素是一个`inline`**行内元素**

#### 3.1`::before`

​	在当前元素内容**前面**插入一些内容

#### 3.2`::after`

​	在当前元素内容**后面**插入一些内容

```html
<style>
    div{
        width:200px;
        height:200px;
    }
    div::before{
        content:'你好';
    }
    div::after{
        content:'工程师';
    }
</style>
<body>
    <div>前端</div>
</body>
<!-- 添加伪类后就是：你好前端工程师 -->
```

#### 3.3`::first-line`

​	在某个元素的**第一行**文字使用css样式

#### 3.4`::first-letter`

​    某个元素的**首文字**或**首字母**使用css样式

```html
<style>
    div{
        width:100px;
        height:100px;
    }
    div::first-line{
        color:red;
    }
    div::first-letter{
        color:blue;
        font-size:30px
    }
</style>
<body>
    <!-- 第一行文字变红 -->
    <div>前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮</div>
</body>
```

3.5`::selection`

​	选中**当前的内容**出现css样式(个别样式不起作用)

```html
<style>
    div{
        width:100px;
        height:100px;
    }
    div::selection{
        color:red;
        background-color:blue;
    }
</style>
<div>前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮前端攻城狮</div>
```

#### text- transform：文本样式

#### uppercase -- 字母大写                                               

#### lowercase -- 字母小 写                                               

#### capitalize -- 首字母大写

#### user-select：none  -- 禁止用户选中页面文字 

#### text-shadow -- 文本阴影

- text-shadow: x y  颜色  (inset内阴影)

#### box-shadow -- 盒子阴影

- box-shadow: x  y  模糊度 颜色  (inset内阴影)



## 21-form(表单)

### 原理

- 表单页面--输入数据--提交数据--发送给服务器--服务器接收数据--处理数据--返回数据

### 简述

- `form`(表单),是一个双标签，存储表单的一个区域

- 表单属性

  - **`action`**：表单提交的地址(提交目的地)

  - **`method`**：表单数据提交方式

    **get**方式：不安全，数据会显示在url地址栏；数据量小

    **post**方式：安全性高，传输数据大

### 组件

#### 1.input

- input输入框，行内块元素
- input属性：

```markdown
# type属性
	判断输入信息的类别，此属性值必须写，不写默认是text文本信息
  1. text      普通文本类型
  2. password  密码框
  3. submit    提交功能
  4. button	   普通按钮
  5. reset     重置按钮
  6. radio     单选按钮
		设置radio并将name属性得值写成一致实现单选
  7. checkbox  多选按钮
		设置checked属性表示默认选中
  8. time      时间
  9. date      年月日
  10. week     周
  11. month    月份
  12. datetime-local  日期信息
  13. file     文件按钮
		设置multiple -- 可以选择多个文件，然后提示用户选中了几个文件
  14. email    电子邮件
  15. color    选择颜色
  
  
# name属性
	标明该input名称，可用于设置radio单选操作
	
# value
	给input输入框设置默认值
	
# placeholder属性
	文本提示信息，用来标注该input是干啥的
```

- **`lable`**标签

  与input组件搭配使用，通过属性for与input关联，for的属性值是input的id名，点击label标签就会触发input焦点

#### 2.select

- select下拉框，双标签
- 搭配标签：`option` -- 双标签(块级)

```html
<form action="">
    <select name="" id="">
        <option value="">1</option>
        <option value="">2</option>
        <option value="">3</option>
        <option value="">4</option>
    </select>
</form>
```

#### 3.fieldset

- fieldset组件用于创建相同的小部件组，和legend标签搭配使用
- legend标签时fieldset小部件组的标题，卸载fieldset标签里边

```html
<fieldset>
    <legend>海贼王</legend>
    <input type="checkbox">路飞
    <input type="checkbox">索隆
    <input type="checkbox">娜美
    <input type="checkbox">乔巴
    <input type="checkbox">山治
</fieldset>
```

#### 4.textarea

- textarea--多行文本框(文本域)
- textarea属性：

```shell
# cols属性
	设置文本域的宽度
	
# rows属性
	设置文本域的高度
```

- CSS样式

```css
textarea{
    resize:both;  /*默认值：宽高都可以拉大*/
    resize:none; /*不能改变文本域的大小*/
    resize:vertical;/*垂直方向能拉动，水平方向禁止拉动*/
    resize:horizontal;/*水平方向能拉动，垂直方向禁止拉动*/
}
```

## 22-table(表格)

### 属性

```markdown
# border 属性
	设置表格的边框线

# cellspacing = ''
	设置单元格之间的距离
	
# cellpadding = ''
	设置单元格边框和内容之间的距离(内边距)
	
# border-collapse: collapse(css样式)
	表示将单元格边框线合并
	
# colspan = ''
	行合并,值为合并的数量，合并后删除这一行多余的单元格

# rowspan = ''
	列合并，值为合并的数量，合并后删除这一列多余的单元格
```

### 标签

```markdown
# thead 表格头部
# tbody 表格内容
# tfoot 表格注脚
# tr 行标签，平分表格高度
# th 标题单元格，字体加粗并居中
# td 单元格(列)，平分表格宽度
# caption 表格标题，写在table标签里边
```

### 特点

1. 决定表格的宽度是`table`
2. 单元格默认平分`table`宽度
3. tr、td、th没有margin属性

## 23-iframe(内联框架)

- 将其他网页引入到框架中显示

```html
<iframe src="" frameborder="0"></iframe>
```

### 属性

```markdown
# src = ''
	需要引入的文档地址

# frameborder = '0'
	内联框架的边框，默认为0没有边框，值为1有边框

# scrolling = ''
	设置内联框架是否有滚动条，默认没有(no)
	no：没有
	yes：有滚动条
	auto：根据内容显示滚动条
```

将a标签链接的网页显示在iframe框架里边：

```shell
# 将a标签的target属性值设置为iframe框架的name属性值相同即可
```



## 24-transition(过渡)

**[贝塞尔曲线](https://cubic-bezier.com/#.17,.67,.83,.67)**

### 定义

- 用于将CSS样式在一定的时间区域范围内平滑过渡

### 样式

```markdown
# 分样式
  1. transition-property
  	  指定过渡的css属性(宽、高、颜色....)
  	  如果需要多个css同时过渡，可以使用关键词all或者直接不写
  	  
  2. transition-duration
  	  指定过渡所需要的时间
  	  
  3. transition-timing-function
  	  指定过渡函数的运动曲线：
  	  					ease：慢快慢(默认)
  	  					linear：匀速运动
  	  					ease-in：加速运动
  	  					ease-out：减速运动
  	  					ease-in-out：加速再减速
  	  					贝塞尔曲线：https://cubic-bezier.com/#.17,.67,.83,.67
  	  					
  4. transition-delay
  	  指定过渡开始出现的延迟时间
  	  
# 复合样式
	transition：过渡属性 过渡时间 运动曲线 过渡延迟时间
```

### 注意！

- display：none --> display:block 特殊属性不会发生过渡效果(不是数值类型)



## 25-animation(动画)

### 样式

```markdown
# 分样式
   1. animation-name
        动画名称
    
   2. animation-duration
   		动画时间
   
   3. animation-timing-function
   		指定动画运动曲线
   					ease：慢快慢(默认)
                    linear：匀速运动
                    ease-in：加速运动
                    ease-out：减速运动
                    ease-in-out：加速再减速
                    贝塞尔曲线：https://cubic-bezier.com/#.17,.67,.83,.67
                    
   4. animation-delay
   		指定动画开始延迟的时间
   		
   5. animation-iteration-count
   		指定动画播放的次数：1 2 3 4.... infinite（无限循环)
   		
   6. animation-direction
   		动画方向：
   				normal：默认值
   				reverse：反方向播放
   				alternate：先正后返(至少两次)
   				alternate-reverse：先返后正(至少两次)
   		
   7. animation-play-state
   		动画的暂停和运行
   		
   8. animation-fill-mode
   		决定动画的起始位置
   				none(默认值)：原始状态 -> 动画开始 -> 动画结束回到原始状态
   				forwards:原始状态 -> 动画开始 -> 动画结束位置(动画帧100%)
   				backwards：动画开始位置(动画帧0%) -> 动画开始 -> 原始状态
   				both：动画开始位置(动画帧0%) -> 动画开始 -> 动画结束位置(动画帧100%)
   				
# 复合样式
	animation：动画名 动画时间 动画曲线 延迟时间 动画次数 动画方向 
```

### @keyframes

- @keyframes两种写法

```css
@keyframes name {
    form{

    }
    to{

    }
}
@keyframes name {
    0%{

    }
    50%{

    }
    100%{

    }
}
```



## 26-transform(形变)

- 形变分为2d和3d变换，描述一种变化之后的结果 
- 单位：deg(角度)、rad(弧度)、grad(梯度)、turn(圈)
  - 弧度 = 角度*π/180
  - grad = 360度(一圈)

### 旋转

```markdown
# transform:rotate(角度)
	单位：deg、rad(弧度)  弧度 = 角度*π/180
	正值表示顺时针旋转
	负值表示逆时针旋转
# transform：rotateX(角度)
	围绕x轴旋转
# transform：rotateY(角度)
	围绕y轴旋转
```

### 位移

```markdown
# transform:translate(x,y)
	单位：px
	如果只有一个值默认在x轴位移

# transform:translateX()
	在X轴上位移
# transform:translateY()
	在y轴上位移
```

### 缩放

```markdown
# transform:scale(倍数)
	单位：数值类型，可以是小数
	1：本身大小
	0：看不见，元素消失
	0-1之间：缩小
	1以上：放大
```

### 倾斜

```markdown
# transform:skew(角度)
# transform:skewX(角度)
# transform:skewY(角度)
```

### 复合样式

```markdown
# transform:旋转 位移 缩放 倾斜 

# 注意！！
	复合样式放置的顺序不一样，产生的效果也就不一样
```

###  变换基点

```markdown
# transform-origin:
	值可以关键字：top、left、right、bottom、center
	也可以是百分比；
```

### 3D

- 创造一个3D空间
- 作用于父元素

```markdown
# transform-style：preserve-3d
	给父级开辟3D空间，造出一个z轴
# perspective：8000px
	改变z轴长度，增加(减小)景深
```



## 27-filter(滤镜)

- 在CSS3新增加的属性中有一个属性较为特殊，那就是filter属性
- 该属性一般来说是用于元素本身的装饰，使页面产生更多的显示特效

### 亮度

```markdown
# filter：brightness（倍数）
	当倍数值大于1的时候元素会变亮，小于1的时候元素会变暗
	该属性的作用为调整元素当前的亮度，一般来说可以适用于鼠标悬浮到某元素时的提醒作用
```

```html
.goal{
    width:100px;
    height:100px;
    background-color:orange;
    transition: 0.5s;
}
.goal:hover{
	filter: brightness(2.1);
}
<div class="goal"></div>
```

### 对比度

```markdown
# filter：contrast（百分比）
	所谓对比度，简单理解的话就是一个区域里面每个颜色都会变得格外显眼，黑的更黑，白的更白
	当元素只有一种颜色时，该属性看效果和变亮看上去差不多,设置图片能更好的观察效果
```

```html
.goal{
    width:100px;
    height:100px;
    background-image:url("3.png");
    transition: 0.5s;
}
.goal:hover{
	filter: contrast(200%);
}
<div class="goal"></div>
```

### 模糊

```markdown
# filter：blur（模糊半径）
	给图像设置高斯模糊。
	模糊半径的值设定高斯函数的标准差，或者是屏幕上以多少像素融在一起， 所以值越大越模糊；
```

```html
.goal{
    width:100px;
    height:100px;
    background-image:url("3.png");
    transition: 0.5s;
}
.goal:hover{
	filter: blur(10px);

}
<div class="goal"></div>
```

### 色调

```markdown
# filter：grayscale（） -灰色色阶
	将一个颜色复杂的区域改造成一个只有黑白二色的区域
	圆括号里面的值定义转换的比例,值为100%则完全转为灰度图像，值为0%图像无变化
	值在0%到100%之间，则是效果的线性乘子
	
# filter：sepia（） -褐色色阶
	将某个区域的颜色进行简化
	该属性会将一个颜色丰富的区域变成一种老黑白照片效果，让图片有一种轻微泛黄的样子
```

## 28-flex(弹性盒模型)

- 采用flex布局的元素就是一个`flex容器`
- 容器里边的子元素都会自动成为这个容器的成员(`flex项目`)
- 通过父元素flex容器来控制子元素的布局
- 向左向右排列时，flex项目不给高度，默认为flex容器的100%
- 向上向下排列时，flex项目不给宽度，默认为flex容器的100%
- 当设置了flex布局以后，子元素的`float/clear/vertical`属性失效

### `flex`容器样式

#### flex-direction：

- `row` -- 向右排列(默认) 
- `row-reverse` -- 向左排列            
- `column` -- 向下排列        
- `column-reverse` -- 向上排列

#### flex-wrap：

- 交叉轴换行方向
- `nowrap`-- 不换行                                               
- `wrap` --主轴向下换行或交叉轴向右                       
- `wrap-reverse` --主轴向上换行或交叉轴向左

#### flex-flow：

- 前两个复合属性

#### justify-content：

- 元素在主轴上的对齐方式  

  - `flex-start` -- 默认
  - `flex-end`  -- 主轴结尾对齐
  - `center` -- 居中对齐
  - `space-around` -- 每个元素两侧间隔相等

  ```markdown
  space-ground: 子元素和父元素之间的间距=(父元素的宽度-子元素宽度之和)/2 * 子元素个数
  ```

  - `space-between` --两端对齐，每个元素之间间隔相等

  ```markdown
  space-between:元素之间的间隔=(父元素的宽度-子元素的宽度之和)/(子元素个数-1)                  
  子元素之间的间距=(父元素的宽度-子元素宽度之和)/子元素个数
  ```

#### align-items：

- 元素在交叉轴上的对齐方式
  - `flex-start` -- 默认
  - `flex-end`  -- 主轴结尾对齐
  - `center` -- 居中对齐
  - `baseline` -- 基线对齐

#### align-content:

- 换行的元素对齐方式(一行一个整体)
- 只有一行flex项目不起作用
  - flex-start -- 默认 
  - flex-end  -- 主轴结尾对齐        
  - center -- 居中对齐          
  - space-around -- 每个行两侧间隔相等                                                       
  - space-between--两端对齐，每个行之间间隔相等

### flex项目样式

#### order：

- 定义某个项目的排列顺序

- 默认值为0
- 值越大越往后排，越小越靠前

#### flex-grow：

- 弹性因子增长，值为数值型默认为0

- 给某个项目设置，自己占据本行剩余空间(变大)
- 给每个项目设置，平均分配剩余空间

#### flex-shrink：

- 弹性收缩因子，值为number，默认1
- 值为0表示项目部收缩

#### flex-basis：

- 项目占据主轴空间
- 默认值为auto，自动占据空间
- 说白了就是给项目设置宽度

#### flex：

- `flex-grow`、`flex-shrink`、`flex-basis`三个属性的复合写法

#### align-self:

- 设置该属性可以让单个项目和其他项目有不一样的对齐方式
- `align-self：center`，单个项目在交叉轴上居中显示