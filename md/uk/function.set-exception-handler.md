Задає користувальницький обробник винятків

-   [« seterrorhandler](function.set-error-handler.html)
    
-   [triggererror »](function.trigger-error.html)
    
-   [PHP Manual](index.html)
    
-   [Функции обработки ошибок](ref.errorfunc.html)
    
-   Задає користувальницький обробник винятків
    

# setexceptionhandler

(PHP 5, PHP 7, PHP 8)

setexceptionhandler — Задає користувальницький обробник винятків

### Опис

```methodsynopsis
set_exception_handler(?callable $callback): ?callable
```

Задає стандартний обробник для випадків, коли виняток викинуто поза блоком try/catch. Після виклику `callback` виконання буде зупинено.

### Список параметрів

`callback`

Функція, що викликається у разі неперехопленого винятку. Ця функція-обробник повинна приймати один параметр, яким буде об'єкт викинутого виключення [Throwable](class.throwable.html). І [Error](class.error.html) і [Exception](class.exception.html) реалізують інтерфейс [Throwable](class.throwable.html). Сигнатура оброблювача:

```methodsynopsis
handler(Throwable $ex): void
```

Як цей аргумент можна передати **`null`**. У цьому випадку обробник повернеться до свого первісного стану.

### Значення, що повертаються

Повертає раніше певний обробник винятків або **`null`** у разі помилки. Якщо попередніх обробників не було визначено, то також повертається **`null`**

### Приклади

**Приклад #1 Приклад використання **setexceptionhandler()****

```php
<?php
function exception_handler(Throwable $exception) {
  echo "Неперехваченное исключение: " , $exception->getMessage(), "\n";
}

set_exception_handler('exception_handler');

throw new Exception('Неперехваченное исключение');
echo "Не выполнено\n";
?>
```

### Дивіться також

-   [restoreexceptionhandler()](function.restore-exception-handler.html) - Відновлює попередній обробник винятків
-   [restoreerrorhandler()](function.restore-error-handler.html) - Відновлює попередній обробник помилок
-   [errorreporting()](function.error-reporting.html) - Задає, які помилки PHP потраплять у звіт
-   [Исключения PHP 5](language.exceptions.html)