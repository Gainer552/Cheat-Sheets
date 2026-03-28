# 𝗦𝗵𝗲𝗯𝗮𝗻𝗴

- `#!/usr/bin/env -S nasm -felf64 /dev/stdin && ld -o /tmp/asmprog /dev/stdin && /tmp/asmprog`
Note: Optional Unix shell trick for assembling/linking from piped input. Standard Assembly source files do not require a shebang because Assembly is assembled and linked before execution.

# 𝗘𝗺𝗯𝗲𝗱𝗱𝗲𝗱 𝗖𝗼𝗱𝗲 𝗕𝗹𝗼𝗰𝗸

- `; Code goes here!`
- `; Single-line comment in many Assembly syntaxes.`
- `# Alternative comment style in some assemblers/preprocessors.`
- `# Used for documentation, disabling code, or explaining instructions.`

# 𝗘𝘀𝘀𝗲𝗻𝘁𝗶𝗮𝗹 𝗔𝘀𝘀𝗲𝗺𝗯𝗹𝘆 𝗕𝘂𝗶𝗹𝘁-𝗶𝗻 𝗖𝗼𝗺𝗺𝗮𝗻𝗱𝘀

### Program Structure & Toolchain

- `section / segment` - Define a section of the program, such as code, data, or uninitialized data.
- `global` - Export a symbol for the linker.
- `extern` - Declare a symbol defined in another object file or library.
- `label:` - Define a named address.
- `equ` - Define a constant symbol.
- `times` - Repeat data/instructions in assemblers like `NASM`.
- `db / dw / dd / dq` - Define initialized byte, word, doubleword, quadword data.
- `resb / resw / resd / resq` - Reserve uninitialized storage in `.bss`.
- `org` - Set program origin in some formats.
- `bits` - Specify target instruction size mode in `NASM` (`16/32/64`).
- `cpu` - Specify target CPU features in some assemblers.

### Data Movement

- `mov` - Copy data between registers, memory, and immediates.
- `movzx` - Move with zero-extension.
- `movsx / movsxd` - Move with sign-extension.
- `lea` - Load effective address.
- `xchg` - Exchange two operands.
- `push` - Push value onto the stack.
- `pop` - Pop value from the stack.

### Arithmetic

- `add` - Add operands.
- `sub` - Subtract operands.
- `inc` - Increment.
- `dec` - Decrement.
- `imul` - Signed multiply.
- `mul` - Unsigned multiply.
- `idiv` - Signed divide.
- `div` - Unsigned divide.
- `neg` - Two's complement negation.
- `adc` - Add with carry.
- `sbb` - Subtract with borrow.

### Bitwise & Shift

- `and` - Bitwise AND.
- `or` - Bitwise OR.
- `xor` - Bitwise XOR.
- `not` - Bitwise NOT.
- `test` - Bitwise AND for flags only, result not stored.
- `shl / sal` - Shift left.
- `shr` - Logical shift right.
- `sar` - Arithmetic shift right.
- `rol / ror` - Rotate left/right.
- `rcl / rcr` - Rotate through carry.

### Comparison & Control Flow

- `cmp` - Compare operands by subtraction and set flags.
- `jmp` - Unconditional jump.
- `je / jz` - Jump if equal / zero.
- `jne / jnz` - Jump if not equal / not zero.
- `jg / jnle` - Jump if greater (signed).
- `jge / jnl` - Jump if greater or equal (signed).
- `jl / jnge` - Jump if less (signed).
- `jle / jng` - Jump if less or equal (signed).
- `ja / jnbe` - Jump if above (unsigned).
- `jae / jnb` - Jump if above or equal (unsigned).
- `jb / jnae` - Jump if below (unsigned).
- `jbe / jna` - Jump if below or equal (unsigned).
- `jc / jnc` - Jump if carry / no carry.
- `jo / jno` - Jump if overflow / no overflow.
- `js / jns` - Jump if sign / no sign.
- `loop` - Decrement `CX/ECX/RCX` and jump if nonzero.
- `call` - Call a procedure/function.
- `ret` - Return from procedure/function.
- `int` - Software interrupt.
- `syscall` - Invoke operating system syscall on x86-64.
- `sysenter / sysexit` - Fast syscall mechanism on some systems.

