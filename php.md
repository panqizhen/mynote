基础：
is_array(),检查是否是数组
is_scalar(),是否标量
is_callable(),是否是有效的函数名
unset()销毁变量；
switch(){
    case "a" :
    echo "this is a";
    break;
    case "b" :
    echo "this is b";
    break;
    default:
    echo "this is not a or b";
    break;
}
while循环 和 for 循环：当不知道循环所需的重复次数时用while循环，如果要求固定次数的重复就用for循环；
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
文件操作：fopen('file',type);
1.读文件
r只读，文件头开始;r+，读写文件头开始如果文件不存在则创建；
w,只写，从文件头开始写，如果文件已存在则会删除所有已有内容，如果文件不存在则创建，w可写
x谨慎写，如果文件存在则不会打开，返回false，文件不存在则会创建并从头写；
a追加，如果文件已有内容，从后面追加，如果文件不存在则创建；
b二进制，通常和打开模式结合 如rb,wb;
fopen支持通过fttp、ftp或其他协议打开文件，在php.ini中可以通过关闭allow_url_fopen来禁用此功能；
如果使用的文件名是ftp://开头的，fopen将建立一个链接到指定服务器的*被动模式*，并返回指针；
2.写文件，可用fwrite()或fputs(),fputs是fwrited的别名函数
也可以用 intfile_put_contents(string filename，string data[,int flags[,resource context]])这个函数可以不用打开文件，将data中的数据写入文件。当使用ftp或http时，最常用的参数是flags和context。
int fwrite(handle,string data[,length])length表示写入的最大字符数，当使用二进制写入的时候可能会用到
关闭文件fclose() 
知道何时读完文件：feof()
while(!feof($fp))，作为循环读取，判断结束的条件
每次读取一行数据：fgets();变体fgetss()会过滤html和php更安全，fgetcsv()更方便格式化
读取一个字符fgetc()
读取整个文件:readfile(),打开文件，将文件内容输出到标准输出（浏览器）中然后关闭文件
读取任意长度：fread()
查看文件是否存在file_exists()
文件大小file_size();
删除文件unlink()
文件锁定：fclock()，当一个文件被打开并且在读写操作前应该被锁住