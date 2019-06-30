## 基础语法

#### 基础语法

1.PHP 脚本可以放在文档中的任何位置。

2.PHP 脚本以 **<?php** 开始，以 **?>** 结束：

3.PHP 文件的默认文件扩展名是 ".php"。

4.PHP 文件通常包含 HTML 标签和一些 PHP 脚本代码。

```php
<!DOCTYPE html> 
<html> 
<body> 

<h1>My first PHP page</h1> 

<?php 
echo "Hello World!"; 
?> 

</body> 
</html>
```

#### 变量

1.变量是用于存储数据的容器。

2.定义变量以开头$符定义,后面接着变量名,

3.变量名必须以字母或者下划线开始

4.变量名是区分大小写的

```php
<?php
$str = "hello world";
$a = 1;    
$b = $a;   
echo $b;   //1
?>
```

#### 常量

1.常量是一个简单值的标识符。该值在脚本中不能改变。

2.常量在整个脚本中都可以使用。

3.常量有三个参数 define(**name**:常量名,**value**:值,**case_insensitive**:是否大小写敏感) 

- 第一第二个参数是必选参数
- 第三个参数是可选参数
- 定义常量是全局的

```php
<?php
// 区分大小写的常量名
define("GLOBALNAME", "hello world");
echo GREETING;    // hello world
?>
```



#### 作用域

PHP 有三种不同的变量作用域：

- local   // 局部
- global    //全局
- static      // 静态

```php
<?php
$a = 10;   //global
function test() {
$b = 20;     // local

echo "内部测试:".$a;
echo "内部测试:".$b;
}
test()
echo "外部测试".$a;   
echo "外部测试".$b;

// 内部测试:
// 内部测试:20;

// 外部测试:10;
// 外部测试:


// 以上test函数里访问外部的话 
{
  //代码块内加入
    global $a;
  //	$a 即可访问变量
}
?>
```

#### 数组

##### 数值数组

1.定义数组,$arr = array("apple",1,"name");

2.取数组值,$arr[0]  //apple ,根据数组下标取值.   下标是创建数组时自动分配的ID键,第一个以0开始,以逗号分割

3.获取数组长度 count($arr);   // 3

4.遍历数组

```php
<?php
$arr=array("Volvo","BMW","Toyota");  //创建数组
$arrlength=count($arr);   //获取长度
 
for($i=0;$i<$arrlength;$i++)
{
    echo $arr[$i];   //取出arr 下标第i个值
    echo "<br>";
}
?>
```

##### 关联数组

1.关联数组是使用您分配给数组的指定的键的数组。

2.关联数组创建及取值和遍历方法：

```php
// 创建关联数组
$arr = array("Peter"=>"35","Ben"=>"37","Joe"=>"43"); 

// 取出数组的值
echo $arr['peter'];

 // 遍历关联数组
foreach($arr as $i=>$i_value)  // $x是key-$i_value
{
    echo "Key=" . $i . ", Value=" . $i_value;
    echo "<br>";
}

```

