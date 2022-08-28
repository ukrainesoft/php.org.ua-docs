Отримати код останньої помилки

-   [« Transliterator::createInverse](transliterator.createinverse.html)
    
-   [Transliterator::getErrorMessage »](transliterator.geterrormessage.html)
    
-   [PHP Manual](index.html)
    
-   [Transliterator](class.transliterator.html)
    
-   Отримати код останньої помилки
    

# Transliterator::getErrorCode

# transliteratorgeterrorcode

(PHP 5 >= 5.4.0, PHP 7, PHP 8, PECL intl >= 2.0.0)

Transliterator::getErrorCode -- transliteratorgeterrorcode — Отримати код останньої помилки

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public Transliterator::getErrorCode(): int|false
```

Процедурний стиль

```methodsynopsis
transliterator_get_error_code(Transliterator $transliterator): int|false
```

Повертає код останньої помилки.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`transliterator`

### Значення, що повертаються

Код помилки або **`false`**якщо помилок не було або якщо отримати його не вдалося.

### Дивіться також

-   [Transliterator::getErrorMessage()](transliterator.geterrormessage.html) - Отримати останнє повідомлення про помилку
-   [Transliterator::listIDs()](transliterator.listids.html) - Отримати ідентифікатори транслітератора