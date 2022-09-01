---
navigation:
  - function.ob-get-length.html: « obgetlength
  - function.ob-get-status.html: проgetstatus »
  - index.html: PHP Manual
  - ref.outcontrol.html: Функції контролю виведення
title: проgetlevel
---
# проgetlevel

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

проgetlevel - Повертає рівень вкладеності механізму буферизації виводу

### Опис

```methodsynopsis
ob_get_level(): int
```

Поверне рівень вкладеності механізму буферизації виведення.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає рівень вкладеності обробників буферизації виводу або 0, якщо не активна буферизація.

### Дивіться також

-   [проstart()](function.ob-start.html) - Включення буферизації виводу
-   [проgetcontents()](function.ob-get-contents.html) - Повертає вміст буфера виводу
