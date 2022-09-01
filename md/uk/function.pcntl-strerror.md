---
navigation:
  - function.pcntl-sigwaitinfo.html: pcntlsigwaitinfo
  - function.pcntl-unshare.html: pcntlunshare »
  - index.html: PHP Manual
  - ref.pcntl.html: Функції PCNTL
title: pcntlstrerror
---
# pcntlstrerror

(PHP 5> = 5.3.4, PHP 7, PHP 8)

pcntlstrerror — Отримати текст помилки за її кодом

### Опис

```methodsynopsis
pcntl_strerror(int $error_code): string
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`error_code`

### Значення, що повертаються

Повертає опис помилки.

### Дивіться також

-   [pcntlgetlasterror()](function.pcntl-get-last-error.md) - Отримати код останньої помилки, що виникла в pcntl-функції
