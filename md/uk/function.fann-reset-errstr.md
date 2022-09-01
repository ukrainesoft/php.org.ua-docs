---
navigation:
  - function.fann-reset-errno.html: « fannreseterrno
  - function.fann-reset-mse.html: fannresetMSE »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fannreseterrstr
---
# fannreseterrstr

(PECL fann> = 1.0.0)

fannreseterrstr — Скидає останній рядок помилки

### Опис

```methodsynopsis
fann_reset_errstr(resource $errdat): void
```

Скидає останній рядок помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Не повертає жодного значення.

### Дивіться також

-   [fanngeterrstr()](function.fann-get-errstr.html) - Повертає останній рядок помилки
-   [fannreseterrno()](function.fann-reset-errno.html) - скидає номер останньої помилки
