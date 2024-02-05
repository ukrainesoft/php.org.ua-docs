---
navigation:
  - function.fann-reset-errno.md: « fann\_reset\_errno
  - function.fann-reset-mse.md: fann\_reset\_MSE »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_reset\_errstr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_reset\_errstr

(PECL fann >= 1.0.0)

fann\_reset\_errstr — Скидає останній рядок помилки

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

-   [fann\_get\_errstr()](function.fann-get-errstr.md) \- Повертає останній рядок помилки
-   [fann\_reset\_errno()](function.fann-reset-errno.md) \- скидає номер останньої помилки
