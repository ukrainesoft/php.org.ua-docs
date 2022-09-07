---
navigation:
  - function.fann-get-connection-rate.md: « fanngetconnectionrate
  - function.fann-get-errstr.md: fanngeterrstr »
  - index.md: PHP Manual
  - ref.fann.md: Функции Fann
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

-   [fannreseterrno()](function.fann-reset-errno.md) - скидає номер останньої помилки
-   [fanngeterrstr()](function.fann-get-errstr.md) - Повертає останній рядок помилки
