---
navigation:
  - class.errorexception.md: « ErrorException
  - errorexception.getseverity.md: 'ErrorException::getSeverity »'
  - index.md: PHP Manual
  - class.errorexception.md: ErrorException
title: 'ErrorException::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ErrorException::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

ErrorException::\_\_construct — Створює виняток

### Опис

public **ErrorException::\_\_construct**  
string`$message` = "",  
int`$code`  
int`$severity` **`E_ERROR`**,  
?string`$filename` **`null`**,  
?int`$line` **`null`**,  
?[Throwable](class.throwable.md) `$previous` **`null`**  
) .

Створює виняток.

### Список параметрів

`message`

Текст виключення.

`code`

Код виключення.

`severity`

Рівень серйозності виключення.

> **Зауваження** :
> 
> У той час, як рівень серйозності може бути будь-яким цілим числом (int), передбачається, що для її вказівки будуть використані константи [помилок](errorfunc.constants.md)

`filename`

Ім'я файлу, де викликано виняток.

`line`

Номер рядка, де викликано виняток.

`previous`

Попередній виняток. Використовується для створення ланцюжка винятків.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `filename`и`line` тепер допускають значення null. Раніше їх значеннями за промовчанням були \*\*`__FILE__`** і **`__LINE__`\*\*відповідно. |
