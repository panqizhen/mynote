基础：
$GLOBALS:所有*全局变量*数组
$_SEVER*服务器*环境变量数组
$_FILES文件上传相关变量
$_ENV 环境变量数组
*常量一旦被定义就无法修改*
魔法常量 __FUNCTION__  __CLASS__可能有用
返回多个值的函数调用：可以通过返回*数组*，使用*list()*函数获取list($a,$b,$c)=$arr;
变量名分大小写而函数不分
一般变量在函数内外是无关的，相当于两个变量
global $a 用来声明全局变量，不推荐同$GLOBALS['a']=5
include 'include.php'效果和在同位置复制该文件内容一样
required('init.php')于include基本相同，require会爆致命错误，而include会警告
settype()设置变量类型，返回布尔值bool settype ( mixed &$var , string $type )
gettype()返回string类型

