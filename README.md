
## 题目分布：
单选 6\*2，多选 3\*2，判断 3\*2，简答 2\*2，技术题 1\*2
主要内容包括：
ES2015等js新特性  
React（16.0版本）实际使用  
Redux基础知识了解  
Docker的基础使用

### 单选
#### JS(ES2015) * 4
1、
```js
console.log(a);let a = 1;
```
输出结果为：
A：1  B：0  C：undefined  D：异常：a is not defined

答案：D

2、
```js
console.log(b);const b = 1;
```
输出结果为：
A：1  B：0  C：undefined  D：异常：b is not defined

答案：D

3、
```js
{
  var a = [];
  for (var i = 0; i < 10; i++) {
    a[i] = function () {
      console.log(i);
    };
  }
  a[6]();
}
```
输出结果为：
A: 0；B：6；C：10；D：undefined

答案：C

4、
```js
{
  var a = [];
  for (let i = 0; i < 10; i++) {
    a[i] = function () {
      console.log(i);
    };
  }
  a[6]();
}
```
输出结果为：
A: 0；B：6；C：10；D：undefined

答案：B

#### React * 4
1、  
调用setState时，当前组件会触发下列哪个周期函数：  
A: componentWillMount  
B：componentDidMount  
C：shouldComponentUpdate  
D：componentWillReceiveProps

答案：C

2、  
React性能优化是下列哪个周期函数：  
A: componentWillMount  
B：componentDidMount  
C：shouldComponentUpdate  
D：componentDidUpdate

答案：C

3、  
当父组件由于setState导致render函数被调用时，首先会触发子组件的哪个周期函数：  
A: componentWillMount  
B：componentDidMount  
C：shouldComponentUpdate  
D：componentWillReceiveProps

答案：D

4、
在React中，下列哪个周期函数内不适合调用setState：  
A: componentWillMount  
B：componentDidMount  
C：componentWillUpdate  
D：componentWillReceiveProps

答案：C

#### Docker * 4
1、
在创建Docker镜像时，下列哪项指令是错误的：  
A：docker build -t testname .  
B：docker build -t testname:1 .  
C：docker build -t testName:2.1 .  
D：docker build -t test_name:3.0.1 .  

答案：D

2、
使用Docker时，下面哪项指令可以用来删除未运行的hi:0.0.1镜像：  
A：docker rmi hi:0.0.1  
B：docker rm hi:0.0.1  
C：docker stop hi:0.0.1  
D：docker delete hi:0.0.1  

答案：A

3、
使用Docker时，下面哪项指令可以用来删除未运行的7d2b64c6277c容器：  
A：docker rmi 7d2b64c6277c  
B：docker rm 7d2b64c6277c  
C：docker stop 7d2b64c6277c  
D：docker delete 7d2b64c6277c  

答案：B

4、
在编写Dockerfile时，下列哪项指令可以将`jdk.tar.gz`添加到镜像的`/usr/local/`目录下并完成解压：  
A：ADD jdk.tar.gz /usr/local/  
B：COPY jdk.tar.gz /usr/local/  
C：TAR jdk.tar.gz /usr/local/  
D：ENV jdk.tar.gz /usr/local/  

答案：A

### 多选
#### JS(ES2015) * 2
1、
在ES2015标准中，下面哪几项可以声明变量a并初始化值为1：  
A：var a = 1  B：let a = 1  C：const a = 1  D：a = 1

答案：ABCD

2、
arr = [0, 1, 2, 3]，下面哪几项的修改会改变arr的值：  
A：tmp = arr; tmp.push(4);  
B：tmp = arr.slice(); tmp.push(4);  
C：tmp = arr.reverse(); tmp.push(4);  
D：tmp = [...arr]; tmp.push(4);  

答案：AC

#### React(16.0) * 2
1、
React中构建组件的方式可以为：  
A：React.createClass  
B：extends React.Component  
C：无状态函数  
D：new React  

答案：ABC

2、
React中，以下哪几项为PropTypes可以声明的类型：  
A：string  
B：number  
C：object  
D：array  

答案：ABCD

