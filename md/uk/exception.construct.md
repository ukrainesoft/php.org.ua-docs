---
navigation:
  - class.exception.md: « Exception
  - exception.getmessage.md: 'Exception::getMessage »'
  - index.md: PHP Manual
  - class.exception.md: Exception
title: 'Exception::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Exception::\_\_construct

(PHP 5, PHP 7, PHP 8)

Exception::\_\_construct — Створити виняток

### Опис

public**Exception::\_\_construct**(string`$message` = "", int `$code` [Throwable](class.throwable.md) `$previous` **`null`**) .

Створює виняток.

### Список параметрів

`message`

Текст повідомлення.

`code`

Код виключення.

`previous`

Попередній виняток. Використовується для створення ланцюжка винятків.

> **Зауваження**: Виклик конструктора Exception з його підкласу, ігнорує аргументи за замовчуванням, якщо властивості $code і $message вже встановлені.

### Примітки

> **Зауваження** :
> 
> Параметр`message` *не* є бінарно-безпечним.
