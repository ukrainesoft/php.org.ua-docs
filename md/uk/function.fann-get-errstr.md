---
navigation:
  - function.fann-get-errno.html: « fanngeterrno
  - function.fann-get-layer-array.html: fanngetlayerarray »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
title: fanngeterrstr
---
# fanngeterrstr

(PECL fann> = 1.0.0)

fanngeterrstr — Повертає останній рядок помилки

### Опис

```methodsynopsis
fann_get_errstr(resource $errdat): string
```

Повертає останній рядок помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Останній рядок помилки або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannreseterrstr()](function.fann-reset-errstr.html) - Скидає останній рядок помилки
-   [fanngeterrno()](function.fann-get-errno.html) - Повертає останній номер помилки
