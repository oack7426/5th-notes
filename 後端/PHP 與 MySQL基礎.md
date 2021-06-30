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

#### 清除快取 XAMPP
![Xnip2021-06-28_21-59-13](https://i.imgur.com/872NoX3.jpg)

#### 建立專案
http://localhost:8080/test/
其他頁 例如 data.php http://localhost:8080/test/data.php
![Xnip2021-06-29_22-38-48](https://i.imgur.com/37RvUX4.jpg)

## php 運作原理
![Xnip2021-06-28_22-02-42](https://i.imgur.com/0n1Iz0r.jpg)
## PHP 基本語法
###### 筆記參考
[第 60 天 - PHP 與 MySQL 入門](https://www.coderbridge.com/series/e6ca520d20de4f8497e17d1a8d95245f/posts/2da4b41f85134ac5a4042325b43b85dc)
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
### 從前端傳資料給後端：GET 與 POST
基本的前後端溝通 表單
![Xnip2021-06-28_22-24-51](https://i.imgur.com/NXtAj2A.jpg)
#### php $_GET
> 假設網址是 ?a=&b=，只有傳 key 沒有傳 value，`isset` 的結果依舊會是 `true` 必須連 key 都沒有傳，`isset` 才會是 `false`
因此針對這種檢查，會推薦使用 `empty` 來檢測，因為 `empty` 可以順便檢測空字串的狀況

![Xnip2021-06-28_22-17-11](https://i.imgur.com/pjjSCMI.jpg)![Xnip2021-06-28_22-17-41](https://i.imgur.com/VxexIzZ.jpg)

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

#### 管理資料庫軟體
phpmyadmin

本機網址 （開啟 XAMPP）
http://localhost:8080/phpmyadmin/

### 新增使用者 & 同時建表
![Xnip2021-06-29_23-07-03](https://i.imgur.com/xBnvAkm.jpg)

### 建表
![Xnip2021-06-29_22-30-07](https://i.imgur.com/e1k82tc.jpg)
![Xnip2021-06-29_22-36-02](https://i.imgur.com/XQnW5q9.jpg)
![Xnip2021-06-29_22-33-11](https://i.imgur.com/ITfCgLp.jpg)

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

#### 從 PHP 連線到 MySQL 資料庫
>建議事先將伺服器位置、登入帳號、密碼、資料庫名稱等輸入資訊作為變數宣告在開頭
推薦將PHP連線的程式碼額外寫在單一的PHP檔案內(conn.php)，要使用時再從程式碼中引用即可

conn.php 
``` php
<?php
  $server_name = 'localhost';  //伺服器位置
  $username = 'annie'; //登入帳號
  $password = 'annie'; //密碼
  $db_name = 'annie'; //資料庫名稱

  $conn = new mysqli($server_name, $username, $password, $db_name);

  if ($conn->connect_error) {
    die('資料庫連線錯誤:' . $conn->connect_error);
  }

  $conn->query('SET NAMES UTF8'); // 設定編碼 UTF8
  $conn->query('SET time_zone = "+8:00"'); //設定時區為台灣
?>
```

##### PHP 與 MySQL 的互動：讀取資料
data.php
```php
<?php
  require_once('conn.php');

  $result = $conn->query("SELECT * FROM users");
  if (!$result) { //如果空值
    die($conn->error); //die 跳出程式不執行 
    //$conn 的定義在 conn.php
    //$conn->error 顯示錯誤資訊
  }

  while ($row = $result->fetch_assoc()) {
    echo "id:" . $row['id'] . '<br>';
    echo "name:" . $row['name'] . '<br>';
  }
?>
```

##### PHP 與 MySQL 的互動：新增資料 
單純塞入資料
![Xnip2021-06-30_22-36-28](https://i.imgur.com/xuiF4TB.jpg)
data.php
```php
<?php
  require_once('conn.php');

  $result = $conn->query("insert into users(name) values('apple')");
  // 在 users 的資料表新增 name = apple 的資料  呼叫多次就會塞入多次同筆資料
  if (!$result) {
    die($conn->error);
  }
  print_r($result) 
  //會印出 1 代表 true 成功新增資料
?>
```
透過表單塞入資料
![Xnip2021-06-30_22-44-35](https://i.imgur.com/Wx5FBvj.jpg)
![Xnip2021-06-30_22-44-43](https://i.imgur.com/MWUgy1N.jpg)
![Xnip2021-06-30_22-44-57](https://i.imgur.com/O9DKymf.jpg)
index.php
```html
<form method="POST" action="data.php">
 user:<input name="name">
  <input type="submit">
</form>
```

data.php
```php
<?php
  require_once('conn.php');

  if (empty($_POST['name'])) {
    die('請輸入 name');
  }

  $name = $_POST['name'];
  $sql = sprintf(
    "insert into users(name) values('%s')",
    $name
  );
  $result = $conn->query($sql);
  if (!$result) {
    die($conn->error);
  }
  echo "新增成功"

  header("Location: index.php"); // 跳轉回首頁
?>
?>

```


PHP 與 MySQL 的互動：刪除資料
PHP 與 MySQL 的互動：編輯資料


