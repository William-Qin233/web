# 集合的定义
一种无序且唯一的数据结构

ES6 中的集合方法： Set
# 常用操作
去重、判断某元素是否在集合中、求交集。
# Set用法
```javascript
// 去重
const arr = [1,2,3,2,1,]
const arr2 = [...new Set(arr)]

// 判断元素是否在集合中
const set = new Set(arr)
const has = set.has(1)

// 求交集，需要借助数组的filter方法
const set2 = new Set([2, 3])
const set3 = new Set([...set].filter(item => set2.has(item)))
```
# LeetCode：349，两个数组的交集
```javascript
// 求解两个数组的交集，输出的数组可以无序且唯一
// 先对nums1去重，然后遍历nums1，看nums2里面是否存在nums1里面的值
const func = (nums1, nums2) => {
    return [...new Set(nums1)].filter(item =>nums2.includes(item))
}
```
# 使用 Set 对象：new add delete has size
```javascript
let mySet = new Set()
将Set转换成Array：
const arr = [...mySet]
const arr2 = Array.form(mySet)

将Array转换成Set
const mySet2 = new Set([1, 2, 3, 3, 4])    //会自动去重
```
# 迭代set，多种迭代方法
```javascript
// for ... in... 方法
for ( let item of mySet) {
console.log(item)
}

for (let key of mySet.keys()) {
console.log(key)
}

for (let item of mySet.values()) {
console.log(key)
}

for (let key of mySet.entries()) {
console.log(key)
}
```
# 求2个集合的交集、差集
```javascript
const intersection = new Set([ ...mySet].filter( x => mySet2.has( x ) )

const intersection = new Set([ ...mySet].filter( x => !mySet2.has( x ) )
```
