1. 字串反轉
給一個字串 str，請輸出 str 反過來的結果
範例輸入：hello
範例輸出：olleh
PS. 可以用 str[i] 取得第 i 個字，例如說 str="abc"，str[0] 就是 'a'

```
var str
var strReverse
for (i from str.length to 0) do
    strReverse＋＝str[i]
end for
print strReverse
```

2. 陣列總和
給一個陣列 arr，裡面全都包含了數字（整數），請輸出陣列加總的結果（總和保證不超過 int 範圍）
範例輸入：[1, 2, 3]
範例輸出：6

```

for (i form 0 to arr.length) do
    num + = arr[i]
end for
print num
```


3. 找最大值
給一個陣列 arr，裡面全都包含了數字（整數），請輸出陣列中的最大值
範例輸入：[1, 2, 3]
範例輸出：3

- var array = [] 
- 

```
var bigNum = arr[0];
for (i from 0 to arr.length) do
    if (bigNum < arr[i]) do
    bigNum = arr[i]
    end if
end for
print bigNum
```