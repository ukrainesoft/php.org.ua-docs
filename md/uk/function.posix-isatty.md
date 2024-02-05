---
navigation:
  - function.posix-initgroups.md: « posix\_initgroups
  - function.posix-kill.md: posix\_kill »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_isatty
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_isatty

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_isatty — Визначає, чи є файловий дескриптор інтерактивним терміналом.

### Опис

```methodsynopsis
posix_isatty(resource|int $file_descriptor): bool
```

Визначає, чи є файловий дескриптор. `file_descriptor` посиланням на валідний термінал.

### Список параметрів

`file_descriptor`

Файловий дескриптор, який очікується у вигляді ресурсу або ресурсу або цілого числа int. Під int мається на увазі файловий дескриптор, який можна передати безпосередньо до базового системного виклику.

### Значення, що повертаються

Повертає **`true`** якщо `file_descriptor` є відкритим файловим дескриптором, пов'язаним з терміналом та **`false`** в інших випадках.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Помилки рівня **`E_WARNING`** тепер видаються при перетворення цілих чисел відповідно до звичайної семантикою перетворення типів PHP. |

### Дивіться також

-   [posix\_ttyname()](function.posix-ttyname.md) \- Визначає ім'я термінального пристрою
-   [stream\_isatty()](function.stream-isatty.md) \- Перевіряє, чи є потік TTY
