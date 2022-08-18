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
## 删元素
* 跟对象是一样的操作（此法不推荐）
1. let arr =['a','b','c']//设置一个数组，有abc三个元素
2. delete arr['0']//删除第一个（0是第一个）
3. arr //[empty,'b','c']
4. 数组的长度不会改变，这种叫做稀疏数组
* length可以直接设置要保留的元素（此法不推荐）
1. let arr = [1,2,3,4,5]
2. arr.length=1 //(只保留1个长度)
* shift法删除头部元素\
1. let arr = [1,2,3,4]
2. arr.shift() //（）里不用写东西，此法会删掉arr里的第一个元素，并返回被删除的元素
* pop法删除尾部元素
1. let arr = [1,2,3,4]
2. arr.pop() //（）里不用写东西，此法会删掉arr里的最后一个元素，并返回被删除的元素
* 删除中间的元素
1. let arr = [1,2,3,4]
2. arr.splice(2,3)//（）内第一个数表示从第几个下标开始删，第二个数字是删除几个元素。本句表示从第二个下标（含第二个）（下标就是元素的序号），删除3个元素
3. 或者arr.splice(2,1,666)//（从第二个下标（含），删除一个，改为新元素）
4. arr.splice(2,1,666,777,888)添加新元素进当前数组
# 查看所有元素
* 查看所有属性名
1. let arr = [1,2,3,4,5];arr.x='xxx'
2. Object.keys(arr)
3. for(let i in arr){console.log(i)}
* 查看数字（字符串）属性名和值
1. for(let i = 0,i < arr.length;i++){
    console.log(`${1} : ${[1]}`)
}
2. 自己要控制i 从0增长到length-1
   <pre>arr.forEach(function(xxx,yyy，zzz){
    console.log(`${xxx} : ${yyy}`)
   })
   //xxx表示数组的元素，yyy表示下标，zzz是数组本身（可加可不加）</pre>
* 查看单个属性
# 查看单个属性
* 跟查看对象一样
1. let arr = [111,222,333]
2. arr[0]
* 索引越界
1. arr[arr.length]===undefined
2. arr[-1] === undefined
* 举例
<pre>for(let i = 0;i <= arr.length;i++){
    console.log(arr[i].toString())
}</pre>
1. 报错：Canont read property 'toString' of undefined//意思是读取了 undefined的toString属性
* 查看某个元素是否在数组里
1. arr.indexOf(item)//（）里写你要查找的元素，存在就返回查找的元素的下标，否则就返回-1
2. 使用条件查找元素
   <pre>arr.find(function(x){
    return x%2===0)
    }）
    //返回第一个x除以2的余数为0的元素</pre>
3. 使用条件查找元素的索引
1. arr.findIndex(x%2===0)//找到第一个偶数的索引下标
## 增加数组中的元素
* 在尾部增加元素
1. arr.push(newItem)//修改arr，返回新的长度
2. arr.push(newItem1,newItem2)//修改arr，返回新长度
* 在头部增加元素
1. arr.unshift(newItem)//修改arr，返回新长度
2. arr.unshift(newItem1,newItem2)//修改arr，返回新长度
* 在中间添加元素
1. arr.splice(3,0,x)//在第三个下标删除0个元素，添加x
2. arr.splice(3,0,x,y)//在第三个下标删除0个元素，添加x和y
## 修改数组中的元素 
* 反转顺序
1. arr.reverse() //颠倒原数组的排序
* 自定义顺序
1. arr.sort((a,b)=> a-b)
## 数组变换
* map
1. n变n
2. 不会改变原数组
* filter
1. n变少
2. 不会改变原数组
* reduce
1. n变1
2. <pre></pre>
