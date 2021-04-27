ES6 解釋：ECMAScript 6 在 2015 年正式發佈
ES6 = ES2015

## 定義變數
`let`   作用域變數
`const` 常數 （永不變）

## Template Literals 字串模板
範例
``` javascript
var name = '小哩';
var str = `你好，我是${name}`;
console.log(str);

結果
你好，我是小哩
```

## Destructuring 解構
可用在 `array` 跟 `object`

`array`範例
``` javascript
const arr = [2, 3, 4];
var [first, second] = arr;

// 程式碼等於es5 
var first = arr[0];
var second = arr[1];
// es5 end 

console.log(first, second)

結果
2 3
```

`object`範例
``` javascript
var obj = {
    name:'nick',
    age:30
}

var {name,age} = obj

// 程式碼等於es5 
var name = obj.name;
var age = obj.age;
// es5 end

console.log(name, age);

結果
'nick' 30
```


`object`範例 - 也可以雙層解構
``` javascript
const obj = {
    name: 'nick'
};
var {name} = obj
console.log(name);

結果
nick
```

## Spread Operator 展開
也可以用在複製 `array` `object` 的值  
`...{要展開的陣列or變數}` 展開 
``` javascript
var arrIn = ['A', 'B', 'C'];
var arr1 = [1, 2, 3, arrIn];
var arr2 = [1, 2, 3, ...arrIn]; // 展開arrIn

console.log(arr1);
console.log(arr2);

結果
[ 1, 2, 3, [ 'A', 'B', 'C' ] ]
[ 1, 2, 3, 'A', 'B', 'C' ]
```

## Rest Parameters 類反向展開

``` javascript
var arr = ['A', 'B', 'C', 'D'];
var [first, ...rest] = arr;
console.log(first);
console.log(rest); //印出剩下的

結果
A
[ 'B', 'C', 'D' ]
```

 
## Default Parameters 預設值

範例
```javascript
function repeat(str, num = 5) { //num 沒帶值的話，預設為5
    return str.repeat(num);
}
console.log(repeat('abc'));

結果
abcabcabcabcabc
```
## Arrow Function 箭頭函式 

``` javascript
const test = (n) => { 
  console.log(n)
}
test(2)

結果
2
```

## export 與 import
簡化 module 寫法
>tips:
>無法使用 node 執行，會報錯

執行指令，要裝Babel套件且設定好才有效
```
npx babel-node {檔案}
```

myModule.js
```javascript
// 只需要在想模組的 function / object / 變數 前加上 export 即可
export function double(n) {
    return n * 2;
}

export PI = 3.14
```

使用模組的檔案
```javascript
import {double} from './myModule.js';

console.log(double(5));
```

## Babel 套件
>TODO:筆記待補
ES6/7/8 轉換為 ES5 語法

[Babel 安裝說明](https://babeljs.io/docs/en/babel-node.html)

設定步驟：

1.安裝必要套件：npm install --save-dev @babel/core @babel/node @babel/preset-env
2.新增 .babelrc 檔案
3.在 .babelrc 填入內容，告訴 babel 要用這個 preset：
{

 "presets": ["@babel/preset-env"]

}

4.最後使用 `npx babel-node {檔案}` 即可 (就可以使用 export 與 import)