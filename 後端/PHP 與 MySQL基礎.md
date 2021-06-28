## 環境建置
均使用 XAMPP 安裝
https://www.apachefriends.org/zh_tw/index.html


## 啟動 XAMPP
點一下Start鈕，將它啟用
![](https://photo.minwt.com/img/Content/mac/xampp-for-mac/xampp-4-mac_03.jpg)

接著再切到Services，將要使用的服務給開啟，目前只需開啟Apache與MySQL二個就可以了。
![](https://photo.minwt.com/img/Content/mac/xampp-for-mac/xampp-4-mac_04.jpg)

點 enable 按鈕啟動 “8080" port
![螢幕快照 2021-06-22 下午10.11.57](https://i.imgur.com/2iE0DyW.png)

成功導向 http://localhost:8080/dashboard/

先點 Mout 再點 Explore
![螢幕快照 2021-06-22 下午10.13.52](https://i.imgur.com/SuZEtP6.png)

就會跳出此畫面
![螢幕快照 2021-06-22 下午10.14.47](https://i.imgur.com/fdILIr0.png)

index 檔案對應的就是預設檔
![螢幕快照 2021-06-22 下午10.15.45](https://i.imgur.com/kn8jjMo.png)


## PHP 基本語法
```php
<?php
  // 包在裡面才會被當作是 php 的內容
  // 每行結尾必須要有分號 ;
  echo "123"; // 輸出 123
  echo "<h1>ABC</h1>";

  $a = "Za "; 
  // $ 代表設變數的意思，任何變數的最前面必定有 $
  $b = "Warudo!!!"
  echo $a . $b; // 輸出 $a 和 $b 兩個變數字串拼接的內容
?>
```
設變數
```php
<?php
  $a = "Za "; 
  // $ 代表設變數的意思，任何變數的最前面必定有 $
  $b = "Warudo!!!"
  echo $a . $b; // 輸出 $a 和 $b 兩個變數字串拼接的內容
?>
```
陣列
```
<?php
  $arr = array(1, 2, 3, 4, 5);
  echo $arr[0]; // 輸出 arr 中 index 為 0 的內容
  echo "length" . sizeof($arr); // sizeof() 是 arr 的長度
  var_dump($arr); // 輸出 type, value
  print_r($arr); // 輸出 value
?>
```
php 變數宣告 `$` (使用時也要加 `$`)
php 字串拼接 `.`
php 換行 `<br>`
php 拿到 arr 長度 `sizeof`
php 印出 `echo` （只印 string）
php 印出 `var_dump` （把所有型態跟值都印）

request => apache(server) => php => html => apache => response

---
### 資料庫系統
![](https://i.imgur.com/MuuwmrZ.png)
server => 程式，專門處理 request 跟 response 的程式
資料庫系統 => 程式，專門處理資料的程式

Server：專門處理 Request 和 Response 的程序
資料庫系統：專門處理資料的程序

##### 關聯式資料庫 SQL 
要先定義表結構 (想像成excel)
業界最常用 MySQL

#### 非關聯式資料庫 NoSQL （not only SQL） 
相較於 SQL 只能存儲單一類型的數據，沒有 SQL 可以存儲的數據更複雜一些，比較常存日誌日誌
優點是比較活躍，如果要增加排位則不用去改變資料庫設計

存取資料格式為 json
資料結構自由，缺點太自由很難新增資料

業界最常用 PostgreSQL

### MySQL 語法基礎

### 管理資料庫軟體
phpmyadmin

本機網址 （開啟 XAMPP）
http://localhost:8080/phpmyadmin/


![螢幕快照 2021-06-24 下午8.46.19](https://i.imgur.com/kfkPGtF.png)
![螢幕快照 2021-06-24 下午8.53.07](https://i.imgur.com/V6OK2Aj.jpg)

## SQL 指令
這寫指令都可以按這些按鈕得到
![Xnip2021-06-27_20-54-39](https://i.imgur.com/7LRNjqM.jpg)

#### 查詢資料 Select
>語句中的 `SELECT`和 `FROM` 語句是必須的，其他部分是任選的。

`SELECT`之後是要注意的列或星號（`*`的列表），顯示返回所有列。
`FROM` 指定要查詢數據的表或視圖。
`JOIN` 可根據部分連接條件從其他表中獲取數據。
`WHERE` 過濾結果集中的行。
`GROUP BY` 將一排組合成小成績，每個小成績應用程序。
`HAVING` 過濾器基於 `GROUP BY` 子句定義的小成績。
`ORDER BY` 指定用於排序的列的列表。
`LIMIT` 限制返回行的數量。


``` SQL
SELECT * FROM `XXX檔案` 
```
```SQL
SELECT id as name FROM `XXX檔案`
```

```SQL
SELECT * FROM `XXX檔案` where username = 'XXXX'
```
#### 新增資料 Insert
新增單行資料
```SQL
INSERT INTO table(column1,column2...) VALUES (value1,value2,...);
```
插入多行資料
```SQL
INSERT INTO table(column1,column2...)
VALUES (value1,value2,...),
       (value1,value2,...),
...;
```

####  修改資料 Update
>`WHERE`非常重要，如果忘記寫上`WHERE`子句，可能會更新表中的所有行。

首先，在`UPDATE`關鍵字指定要更新數據的表名。
即將，`SET`子句指定要修改的列和新值。要多個，請使用以防止更新影響的列表。以字面值，表達式或子查詢的形式在每列的賦值列中來提供要設置的值。
第三，使用`WHERE`子句中的條件指定要更新的行。`WHERE`子句是任選的。如果省略`WHERE`子句，則更新語句將更新表中的所有行。


```SQL
UPDATE [LOW_PRIORITY] [IGNORE] table_name 
SET 
    column_name1 = expr1,
    column_name2 = expr2,
    ...
WHERE
    condition;
```

####  刪除資料 Delete
>`WHERE`在這非常重要，沒有將`WHERE`系統添加到所有行為中，即會刪除所有數據。
一般不會使用`DELETE`，因為顯示刪除了就找不回這些資料；相對應的做法是在表中，加上`is_deleted`行來操作內容是否該筆資料。


```SQL
DELETE FROM table_name WHERE condition;
```

#### 修改表格屬性
修改名稱表格

```SQL
ALTER TABLE old_table_name RENAME TO new_table_name;
```

修改屬性（設置唯一值）
```SQL
ALTER TABLE table_name ADD unique(`username`);
```

