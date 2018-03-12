#### configurable 
指定该属性是否可以背重新定义，如果为false则再次针对该属性调用Object.defineProperty的时候会报异常
```
let obj = {};
Object.defineProperty(obj,"name", {
    value:"test",
    configurable:false
})
//TypeError: Cannot redefine property: name
Object.defineProperty(obj,"name", {
    value:"testq",
})
console.log(obj.name);

```
