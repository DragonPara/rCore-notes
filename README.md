# rCore-notes
学习用rust写一个精简指令集操作系统

参考文档：https://learningos.cn/rCore-Tutorial-Guide-2024S/index.html
```asm
target/riscv64gc-unknown-none-elf/debug/ch1:    file format elf64-littleriscv

Disassembly of section .text:

0000000000011158 <_start>:
;     loop{};
   11158: 09 a0         j       0x1115a <_start+0x2>
   1115a: 01 a0         j       0x1115a <_start+0x2>
```
`;     loop{};` 表示注释，如果编译时加--release，则不生成该注释

`11158`表示指令地址，程序入口即为第一条指令的位置

`j`跳转

`0x1115a`是跳转的地址，可知前面的指令地址`11158`也是16进制的
`0x1115a` 和 `<_start+0x2>` 表示同一个位置
