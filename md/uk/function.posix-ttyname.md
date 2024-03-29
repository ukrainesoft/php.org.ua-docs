---
navigation:
  - function.posix-times.md: « posix\_times
  - function.posix-uname.md: posix\_uname »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функції
title: posix\_ttyname
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# posix\_ttyname

(PHP 4, PHP 5, PHP 7, PHP 8)

posix\_ttyname — Визначає ім'я термінального пристрою

### Опис

```methodsynopsis
posix_ttyname(resource|int $file_descriptor): string|false
```

Повертає string, що містить абсолютний шлях до поточного термінального пристрою, який відкрито та пов'язано з файловим дескриптором `file_descriptor`

### Список параметрів

`file_descriptor`

Файловий дескриптор, який очікується у вигляді ресурсу або ресурсу або цілого числа int. Під int мається на увазі файловий дескриптор, який можна передати безпосередньо до базового системного виклику.

### Значення, що повертаються

У разі успішного виконання повертає рядок (string), який містить абсолютний шлях до терміналу, пов'язаного з файловим дескриптором `file_descriptor`. У разі невдачі повертає **`false`**

### Помилки

При неприпустимих цілих значеннях параметра `file_descriptor` видається помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Помилки рівня **`E_WARNING`** тепер видаються при перетворення цілих чисел відповідно до звичайної семантикою перетворення типів PHP. |
| 8.3.0 | При неприпустимих цілих значеннях параметра `file_descriptor` тепер видається помилка рівня **`E_WARNING`** |

### Дивіться також

-   [posix\_isatty()](function.posix-isatty.md) \- Чи визначає файловий дескриптор інтерактивним терміналом
-   [stream\_isatty()](function.stream-isatty.md) \- Перевіряє, чи є потік TTY
