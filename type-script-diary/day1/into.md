# 什么是 TypeScript
>Typed JavaScript at Any Scale.
添加了类型系统的 JavaScript，适用于任何规模的项目。

## 特性 类型系统、适用于任何规模
### 类型系统
#### TypeScript 是静态类型
>静态类型是指编译阶段就能确定每个变量的类型，这种语言的类型错误往往会导致语法错误

得益于 TypeScript 强大的[类型推论][]，即使不去手动声明变量 foo 的类型，也能在变量初始化时自动推论出它是一个 number 类型。
```ts
let foo: number = 1;
foo.split(' ');
// Property 'split' does not exist on type 'number'.
// 编译时会报错（数字没有 split 方法），无法通过编译
```
#### TypeScript 是弱类型
类型系统按照「是否允许隐式类型转换」来分类，可以分为强类型和弱类型
```
console.log(1 + '1');
// 打印出字符串 '11'
```
TypeScript 是完全兼容 JavaScript 的，它不会修改 JavaScript 运行时的特性，所以它们都是弱类型。

作为对比Python 是强类型

>TypeScript 的核心设计理念[6]：在完整保留 JavaScript 运行时行为的基础上，通过引入静态类型系统来提高代码的可维护性，减少可能出现的 bug。

约定使用 TypeScript 编写的文件以 .ts 为后缀，用 TypeScript 编写 React 时，以 .tsx 为后缀。

