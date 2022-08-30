Створює виняток

-   [« ErrorException](class.errorexception.md)
    
-   [ErrorException::getSeverity »](errorexception.getseverity.md)
    
-   [PHP Manual](index.md)
    
-   [ErrorException](class.errorexception.md)
    
-   Створює виняток
    

# ErrorException::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

ErrorException::construct — Створює виняток

### Опис

public **ErrorException::construct**  
string `$message` = "",  
int `$code`  
int `$severity` **`E_ERROR`**  
?string `$filename` **`null`**  
?int `$line` **`null`**  
[Throwable](class.throwable.md) `$previous` **`null`**

Створює виняток.

### Список параметрів

`message`

Текст виключення.

`code`

Код виключення.

`severity`

Рівень серйозності виключення.

> **Зауваження**
> 
> У той час, як рівень серйозності може бути будь-яким цілим числом (int), передбачається, що для її вказівки будуть використані константи [ошибок](errorfunc.constants.md)

`filename`

Ім'я файлу, де викликано виняток.

`line`

Номер рядка, де викликано виняток.

`previous`

Попередній виняток. Використовується для створення ланцюжка винятків.

### список змін

| Версия | Описание                                                                                                                                     |
|--------|----------------------------------------------------------------------------------------------------------------------------------------------|
|        | `filename` і `line` тепер допускають значення null. Раніше їх значеннями за промовчанням були **`__FILE__`** і \*\*`__LINE__`\*\*відповідно. |