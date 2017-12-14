[TOC]
## 0.  目录{#index}
## App接口文档。
链接：[百度](http://www.baidu.com)  
图片：![蓝象资本](https://pic.36krcnd.com/avatar/201705/31084933/669lxktivz9axd6h.png)  
#### 项目更新  
tags:  
   - Markdown
   - 语言
   categories:
   - 技术

##### 斜体、粗体
* 斜体语法：在斜体的字两边加*或_,例如：我是斜体 _我是斜体_
* 粗体：**粗体**
* 斜体+粗体： ***斜体+粗体***
* 删除线 ~~*删除*~~

##### 超链接
* ###### 行链接  
[]里写链接文字，()里写链接地址, ()中的”“中可以为链接指定title属性，title属性可加可不加，例如：  
    1. ```欢迎来到[梵居闹市](http://blog.leanote.com/freewalk)``` ,  
    2. ```欢迎来到[梵居闹市](http://blog.leanote.com/freewalk "梵居闹市")```
* ###### 参考式  
1. 语法： 两部分  
* 文中：[链接文字][链接标记]
* 任意位置，一般文末： [链接标记]:链接地址 “链接标题”
* 如果链接文字本身可以做为链接标记，你也可以写成[链接文字][]
[链接文字]：链接地址的形式，见代码的最后一行。  
例如：
手机`App`主要用到的`App`有[知乎][1]，[开发者头条][开发者头条]以及在[Github][Github]维护的一个博客.[Google][]是全世界最好用的搜索引擎   
* [1]:http://www.zhihu.com
* [开发者头条]:https://toutiao.io/signin
* [Github]:https://github.com/
* []:http://www.baidu.com

* ###### 自动链接
* 语法：用<>前后闭合，例如：
<http://example.com/>

#### 锚点
* 语法：在你准备跳转到的指定标题后插入锚点`{#标记}`，然后在文档的其它地方写上连接到锚点的链接。例如：  
跳转至[目录](#index)

#### 列表
* **无序**  使用 *，+，- 表示无序列表
* **有序**  有序列表则使用数字接着一个英文句点。  

#### 定义型列表
* 语法：定义型列表由名词和解释组成。一行写上定义，紧跟一行写上解释。解释的写法:紧跟一个缩进(Tab)  
Markdown  
: 轻量级文本标记语言，可以转换成html，pdf等格式（左侧有一个可见的冒号和四个不可见的空格）
代码块 2  
:   这是代码块的定义（左侧有一个可见的冒号和四个不可见的空格）  
      代码块（左侧有八个不可见的空格）  

##### 包含引用的列表
* 如果要在列表项目内放进引用，那 > 就需要缩进  
*   阅读的方法:
    > 打开书本。  
    > 打开电灯。
##### 代码块  
    代码<Hello world !>  

#### 引用
* 1  
> 这是一个有两段文字的引用,  
> 无意义的占行文字1.  
>无意义的占行文字2.
>
> 无意义的占行文字3.  
>无意义的占行文字4.

* 2 引用的多层嵌套  
>>> 请问 Markdwon 怎么用？ - 小白  
>> 自己看教程！ - 愤青  
> 教程在哪？ - 小白  

* 引用其它要素
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
>
> 给出一些例子代码：
>
>     return shell_exec("echo $input | $markdown_script");  

#### LaTeX 公式
* $ 表示行内公式：  
质能守恒方程可以用一个很简洁的方程式 $E=mc^2$ 来表达。
* $$ 表示整行公式：  
$$\sum_{i=1}^n a_i=0$$
$$f(x_1,x_x,\ldots,x_n) = x_1^2 + x_2^2 + \cdots + x_n^2 $$
$$\sum^{j-1}_{k=0}{\widehat{\gamma}_{kj} z_k}$$

#### 流程图

flow
st=>start: Start:>https://www.zybuluo.com
io=>inputoutput: verification
op=>operation: Your Operation
cond=>condition: Yes or No?
sub=>subroutine: Your Subroutine
e=>end
st->io->op->cond
cond(yes)->e
cond(no)->sub->io

#### 表格
1. 不管是哪种方式，第一行为表头，第二行分隔表头和主体部分，第三行开始每一行为一个表格行。
2. 列于列之间用管道符|隔开。原生方式的表格每一行的两边也要有管道符。
3. 第二行还可以为不同的列指定对齐方向。默认为左对齐，在-右边加上:就右对齐。  

产品|价格
-|-:
Leanote 高级账号|60元/年
Leanote 超级账号|120元/年

#### 分隔符  
1. * * *
2. ***
3. *****
4. _ _ _
5. _ _ _ _ _ _ _ _ _

#### 代码  
* 行代码 "``"：        
C语言里的函数 `scanf()` 怎么使用？
* 缩进式多行代码   
      #include <stdio.h>
      int main(void)
      {
          printf("Hello world\n");
      }
* 用六个`包裹多行代码  
```
#include <stdio.h>
int main(void)
{
    printf("Hello world\n");
}
```
