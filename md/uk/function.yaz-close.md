---
navigation:
  - function.yaz-ccl-parse.md: « yaz\_ccl\_parse
  - function.yaz-connect.md: yaz\_connect »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_close

(PHP 4 >= 4.0.1, PECL yaz >= 0.9.0)

yaz\_close — Закриває з'єднання YAZ

### Опис

```methodsynopsis
yaz_close(resource $id): bool
```

Закриває з'єднання, яке визначається параметром `id`

> **Зауваження** :
> 
> Функція закриє лише непостійні з'єднання, відкриті функцією [yaz\_connect()](function.yaz-connect.md)с параметром`persistent` встановленим у значення **`false`**

### Список параметрів

`id`

Дескриптор з'єднання, що повертається [yaz\_connect()](function.yaz-connect.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [yaz\_connect()](function.yaz-connect.md) \- Готує з'єднання із сервером Z39.50
