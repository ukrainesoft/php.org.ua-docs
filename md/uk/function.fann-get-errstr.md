---
navigation:
  - function.fann-get-errno.md: « fann\_get\_errno
  - function.fann-get-layer-array.md: fann\_get\_layer\_array »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_errstr
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_errstr

(PECL fann >= 1.0.0)

fann\_get\_errstr — Повертає останній рядок помилки

### Опис

```methodsynopsis
fann_get_errstr(resource $errdat): string
```

Повертає останній рядок помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Последняя строка ошибки или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_reset\_errstr()](function.fann-reset-errstr.md) \- Скидає останній рядок помилки
-   [fann\_get\_errno()](function.fann-get-errno.md) \- Повертає останній номер помилки
