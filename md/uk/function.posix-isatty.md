---
navigation:
  - function.posix-initgroups.html: « posixinitgroups
  - function.posix-kill.html: posixkill »
  - index.md: PHP Manual
  - ref.posix.md: POSIX Функции
title: posixisatty
---
# posixisatty

(PHP 4, PHP 5, PHP 7, PHP 8)

posixisatty — Визначає, чи є файловий дескриптор інтерактивним терміналом.

### Опис

```methodsynopsis
posix_isatty(resource|int $file_descriptor): bool
```

Визначає, чи є файловий дескриптор. `file_descriptor` посиланням на валідний термінал.

### Список параметрів

`fd`

Файловий дескриптор, який очікується у вигляді ресурсу ресурсу або цілого числа int. Під int мається на увазі файловий дескриптор, який можна передати безпосередньо до базового системного виклику.

У більшості випадків вам потрібно буде передавати файловий ресурс.

### Значення, що повертаються

Повертає **`true`** якщо `file_descriptor` є відкритим файловим дескриптором, пов'язаним з терміналом та **`false`** в інших випадках.

### Дивіться також

-   [posixttyname()](function.posix-ttyname.html) - Визначає ім'я термінального пристрою
-   [streamisatty()](function.stream-isatty.html) - Перевіряє, чи є потік TTY
