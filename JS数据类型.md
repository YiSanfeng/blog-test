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
* 7种（大小写无所谓）
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