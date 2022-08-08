# JS数据类型
## 二进制
* 10转2
 <pre>x=y*2^5+y*2^4+y*2^3+y*2^2+y*2^1+y*2^0</pre>

* 2转10
1. 从右往左（最右边是第0位），第几位就乘2的几次方，然后加起来即可
2. 除0以外的任何数的0次方都得0
## 用十六进制表示二进制
1. 用8421从右往左对应xxxx
2. 8421代表2^3+2^2+2^1+2^0
3. 十六进制数字排序：0、2、3、4、5、6、7、8、9、a、b、c、d、e、f
4. 计算器程序员模式：HEX表示16进制，BIN表示2进制，OCT表示8进制，DEC表示10进制

## JS中的数据类型
* 7种（大小写无所谓）（前六种属于简单类型，后一种属于复杂类型）
1. 数字 number
2. 字符串 string
3. 布尔 bool
4. 符号 symbol
5. 空 undefined
6. 空 null
7. 对象 object、
8. 四基两空一对象
* 以下不是数据类型
1. 数组、函数、日期
2. 它们都属于object
## 转义
1. \'表示'
2. \"表示"
3. \n表示换行
4. \n表示回车
5. \t表示tab制表符
6. \ \表示\
7. \uFFFF表示对应的Unicode字符
8. \xFF表示前256个Unicode字符
## 通过下标读取字符（举例）
1. let s = 'hello'
2. s[0] // "h"
3. s[1] // "e"
4. s[4] // "0"
5. 字符的第一位的下标从0开始算
## base64 转码
1. 写法：<pre>window.atob('要转的内容')</pre>
## 五个falsy值（相当于false但又不是false的值）
1. 分别是undefined、null、0、NaN、''
## 类型转换
1. number转string（以n为例）
* String（n）
* n + ''（把n加上一个空的字符串，此法前端程序员常用方法）
2. string转number（以s为例）
* Number（s）
* s -0
* +s
* parselnt(s)/parseFloat(s)
3. x=>bool(以x为例)
* Boolean(x)
* !!x
4. x=>string
* String(x)
* x.toString()
## 对象object
1. 定义
* 是无序的数据集合
* 键值对的集合（键和值组成一对）
* 键名(也叫属性名)是字符串，不是标识符，可以包含任意字符
* 引号可以省略（非英文的特殊字符不建议省略），省略之后就只能写标识符
* 就算引号省略了，键名也还是字符串（重要）
* Object.keys(obj)可以得到所有的obj的所有key
2. 写法
* <pre>let obj={'name':'frank','age':'18'}</pre>
* <pre>let obj=new Object({'name':'frank'})
  console.log({'name':'frank','age':'18'})</pre>
## 变量做属性名
1. 如何用变量做属性名
* 之前都是用常量做属性名
* let p1='name'
* let obj={p1:'frank'}这样写，属性名为'p1'
* let obj={[p1]:'frank'}这样写，属性名为'name'
2. 对比
* 不加[]的属性名会自动编程字符串
* 加了[]则会当作变量求值
* 值如果不是字符串，则会自动变成字符串
# 对象的增删改查
## 
### 删除属性(delete用来删属性用)
1. delete obj.xxx或delete obj[ 'xxx' ] (同时删除属性名和属性值)
2. obj.xxx=undefined（没有删除属性名，只删除了属性值）
* 查看对象里是否存在某个属性名
3. 'xxx' in obj ===false（不存在）/true（存在）
* 'xxx' in obj && obj.xxx===undefined
4. 注意obj.xxx===undefined
* obj.xxx是否为obj的属性
### 查看属性
1. 查看自身所有属性
* 查看所有keys:Object keys(xxx)
* 查看所有values:Object values(xxx)
* 查看所有keys和values:Object entries(xxx)
2. 查看自身+共有属性
* console.dir(xxx)
3. 判断一个属性是自身的还是共有的
* obj.hasOwnProperty('toString')
4. 两种方法查看属性（新人推荐使用中括号法）
* 中括号语法：obj[ 'key' ]
* 点语法：obj.key
#### 补充点
1. <pre>obj.name等价于obj.['name']</pre>
2. <pre>obj.name不等价于obj.[name]</pre>
* 注释：<pre>[] 里的'name'是字符串，而[]里的name是变量，所以不相等</pre>
3. <pre>let name = 'frank'
   obj[name]等价于obj['frank']
   因为已经声明了变量name等于字符串'frank'</pre>
### 写属性
1. 批量赋值<pre>Object.assign(obj,{age:18,gender:'man'})</pre>
2. 修改或增加共有属性
1. 无法通过自身修改或增加来改变共有属性（如果进行此操作，只会在自身对象里修改或增加此属性）
### 修改隐藏属性
1. 不推荐使用__proto__(会降低性能)
2. 推荐使用Object.create
* <pre>let obj=Object.create(common)
  obj.name='frank'</pre>
* <pre>let obj2=Object.create(common)
  obj.name='jack'</pre>
* 注释：规范大概的意思是，要改就一开始就改，别后来再改

