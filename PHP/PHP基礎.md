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
 echo "123";
?>

```

php 變數宣告 `$` (使用時也要加 `$`)
php 字串拼接 `.`
php 換行 `<br>`
php 拿到 arr 長度 `sizeof`
php 印出 `echo` （只印 string）
php 印出 `var_dump` （把所有型態跟值都印）
