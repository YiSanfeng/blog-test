# JS数组
## 创建一个数组
* 新建
1. let arr = [1,2,3]
2. let arr = new Array(1,2,3)
3. let arr = new Array(3)
* 转化
1. let arr = '1,2,3'.split(',')
2. let arr = '123'.split('')
3. Array.form('1,2,3')
4. 理解：转化的前提是要有（0123）这样的下标或有length属性
5. 在步骤3的转化过程中，如果下标和length的长度不一致，则采用length来转化数组
* 伪数组
1. let divList = document.querySelectorAll('div')
2. 伪数组的原型链中并没有数组的原型
3. 
* 合并两个数组，得到新数组
1. arr1.concat(arr2) //数组1连接数组2，合成一个新的数组，这个数组包含原来两个数组的内容 
* 截取一个数组的一部分
1. arr1.slice(1) //从第二个元素开始截取（第二个元素包含在内）
2. arr1.slice(0) //从第一个元素开始截取（第一个元素包含在内）
3. JS只提供浅拷贝