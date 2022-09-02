---
navigation:
  - function.set-error-handler.md: « seterrorhandler
  - function.trigger-error.md: triggererror »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функции обработки ошибок
title: setexceptionhandler
---
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

Функція, що викликається у разі неперехопленого винятку. Ця функція-обробник повинна приймати один параметр, яким буде об'єкт викинутого виключення [Throwable](class.throwable.md). І [Error](class.error.md) і [Exception](class.exception.md) реалізують інтерфейс [Throwable](class.throwable.md). Сигнатура оброблювача:

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

-   [restoreexceptionhandler()](function.restore-exception-handler.md) - Відновлює попередній обробник винятків
-   [restoreerrorhandler()](function.restore-error-handler.md) - Відновлює попередній обробник помилок
-   [errorreporting()](function.error-reporting.md) - Задає, які помилки PHP потраплять у звіт
-   [Исключения PHP 5](language.exceptions.md)
