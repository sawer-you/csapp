# IA32 CPU

31|15|   8|7    0

%eax | %ax | %ah | %al
--- | ---: | :---: |:---:
%ecx | %ax | %ah | %al
%edx|%dx|%dh|%dl
%ebx|%bx|%bh|%bl
%esi|%si||
%edi|%di||
%esp|%sp||
%ebp|%bp||

类型 | 格式 | 操作数值 | 名称
--- | --- | --- | ---
立即数 | $_Imm_ | _Imm_ | 立即数寻址
寄存器 | E<sub>_a_</sub> | R\[E<sub>_a_</sub>] | 寄存器寻址
存储器 | _Imm_ | M\[_Imm_] | 绝对寻址
存储器  | (E<sub>_a_</sub>) | M\[R\[E<sub>_a_</sub>]] | 间接寻址
存储器  | _Imm_(E<sub>_a_</sub>) | M\[_Imm_ + R\[E<sub>_a_</sub>]] | (基址+偏移量) 寻址
存储器 | (E<sub>_b_</sub>, E<sub>_i_</sub>) | M\[R\[E<sub>_b_</sub> + R\[E<sub> _i_ </sub>]]] | 变址寻址
存储器  | _Imm_(E<sub>_b_</sub>, E<sub>_i_</sub>) | M\[_Imm_ + R\[E<sub>_b_</sub> + R\[E<sub> _i_ </sub>]]] | 变址寻址
存储器  | (, E<sub>_i_</sub>, _s_) | M\[R\[E<sub>_i_</sub>] · _s_] | 比例变址寻址
存储器  | _Imm_(, E<sub>_i_</sub>, _s_) | M\[_Imm_ + R\[E<sub>_i_</sub>] · _s_] | 比例变址寻址
存储器  | (E<sub>_b_</sub>, E<sub>_i_</sub>, _s_) | M\[R\[E<sub>_b_</sub>] + R\[E<sub>_i_</sub>] · _s_] | 比例变址寻址
存储器  | **_Imm_(E<sub>_b_</sub>, E<sub>_i_</sub>, _s_)** | M\[_Imm_ + R\[E<sub>_b_</sub>] + R\[E<sub>_i_</sub>] · _s_] | 比例变址寻址

# 指令
**MOV** movb movw movl  
**MOVS** movsbw movsbl movswl  
**MOVZ** movzbw movzbl movzwl pushl popl  
leal  
INC, DEC, NEG, NOT.  
ADD, SUB, IMUL, XOR, OR, AND.  
SAL, SHL, SAR, SHR.

# condition code
CF : 进位标志。
ZF : 零标志。
SF : 符号标志。
OF : 溢出标志。
指令 : CMP S<sub>1</sub> - S<sub>2</sub>, TEST S<sub>1</sub> & S<sub>2</sub>
