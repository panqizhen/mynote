移动：
hjkl对应左下上右，
ctrl+f,ctrl+b前后移一页
gg文件首行起始位置,G文件尾行起始,NG或Ngg移动到N行
H,M,L屏幕起始中间最后
搜索：
/str enter开始搜索，n表示继续，N往前，
替换r,删除字符x,删除行dd
s用输入的正文替换光标所知字符串
S删除当前行进入编辑模式
p粘贴到前,P粘贴到后
yy复制到缓存区
"+y复制到系统粘贴板
u撤销前一条命令
.重复前一条命令
i前插入模式,I行最前插入,a后插入模式,A行最后插入,o下一行添加新行
:进入命令模式
:w保存，:w file_temp另存,zz保存并退出vim
:q不保存退出，:q!不保存退出vim
:n移动到n行