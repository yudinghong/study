# NASM
## cmd line

`nasm -f <format> <filename>[-o <output>][-l <list>]`
* format 
  * elf 
  * bin
  * coff

`-M 产生Makefile依赖关系`
`-F 选择一个调试格式`
`-g 使调试信息有效`
`-E 把错误信息输入到文件`
`-s 把错误信息输出到stdout`
`-i 包含文件搜索路径`
`-p 预包含一个文件`
`-d 预定义一个宏`
`-u`
`-e`
`-a`
`-On`
`-t`
`-w`
`-v`

## 程序行组成
`label: instruction operands ;comment`
`\`续行符

### 伪指令
`DB DW DD DQ DT ;声明初始化的变量`
`RESB RESW RESD RESQ REST INCBIN ;声明未初始化的变量` `INCBIN ;二进制文件 incbin "file.dat"`