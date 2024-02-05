---
navigation:
  - function.set-error-handler.md: « set\_error\_handler
  - function.trigger-error.md: trigger\_error »
  - index.md: PHP Manual
  - ref.errorfunc.md: Функції обробки помилок
title: set\_exception\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# set\_exception\_handler

(PHP 5, PHP 7, PHP 8)

set\_exception\_handler — Задає користувальницький обробник винятків

### Опис

```methodsynopsis
set_exception_handler(?callable $callback): ?callable
```

Задає стандартний обробник для випадків, коли виняток викинуто поза блоком try/catch. Після виклику `callback` виконання буде зупинено.

### Список параметрів

`callback`

Функція, що викликається у разі неперехопленого винятку. Ця функція-обробник повинна приймати один параметр, яким буде об'єкт викинутого виключення [Throwable](class.throwable.md). [Error](class.error.md) і [Exception](class.exception.md) реалізують інтерфейс [Throwable](class.throwable.md)Сигнатура обработчика:

```methodsynopsis
handler(Throwable $ex): void
```

Як цей аргумент можна передати **`null`**. У цьому випадку обробник повернеться до свого первісного стану.

### Значення, що повертаються

Повертає раніше певний обробник винятків або **`null`** у разі помилки. Якщо попередніх обробників не було визначено, то також повертається **`null`**

### Приклади

**Пример #1 Пример использования**set\_exception\_handler()\*\*\*\*

```php
<?php
function exception_handler(Throwable $exception) {
  echo "Неперехваченное исключение: " , $exception->getMessage(), "\n";
}

set_exception_handler('exception_handler');

throw new Exception('Неперехваченное исключение');
echo "Не выполнено\n";
?>
```

### Дивіться також

-   [restore\_exception\_handler()](function.restore-exception-handler.md) \- Відновлює попередній обробник винятків
-   [restore\_error\_handler()](function.restore-error-handler.md) \- Відновлює попередній обробник помилок
-   [error\_reporting()](function.error-reporting.md) \- Встановлює, які помилки PHP потраплять у звіт
-   [Винятки](language.exceptions.md)
