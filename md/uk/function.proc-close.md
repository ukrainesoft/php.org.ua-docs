---
navigation:
  - function.passthru.md: « passthru
  - function.proc-get-status.md: procgetstatus »
  - index.md: PHP Manual
  - ref.exec.md: Функции запуска программ
title: procclose
---
# procclose

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

procclose — Завершити процес, відкритий [procopen()](function.proc-open.md) та повернути код повернення цього процесу

### Опис

```methodsynopsis
proc_close(resource $process): int
```

Функція **procclose()** схожа на функцію [pclose()](function.pclose.md), за винятком того, що вона працює тільки з процесами, відкритими за допомогою функції [procopen()](function.proc-open.md). Функція **procclose()** очікує завершення процесу та повертає його код повернення. Відкриті канали для цього процесу закриваються під час виклику цієї функції, щоб уникнути повної зупинки програми: дочірній процес не зможе завершитись, якщо є відкриті канали.

### Список параметрів

`process`

Дескриптор типу resource, відкритий за допомогою [procopen()](function.proc-open.md), що буде закрито.

### Значення, що повертаються

Повертає код завершення процесу, який було запущено. У разі помилки повертається `-1`

> **Зауваження**
> 
> Якщо PHP зібрано з опцією --enable-sigchild, значення цієї функції, що повертається, не визначено.