### Flags & Condition Codes

- `ZF` - Zero flag.
- `CF` - Carry flag.
- `SF` - Sign flag.
- `OF` - Overflow flag.
- `PF` - Parity flag.
- `AF` - Auxiliary carry flag.
- `DF` - Direction flag.

### String/Memory Instructions

- `movsb / movsw / movsd / movsq` - Move string data.
- `stosb / stosw / stosd / stosq` - Store accumulator to memory.
- `lodsb / lodsw / lodsd / lodsq` - Load memory into accumulator.
- `cmpsb / cmpsw / cmpsd / cmpsq` - Compare string data.
- `scasb / scasw / scasd / scasq` - Scan string data.
- `rep / repe / repne` - Repeat string instructions based on count/flags.

### Procedure & Stack Management

- `enter` - Create stack frame.
- `leave` - Tear down stack frame.
- `nop` - No operation.
- `hlt` - Halt CPU until interrupt (privileged/special use).
- `cld / std` - Clear/set direction flag.
- `stc / clc / cmc` - Set/clear/complement carry flag.

### Common Registers (x86/x86-64)

- `rax / eax / ax / al` - Accumulator register.
- `rbx / ebx / bx / bl` - Base register.
- `rcx / ecx / cx / cl` - Counter register.
- `rdx / edx / dx / dl` - Data register.
- `rsi / esi / si / sil` - Source index.
- `rdi / edi / di / dil` - Destination index.
- `rbp / ebp / bp / bpl` - Base/frame pointer.
- `rsp / esp / sp / spl` - Stack pointer.
- `r8-r15` - Additional general-purpose registers in x86-64.
- `rip / eip / ip` - Instruction pointer.
- `xmm0-xmm15` - SIMD floating-point/vector registers.
- `ymm0-ymm15 / zmm0-zmm31` - Wider SIMD vector registers (`AVX/AVX-512`).

### Common Directives/Concepts Across Assemblers

- `macro / endm / %macro` - Macro definition.
- `include / %include` - Include another source file.
- `align` - Align data/code boundary.
- `public` - Export symbol (`MASM/TASM` style).
- `proc / endp` - Procedure declaration in `MASM`-style syntax.
- `extern printf` - Link against external symbols provided by other object files/libraries.
- `syscall / int 0x80` - OS interaction for I/O on Linux, depending on `ABI/architecture`.
- `call printf` - Call C library I/O after proper linking and calling convention setup.

# 𝘿𝙖𝙩𝙖 𝙏𝙮𝙥𝙚𝙨

- `Byte` - 8-bit value.
- `Word` - 16-bit value.
- `Doubleword (Dword)` - 32-bit value.
- `Quadword (Qword)` - 64-bit value.
- `Tword` - 80-bit value, often for extended precision/FPU.
- `Oword / XMMword` - 128-bit value.
- `YMMword` - 256-bit value.
- `ZMMword` - 512-bit value.
- `Nibble` - 4-bit half-byte.
- `Bit` - Single binary digit, `0` or `1`.
- `Signed Integer` - Integer interpreted with a sign bit.
- `Unsigned Integer` - Integer interpreted without a sign bit.
- `Character (Char)` - ASCII/byte character value.
- `String` - Sequence of bytes/characters, often null-terminated or length-based.
- `Address / Pointer` - Memory location.
- `Offset` - Distance/address relative to a base.
- `Boolean (Bool)` - Typically represented as `0 = false`, nonzero = true.
- `Floating Point` - Stored in `x87`, `SSE`, or `AVX` registers/memory formats.
- `BCD` - Binary-coded decimal (legacy/specialized).
- `Packed Data` - Multiple smaller values packed into one register.
- `Arrays` - Contiguous memory locations of same-sized elements.
- `Structures` - Memory layout containing multiple named fields.
- `Unions` - Multiple interpretations of same storage region.
- `Stack Data` - `LIFO` memory region used for calls, locals, saved state.
- `Heap Data` - Dynamically allocated memory managed by runtime/OS/library.
- `Immediate Values` - Constant values encoded directly in instructions.
- `Registers` - Small, fast storage locations inside the CPU.
- `Null` - Usually represented as `0` when used as a pointer/address sentinel.
- `Labels` - Symbolic names for addresses in code or data.

