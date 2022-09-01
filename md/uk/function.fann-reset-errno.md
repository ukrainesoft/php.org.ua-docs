---
navigation:
  - function.fann-read-train-from-file.html: « fannreadtrainfromfile
  - function.fann-reset-errstr.html: fannreseterrstr »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannreseterrno
---
# fannreseterrno

(PECL fann> = 1.0.0)

fannreseterrno — Скидає номер останньої помилки

### Опис

```methodsynopsis
fann_reset_errno(resource $errdat): void
```

Скидає номер останньої помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Не повертає жодного значення.

### Дивіться також

-   [fanngeterrno()](function.fann-get-errno.html) - Повертає останній номер помилки
-   [fannreseterrstr()](function.fann-reset-errstr.html) - Скидає останній рядок помилки
