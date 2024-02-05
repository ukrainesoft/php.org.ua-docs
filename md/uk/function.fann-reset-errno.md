---
navigation:
  - function.fann-read-train-from-file.md: « fann\_read\_train\_from\_file
  - function.fann-reset-errstr.md: fann\_reset\_errstr »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_reset\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_reset\_errno

(PECL fann >= 1.0.0)

fann\_reset\_errno — Скидає номер останньої помилки

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

-   [fann\_get\_errno()](function.fann-get-errno.md) \- Повертає останній номер помилки
-   [fann\_reset\_errstr()](function.fann-reset-errstr.md) \- Скидає останній рядок помилки
