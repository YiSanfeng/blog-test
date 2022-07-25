# CSS布局
## 常用单词
* <pre>display 陈列</pre>
* <pre>top 顶部</pre>
* <pre>nav 导航</pre>
* <pre>container 容器</pre>
* <pre>itmes 项目</pre>
* <pre>center 中央</pre>
* <pre>left 左</pre>
* <pre>right 右</pre>
* <pre>row 行</pre>
* <pre>column 列</pre>
* <pre>reverse 反转</pre>
* <pre>wrap 折叠</pre>
* <pre>justify 整理版面</pre>
* <pre>space 以一定间隔排列</pre>
* <pre>between 在某某中间</pre>
* <pre>around 在某某周围</pre>
* <pre>stretch 一样高</pre>
* <pre>start 开始</pre>
* <pre>end 结束</pre>
* <pre></pre>
* <pre></pre>
* <pre></pre>
* <pre></pre>
## 一、float布局
1. HTML里的父元素中需要写上<pre>clearfix</pre>
2. CSS里的父元素中需要写上<pre>clearfix:after{content:"";display:block;clear:both;}
3. CSS里的子元素中需要写上<pre>float:left;或float:right;(将此元素改为float元素)
4. 如果图片下方有多余部分<pre>vertical-align:middle</pre>或<pre>vertical-align:top</pre>
## 二、flex布局
1. 将一个元素改变为flex容器<pre>display:flex;</pre>
2. 改变items的主轴流动方向<pre>flex-direction:row 从左往右</pre><pre>flex-direction:row-reverse 从右往左</pre><pre>flex-direction:colum 从上到下</pre><pre>flex-direction:colum-reverse 从下到上</pre>
3. 折行<pre>flex:wrap</pre>不折行<pre>flex:nowrap</pre>
4. 改变主轴对齐方式（横向）<pre>justify-content:center 居中对齐</pre><pre>justify-content:start 靠左对齐</pre><pre>justify-content:end 靠右对齐</pre><pre>justify-content:space-between 把空间放到中间</pre><pre>justify-content:space-around 把空间放到周围</pre>
5. 改变次轴对齐方式（竖向）<pre>align-items:flex-start 靠上对齐</pre><pre>align-items:flex-end 靠下对齐</pre><pre>align-items:flex-center 居中对齐</pre><pre>align-items:flex-stretch 一样高</pre>
6. 