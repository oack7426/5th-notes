解題系統分兩種
1.LeetCode - 實作function
2.LIOJ - 

## LIOJ
### 第一種 - 鍵盤輸入測試
用 `node` 執行 ex: `node test.js`
然後再用 input(鍵盤輸入對應測資) 輸入
結束 `ctrl + D`
![螢幕快照 2021-04-20 下午10.05.11](https://i.imgur.com/mEwQ2Fj.png)

### 第二種 - 外部檔案測試
`cat XXX.txt | node XXX.js` 把 XXX.txt 的東西輸入到 XXX.js

```
var readline = require('readline');
var rl = readline.createInterface({
  input: process.stdin
});

var lines = []

// 讀取到一行，先把這一行加進去 lines 陣列，最後再一起處理
rl.on('line', function (line) {
  lines.push(line)
});

// 輸入結束，開始針對 lines 做處理
rl.on('close', function() {
  solve(lines)
})

// 上面都不用管，只需要完成這個 function 就好，可以透過 lines[i] 拿取內容
function solve(lines) {
}




```