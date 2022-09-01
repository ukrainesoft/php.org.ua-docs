---
navigation:
  - class.error.html: « Error
  - error.getmessage.html: 'Error::getMessage »'
  - index.html: PHP Manual
  - class.error.html: Error
title: 'Error::construct'
---
# Error::construct

(PHP 7, PHP 8)

Error::construct — Створює об'єкт класу Error

### Опис

public **Error::construct**(string `$message` = "", int `$code` [Throwable](class.throwable.html) `$previous` **`null`**

Створює об'єкт класу Error.

### Список параметрів

`message`

Повідомлення про помилку.

`code`

Код помилки.

`previous`

Попередній об'єкт, що реалізує throwable інтерфейс, використовується для створення ланцюжка винятків.

### Примітки

> **Зауваження**
> 
> Значення `message` *НЕ* є безпечним для бінарних даних, тобто в тексті повідомлення не можна використовувати символ із кодом
