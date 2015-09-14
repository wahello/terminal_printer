# terminal printer

##### 在使用link等快捷方式,或者在其他目录调用主程序时,字体目录需要使用绝对路径,即需要指定程序所在绝对目录
##### (当然如果在主程序当前目录的话随意)
##### 如果输出结果为乱码,说明该字体不支持这个字(出现问题一般都是中文,即中文字体库不完全)
##### 当在终端打印图片时,终端字体越小,终端越大(目测高分屏显示效果比较理想,然而并没有尝试过),理论上显示的再现度越高(当初想在rmbp上试一下~~然而还没有机会) 
##### 主程序并不大,臃肿的是字体库,下一个版本再尝试调用系统字体库
>* 程序的临时目录使用 /tmp 未考虑多用户调用,且使用同一个临时文件名,由于 /tmp 的特殊权限,多用户先后调用程序会发生错误,下一版本修改该bug
>>* 临时文件名加上当前用户名区分,目前使用应该不会出现该问题

+ 中英文混合输入时字体宽度异常
+ 计划将中文英文在同一行中分别输出,这将导致核心部分大面积重写(猜测)