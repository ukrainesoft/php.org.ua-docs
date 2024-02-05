---
navigation:
  - class.error.md: « Error
  - error.getmessage.md: 'Error::getMessage »'
  - index.md: PHP Manual
  - class.error.md: Error
title: 'Error::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Error::\_\_construct

(PHP 7, PHP 8)

Error::\_\_construct — Створює об'єкт класу Error

### Опис

public **Error::\_\_construct**(string`$message` = "", int `$code` [Throwable](class.throwable.md) `$previous` **`null`**) .

Створює об'єкт класу Error.

### Список параметрів

`message`

Повідомлення про помилку.

`code`

Код помилки.

`previous`

Попередній об'єкт, що реалізує throwable інтерфейс, використовується для створення ланцюжка винятків.

### Примітки

> **Зауваження** :
> 
> Значение`message` *НЕ* є безпечним для бінарних даних, тобто в тексті повідомлення не можна використовувати символ із кодом \\0.
