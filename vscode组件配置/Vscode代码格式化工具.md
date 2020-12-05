#### 一.EditorConfig for vs code：

常用属性配置:（当前vscode支持属性&&）

1、root<boolean> : 是否是顶级配置文件，设置为true的时候才会停止搜索.editorconfig文件

2、charset<"latin" | "utf-8" | "utf-8-bom" | "utf-16be" | "utf-16le">   :  文件编码格式

3、indent_style<"tab" | "space">  ：  缩进方式      &&

4、indent_size<number>  ：   缩进大小    &&

5、end_of_line<"lf" | "cr" | "crlf">  ：  换行符类型   &&

6、insert_final_newline<boolean>  ：   是否让文件以空行结束  &&

7、trim_trailing_whitespace<boolean> ：  是否删除行尾空格   &&

8、max_line_length<number>  ：   最大行宽。

参考：https://blog.csdn.net/my_new_way/article/details/105177715

注释：

LF (Line Feed)：换行符，’\n’，表示切换到下一行，ASCII码为10  unix系统及类unix系统

CR (Carriage Return)：回车符，’\r’，表示回到当前行的开头，ASCII码为13 

CRLF：一个回车符和一个换行符，"\r\n"     window系统