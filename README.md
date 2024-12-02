```asm
section .data
    message db 'Welcome', 0
    caption db 'gL49R6YvdXQ1U6', 0

section .text
    global _start
    extern MessageBoxA, InitiateSystemShutdown, GetModuleHandleA

_start:
    push 0
    call GetModuleHandleA

    push 0
    push caption
    push message
    push 0
    call MessageBoxA

    push 0
    push 0
    push 0
    call InitiateSystemShutdown
```
