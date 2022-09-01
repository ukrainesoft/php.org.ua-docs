---
navigation:
  - function.yaz-ccl-parse.html: « yazcclparse
  - function.yaz-connect.html: yazconnect »
  - index.html: PHP Manual
  - ref.yaz.html: Функции YAZ
title: yazclose
---
# yazclose

(PHP 4> = 4.0.1, PECL yaz> = 0.9.0)

yazclose — Закриває з'єднання YAZ

### Опис

```methodsynopsis
yaz_close(resource $id): bool
```

Закриває з'єднання, яке визначається параметром `id`

> **Зауваження**
> 
> Функція закриє лише непостійні з'єднання, відкриті функцією [yazconnect()](function.yaz-connect.md) з параметром `persistent` встановленим у значення **`false`**

### Список параметрів

`id`

Дескриптор з'єднання, що повертається [yazconnect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [yazconnect()](function.yaz-connect.md) - Готує з'єднання із сервером Z39.50