# 𝗥𝗲𝘀𝗲𝗿𝘃𝗲𝗱 𝗪𝗼𝗿𝗱𝘀/𝗞𝗲𝘆𝘄𝗼𝗿𝗱𝘀

- `section` - Declares a program section.
- `segment` - Alternative section declaration in some syntaxes.
- `global` - Exports a symbol for the linker.
- `extern` - Declares an external symbol.
- `bits` - Sets the assembly mode width in `NASM`.
- `org` - Sets origin address in certain formats.
- `equ` - Defines a symbolic constant.
- `db` - Define byte data.
- `dw` - Define word data.
- `dd` - Define doubleword data.
- `dq` - Define quadword data.
- `dt` - Define ten-byte data in some assemblers.
- `resb` - Reserve bytes.
- `resw` - Reserve words.
- `resd` - Reserve doublewords.
- `resq` - Reserve quadwords.
- `times` - Repeat an initializer or reservation.
- `label` - Symbolic address marker.
- `macro / %macro` - Defines a macro.
- `endm / %endmacro` - Ends a macro definition.
- `proc` - Declares a procedure in `MASM`-style assembly.
- `endp` - Ends a procedure in `MASM`-style assembly.
- `byte` - Size specifier.
- `word` - Size specifier.
- `dword` - Size specifier.
- `qword` - Size specifier.
- `ptr` - Pointer-size qualifier in Intel syntax.
- `offset` - Address/immediate offset operator in some syntaxes.
- `far / near` - Call/jump/address qualifiers in some modes/syntaxes.

# 𝗢𝗽𝗲𝗿𝗮𝘁𝗼𝗿𝘀

### Logical Operators

- `;` - Single-line comment in many Assembly syntaxes.
- `#` - Comment in some Assembly dialects or preprocessors.
- `+` - Addition / address arithmetic.
- `-` - Subtraction / negation.
- `*` - Multiplication in expressions or scale factor in addressing.
- `/` - Division in expressions (assembler-time) in some syntaxes.
- `%` - Modulus/operator or macro syntax prefix in some assemblers.
- `=` - Assignment/equate in some assembler syntaxes.
- `== != < > <= >=` - Expression comparison at assembly time in some macro/preprocessor contexts.
- `&` - Bitwise AND in assembler expressions.
- `|` - Bitwise OR in assembler expressions.
- `^` - Bitwise XOR in assembler expressions.
- `~` - Bitwise NOT in assembler expressions.
- `<<` - Left shift in assembler expressions.
- `>>` - Right shift in assembler expressions.
- `[]` - Memory dereference/addressing in Intel syntax, for example `[rax]`, `[rbp-8]`, `[array+rcx*4]`.
- `()` - Grouping in expressions, mostly in `AT&T` syntax/macros/preprocessors.
- `:` - Label terminator and segment/offset notation in some syntaxes.
- `,` - Operand separator.
- `$` - Current location counter or immediate prefix in some syntaxes.
- `@` - Local symbol/operator prefix in some assemblers.
- `?` - Uninitialized data placeholder in some `MASM`-style declarations.

# 𝗗𝗶𝗿𝗲𝗰𝘁𝗼𝗿𝘆 𝗧𝗿𝗮𝘃𝗲𝗿𝘀𝗮𝗹

