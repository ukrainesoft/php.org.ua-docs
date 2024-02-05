---
navigation:
  - function.fann-get-connection-rate.md: « fann\_get\_connection\_rate
  - function.fann-get-errstr.md: fann\_get\_errstr »
  - index.md: PHP Manual
  - ref.fann.md: Функції Fann
title: fann\_get\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# fann\_get\_errno

(PECL fann >= 1.0.0)

fann\_get\_errno — Повертає останній номер помилки

### Опис

```methodsynopsis
fann_get_errno(resource $errdat): int
```

Повертає останній номер помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Номер помилки або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [fann\_reset\_errno()](function.fann-reset-errno.md) \- скидає номер останньої помилки
-   [fann\_get\_errstr()](function.fann-get-errstr.md) \- Повертає останній рядок помилки
