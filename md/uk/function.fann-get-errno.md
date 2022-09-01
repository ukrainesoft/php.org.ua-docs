---
navigation:
  - function.fann-get-connection-rate.html: « fanngetconnectionrate
  - function.fann-get-errstr.html: fanngeterrstr »
  - index.html: PHP Manual
  - ref.fann.html: Функции Fann
title: fanngeterrno
---
# fanngeterrno

(PECL fann> = 1.0.0)

fanngeterrno — Повертає останній номер помилки

### Опис

```methodsynopsis
fann_get_errno(resource $errdat): int
```

Повертає останній номер помилки.

### Список параметрів

`errdat`

Або ресурс (resource) нейронної мережі, або ресурс (resource) навчальних даних нейронної мережі.

### Значення, що повертаються

Номер помилки або **`false`** у разі виникнення помилки.

### Дивіться також

-   [fannreseterrno()](function.fann-reset-errno.html) - скидає номер останньої помилки
-   [fanngeterrstr()](function.fann-get-errstr.html) - Повертає останній рядок помилки
