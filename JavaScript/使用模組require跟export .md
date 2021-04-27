
### 使用模組：require 
把別人寫好的功能引入進來  / 模組化概念
[node.js os module 可使用](https://nodejs.org/dist/latest-v12.x/docs/api/os.html)

使用範例：檢查目前的作業系統
[os.platform( )文件](https://nodejs.org/dist/latest-v12.x/docs/api/os.html#os_os_platform)

```
var osModule = require('os'); //使用的模組名
console.log(osModule.platform()); // platform() 印出使用的作業系統
```

### 自創模組：export

模組檔案 myModule.js
```
function double(n) {
    return n * 2;
}
module.exports = double;  // 定義模組，也可以輸出變數陣列，就看 exports 傳出的東西
```

exports 方法差異
```
module.exports = double; // 可以輸出任何東西 
exports.double = double; // 傳出來的東西會是個物件 （少用，想了解可以在查詳細）
```

使用模組檔案 
```
var useMyModule = require('./myModule.js'); // 模組檔案路徑
console.log(useMyModule(2));

結果 4
```