#### Docker * 2
1、
在编写Dockerfile时，下列哪项指令可以将`hello.sh`添加到镜像的`/usr/local/bin/`目录下  
A：ADD hello.sh /usr/local/bin/  
B：COPY hello.sh /usr/local/bin/  
C：MV hello.sh /usr/local/bin/  
D：ENV hello.sh /usr/local/bin/

答案：AB

2、
下面哪几项是Docker命令：  
A：build  
B：images  
C：exec  
D：delete  

答案：ABC

### 判断
#### JS(ES2015) * 3
1、
```js
const A = [];
A.push("a");
console.log(A[0]);
```
输出结果为：a

答案：正确

2、
```js
const A = 'a';
A = 'b';
console.log(A);
```
输出结果为：b

答案：错误

3、
在js中，对对象的属性进行遍历时，尽量使用`Object.keys()`来代替`for...in`循环

答案：正确

#### React * 3
1、
在componentWillReceiveProps周期函数中可以获取到父组件传进来的最新参数值  

答案：正确

2、
在React组件中，可以通过ref属性来获取到真实DOM节点

答案：正确

3、
React组件中，setState不会立即生效，要经过render过程才能真正改变state值

答案：正确

### 简答 * 4
#### React 16.0 在调用setState后，会触发以下哪几个周期函数：
```
componentWillMount
render
componentDidMount
componentWillReceiveProps
shouldComponentUpdate
componentWillUpdate
componentDidUpdate
componentWillUnmount
```
答：shouldComponentUpdate、componentWillUpdate、render、componentDidUpdate
#### React 中keys的作用是什么
答：Keys 是 React 用于追踪哪些列表中元素被修改、被添加或者被移除的辅助标识。
在开发过程中，我们需要保证某个元素的 key 在其同级元素中具有唯一性。在 React Diff 算法中 React 会借助元素的 Key 值来判断该元素是新近创建的还是被移动而来的元素，从而减少不必要的元素重渲染。此外，React 还需要借助 Key 值来判断元素与本地状态的关联关系，因此我们绝不可忽视转换函数中 Key 的重要性。
#### JS(ES2015)下面代码输出结果是什么，请说明原因
```js
{
  var a = [];
  for (var i = 0; i < 10; i++) {
    a[i] = function () {
      console.log(i);
    };
  }
  a[6]();
}
```
答：上面代码中，变量i是var命令声明的，在全局范围内都有效，所以全局只有一个变量i。每一次循环，变量i的值都会发生改变，而循环内被赋给数组a的函数内部的console.log(i)，里面的i指向的就是全局的i。也就是说，所有数组a的成员里面的i，指向的都是同一个i，导致运行时输出的是最后一轮的i的值，也就是 10。
#### 在什么情况下你会优先选择使用 Class Component 而不是 Functional Component
答：在组件需要包含内部状态或者使用到生命周期函数的时候使用 Class Component ，否则使用函数式组件。

### 技术题 * 2
#### 举例比较分析一下分别使用React与jQuery的实现相同功能点的思路区别：

答：以实现“界面点击按钮后显示当前点击次数”的功能为例：  
React：  
1、创建state来存储当前点击次数  
2、在按钮组件上增加onClick事件，在点击时setState将state中的点击次数加一  
3、setState会自动调用render周期函数进行界面刷新展示最新点击次数

jQuery：  
1、在按钮组件上新增监听事件  
2、在监听到点击事件后，获取当前显示次数的DOM元素值，将该值加一  
3、修改DOM元素的值为当前值

#### 请分析Redux的主要使用场景

答：Redux主要用于多交互、多数据源的场景中，主要包括：  
从使用场景来看：  
用户的使用方式复杂  
不同身份的用户有不同的使用方式  
多个用户之间可以协作  
与服务器大量交互，或者使用了WebSocket  
View要从多个来源获取数据  

从组建角度来看：  
某个组件的状态，需要共享  
某个状态需要在任何地方都可以拿到  
一个组件需要改变全局状态  
一个组件需要改变另一个组件的状态  

## 复习提纲与重点
### JS部分
1、JS中var、let、const修饰变量的区别  
2、ES2015中箭头函数、扩展运算符等知识  
3、ES2015新增功能  

### React+Redux部分
1、React组件的数据、父子组件传值  
2、React组件的生命周期  
3、Redux使用场景  

### Docker部分
1、docker相关指令的使用  
2、docker在实际场景中的使用