- `.` - Current directory.
- `..` - Parent directory.
- `/` - Root directory on Unix-like systems.
- `\` - Directory separator in Windows paths.
- `./program.asm` - Relative file path.
- `/home/user/program.asm` - Absolute Unix path.
- `C:\asm\program.asm` - Absolute Windows path string literal.
Note: Directory traversal is not an Assembly language feature itself, but assemblers use file paths for source files, includes, object files, and linker output.

# 𝗤𝘂𝗼𝘁𝗶𝗻𝗴

- `'A'` - Character literal in many assemblers.
- `"Hello"` - String literal in many assemblers.
- `\` - Escape character in assemblers that support C-style escapes.
- `'\n' / 10` - Newline may be written as escape or raw byte value depending on assembler.
- `'\0' / 0` - Null terminator.
- `` `text` `` - String literal style in some assemblers/preprocessors.
Note: Literal syntax varies by assembler (`NASM`, `MASM`, `GAS`, `FASM`, etc.). Some assemblers treat strings very differently, especially around escape sequences.

# 𝗥𝗲𝗱𝗶𝗿𝗲𝗰𝘁𝗶𝗼𝗻

- `>` - Shell redirection of assembler/linker output to a file.
- `>>` - Shell append redirection.
- `<` - Shell redirection of input from a file.
- `|` - Shell pipeline.
Note: Redirection is typically handled by the shell, not by Assembly itself.

### Assembly-Adjacent Examples

- `%include "file.inc"` - Include another source file at assembly time.

# 𝗚𝗿𝗼𝘂𝗽𝗶𝗻𝗴

- `{}` - Used in some macro/preprocessor syntaxes, not universal in Assembly.
- `()` - Expression grouping in some syntaxes/preprocessors.
- `[]` - Memory dereference/addressing in Intel syntax.
- `label:` - Groups a sequence of instructions/data under a symbolic address.
- `section .text / .data / .bss` - Groups code, initialized data, and uninitialized data.
Note: Grouping rules vary heavily by assembler syntax. Intel syntax and `AT&T` syntax differ significantly.

# 𝗚𝗹𝗼𝗯𝘀/𝗪𝗶𝗹𝗱𝗰𝗮𝗿𝗱𝘀

- `?` - Wildcard in shells/file matching outside Assembly; placeholder for uninitialized data in some `MASM`-style syntax.
- `*` - Current location counter in some assemblers/syntaxes, multiplication scale factor, or shell wildcard outside Assembly.
- `[...]` - Memory reference/addressing in Intel syntax.
Note: File globbing is shell behavior, not an Assembly language feature. Inside Assembly, these symbols usually have addressing, declaration, or expression meanings instead.

# 𝗘𝘅𝗮𝗺𝗽𝗹𝗲𝘀

## 𝗚𝗲𝗻𝗲𝗿𝗮𝗹 𝗧𝘆𝗽𝗲𝘀

### 𝗩𝗮𝗿𝗶𝗮𝗯𝗹𝗲 (𝗩𝗮𝗿)

- `; Declare initialized and uninitialized storage.`
- `section .data`
- `number  dd 10`
- `grade   db 'A'`
- `price   dq 19`
- `section .bss`
- `buffer  resb 64`

### 𝗜𝗻𝘁𝗲𝗴𝗲𝗿 (𝗜𝗻𝘁)

- `; Declare integers of different sizes.`
- `section .data`
- `smallVal    db 10`
- `wordVal     dw 1000`
- `intVal      dd 100000`
- `bigVal      dq 9000000000`

### 𝗙𝗹𝗼𝗮𝘁

- `; Floating-point constants are often stored in memory.`
- `section .data`
- `f32     dd 10.5`
- `f64     dq 20.12`
- `; Actual floating-point arithmetic may use x87 FPU, SSE, or AVX instructions depending on platform and assembler.`

### 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻 (𝗙𝘂𝗻𝗰)

- `; NASM x86-64 example.`
- `section .text`
- `global add_numbers`
- `add_numbers:`
- `    mov rax, rdi`
- `    add rax, rsi`
- `    ret`

## 𝗖𝗼𝗻𝗱𝗶𝘁𝗶𝗼𝗻𝗮𝗹 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁𝘀

### 𝗕𝗼𝗼𝗹𝗲𝗮𝗻 (𝗕𝗼𝗼𝗹)

- `; Booleans are usually represented as 0 = false, nonzero = true.`
- `section .data`
- `flag    db 1`
- `section .text`
- `    cmp byte [flag], 0`
- `    je false_label`
- `    ; true path`
- `false_label:`

### 𝗜𝗳 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁

- `; If rax > rbx, jump to greater_label.`
- `    cmp rax, rbx`
- `    jg greater_label`

### 𝗜𝗳/𝗘𝗹𝘀𝗲 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁

- `; If rax == rbx then equal_path else not_equal_path.`
- `    cmp rax, rbx`
- `    je equal_path`
- `    jmp not_equal_path`
- `equal_path:`
- `    ; code for equal case`
- `    jmp done`
- `not_equal_path:`
- `    ; code for else case`
- `done:`

## 𝗟𝗼𝗼𝗽𝘀

### 𝗙𝗼𝗿 𝗟𝗼𝗼𝗽

- `; Count from 1 to 5 using rcx.`
- `    mov rcx, 1`
- `for_loop:`
- `    ; loop body here`
- `    inc rcx`
- `    cmp rcx, 6`
- `    jl for_loop`

### 𝗪𝗵𝗶𝗹𝗲 𝗟𝗼𝗼𝗽

- `; Loop while rcx <= 5.`
- `    mov rcx, 1`
- `while_loop:`
- `    cmp rcx, 5`
- `    jg while_done`
- `    ; loop body here`
- `    inc rcx`
- `    jmp while_loop`
- `while_done:`

## 𝗔𝗿𝗿𝗮𝘆𝘀

### 𝗜𝗻𝗱𝗲𝘅𝗲𝗱 𝗔𝗿𝗿𝗮𝘆

- `; Declare an array and access elements by index.`
- `section .data`
- `numbers dd 10, 20, 30`
- `section .text`
- `    mov eax, [numbers]`
- `    mov eax, [numbers + 4]`
- `    mov eax, [numbers + rdx*4]`

### 𝗔𝘀𝘀𝗼𝗰𝗶𝗮𝘁𝗶𝘃𝗲 𝗔𝗿𝗿𝗮𝘆

- `; Assembly does not have true associative arrays built into the language.`
- `; A common substitute is a lookup table, parallel arrays, or a manually implemented hash table/tree structure.`
- `section .data`
- `key1    db "name",0`
- `val1    db "John Doe",0`
- `key2    db "email",0`
- `val2    db "john@example.com",0`

## 𝗢𝘁𝗵𝗲𝗿

### 𝗖𝗮𝘀𝗲 𝗦𝘁𝗮𝘁𝗲𝗺𝗲𝗻𝘁

- `; Switch-like behavior is commonly implemented with comparisons and jumps.`
- `    cmp eax, 1`
- `    je case_one`
- `    cmp eax, 2`
- `    je case_two`
- `    cmp eax, 3`
- `    je case_three`
- `    jmp default_case`
- `case_one:`
- `    ; code`
- `    jmp end_case`
- `case_two:`
- `    ; code`
- `    jmp end_case`
- `case_three:`
- `    ; code`
- `    jmp end_case`
- `default_case:`
- `    ; default code`
- `end_case:`

### 𝗢𝗯𝗷𝗲𝗰𝘁

- `; Assembly does not have objects in the OOP sense built into the language.`
- `; The closest equivalent is usually a manually defined structure in memory.`
- `section .data`
- `point:`
- `    dd 10`
- `    dd 20`
- `    mov eax, [point]`
- `    mov ebx, [point + 4]`