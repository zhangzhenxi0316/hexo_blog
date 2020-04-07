---
title: php笔记1
date: 2020-04-06 10:29:04
tags:
    -php
    -学习笔记
categories: 前端
---
## php初步学习
php代码都要写在<?php...?>
php和html相互结合进行使用
php文件默认扩展名是.php
php代码必须在服务器中执行
每一句后面都要加;否则报错

### 基础语法
echo "输出到界面";  可以加标签

```
echo "<h1>hello php</h1>";
```
print_r 输出复杂类型
var_dump 输出复杂类型

php可以和html结合使用
在php文件中可以使html骨架在骨架中使用<?php...?>就可以使用php了

$声明变量
使用变量也要加$
```
$str = "hello";
echo $str;
```

可以做运算和字符串的拼接
php中+代表数学运算
拼接用 . 
```
$number1 = 100;
$number2 = 200;
$number3 = $number1 + $number2;  //300
$str1 = "hello";
$str2 = "world";
$str3 = $str1 . $str2;
```

数组的使用
```
$arr = array();  //定义数组
$arr[0] = "number1";
$arr[1] = "num2";
//echo 不能整个输出数组可以单个输出字符串
echo $arr[1];
print_r($arr);  //[0]=>number1 [1]=>num2
var_dump($arr)   //更加详细的内容可以返回数组每个元素类型及其信息
echo json_encode($arr)  //json_encode()将数组转换成json格式的字符串并反回
```

也能通过arry("str1","str2")
数组索引可以自定义
```
$arr = array("name"=>"zzx","age","sex");
//zzx的索引就是name, age索引是0，改变索引其他没有key的还是按照数字当做索引
echo arr["name"];
数组有二维数组
$arr1 = array();
$arr1["zhangsan"] = array("age","sex");   //二维数组
```

数组遍历
```
for($i = 0;$i<count($arr);$i++){
    echo $arr[i];
}
foreach($arr as $key =>$value){
    echo $key . ">>>" . $value
}
```

函数定义
```
function add($num1,$num2){
    return $num1 + $num2;
}
```

get请求放在地址栏url后面用&链接
```
$_GET["username"]  //获取表单传送过来的get中username的值
```
post
```
$_POST["username"]
```

array_key_exists(key,array)  //判断是否在数组中有key这个索引
php可以跨越着写如
```
<?php
if(array_key_exits($code,$data)){
?>
html代码
<?php
    }else{
        php代码
    }
?>
```
