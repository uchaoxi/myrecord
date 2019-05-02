<h1>关于Set和Map</h1>
<h2>Set</h2>
<h3>成员的值唯一，没有重复的值</h3>
<h3>构造</h3>
let set1 = new Set();
let set2 = new Set([1,2,3,4]);
<h3>属性</h3>
Set.prototype.constrctor:构造函数，默认就是Set函数
Set.prototype.size：返回Set实例的成员总数
<h3>方法</h3>
add(value)
delete(value)
has(value)
clear()
<h3>遍历方法</h3>
keys()
values()//keys和values方法返回完全一致
entries() 
forEach()
for ... of 
使用rest运算符，变成数组遍历
在遍历操作中，改变原来set的结构
Array.from(set,val=>val*2)
new Set([...set].map(val=>val*2))
<h2>WeakSet</h2>
<h3>成员只能是对象，而不能是其他类型的值</h3>
<h3>WeakSet 中的对象都是弱引用，即垃圾回收机制不考虑 WeakSet 对该对象的引用，也就是说，如果其他对象都不再引用该对象，那么垃圾回收机制会自动回收该对象所占用的内存，不考虑该对象还存在于 WeakSet之中。</h3>
<h3>ES6 规定 WeakSet 不可遍历.WeakSet也没有size属性</h3>
<h3>构造</h3>
const a = [[1,2],[3,4]];
const ws = new WeakSet(a);
//WeakSet {[1,2],[3,4]}
<h3>方法</h3>
add(value)
delete(value)
has(value)
<h2>Map</h2>
<h3>键值对集合，但是键的类型不局限于字符串，各种类型的值，包括对象都可以当做键</h3>
<h3>构造</h3>
new Map()
new Map([['name','zhangsan'],['title','author']]);
<p>事实上，不仅仅是数组，任何具有 Iterator 接口、且每个成员都是一个双元素的数组的数据结构（详见《Iterator》一章）都可以当作Map构造函数的参数。这就是说，Set和Map都可以用来生成新的 Map。</p>
<h3>属性方法</h3>
size
set(key,value)
get(key)
has(key)
delete(key),返回true删除失败返回false
clear()清除所有成员，没有返回值
<h3>遍历方法-Map的遍历顺序是插入顺序</h3>
keys()
values()
entries()
forEach()
rest运算符，转成数组遍历
<h2>WeakMap</h2>
<h3>弱引用，无法遍历，没有size属性，无法清空</h3>
<h3>构建</h3>
new WeakMap()
<h3>方法</h3>
get()
set()
has()
delete()
<h3>作用</h3>
DOM节点作为键名
私有变量
