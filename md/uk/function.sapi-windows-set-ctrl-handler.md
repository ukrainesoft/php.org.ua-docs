---
navigation:
  - function.sapi-windows-generate-ctrl-event.md: « sapi\_windows\_generate\_ctrl\_event
  - function.sapi-windows-vt100-support.md: sapi\_windows\_vt100\_support »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapi\_windows\_set\_ctrl\_handler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sapi\_windows\_set\_ctrl\_handler

(PHP 7 >= 7.4.0, PHP 8)

sapi\_windows\_set\_ctrl\_handler — Встановити або видалити обробник події CTRL

### Опис

```methodsynopsis
sapi_windows_set_ctrl_handler(?callable $handler, bool $add = true): bool
```

Встановлює або видаляє обробник події `CTRL`, який дозволить процесам Windows CLI перехоплювати чи ігнорувати події `CTRL+C`и`CTRL+BREAK`. Зверніть увагу, що в багатопотоковому оточенні це можливо тільки при виклику з головного потоку.

### Список параметрів

`handler`

Функція зворотного дзвінка, яка буде встановлена ​​або видалена. Ця функція буде викликатись при настанні подій `CTRL+C`и`CTRL+BREAK`Функция должна иметь следующую сигнатуру:

```methodsynopsis
handler(int $event): void
```

`event`

Отримана подія `CTRL` **`PHP_WINDOWS_EVENT_CTRL_C`** або **`PHP_WINDOWS_EVENT_CTRL_BREAK`**

Установка параметра`handler`в значение\*\*`null`\*\* призведе до ігнорування подій `CTRL+C`, але не `CTRL+BREAK`

`add`

Якщо **`true`**, то обработчик будет установлен. Если\*\*`false`\*\*, Видалений.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Использование**sapi\_windows\_set\_ctrl\_handler()\*\*\*\*

У цьому прикладі показано, як перехоплювати події `CTRL`

```php
<?php
function ctrl_handler(int $event)
{
    switch ($event) {
        case PHP_WINDOWS_EVENT_CTRL_C:
            echo "Вы нажали CTRL+C\n";
            break;
        case PHP_WINDOWS_EVENT_CTRL_BREAK:
            echo "Вы нажали CTRL+BREAK\n";
            break;
    }
}

sapi_windows_set_ctrl_handler('ctrl_handler');
while (true); // Бесконечный цикл
?>
```

### Дивіться також

-   [sapi\_windows\_generate\_ctrl\_event()](function.sapi-windows-generate-ctrl-event.md) \- Надіслати подію CTRL іншому процесу
