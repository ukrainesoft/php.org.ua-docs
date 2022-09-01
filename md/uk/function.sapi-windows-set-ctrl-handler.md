---
navigation:
  - function.sapi-windows-generate-ctrl-event.html: « sapiwindowsgeneratectrlevent
  - function.sapi-windows-vt100-support.html: sapiwindowsvt100support »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sapiwindowssetctrlhandler
---
# sapiwindowssetctrlhandler

(PHP 7> = 7.4.0, PHP 8)

sapiwindowssetctrlhandler — Встановити або видалити обробник події CTRL

### Опис

```methodsynopsis
sapi_windows_set_ctrl_handler(?callable $handler, bool $add = true): bool
```

Встановлює або видаляє обробник події `CTRL`, який дозволить процесам Windows CLI перехоплювати чи ігнорувати події `CTRL+C` і `CTRL+BREAK`. Зверніть увагу, що в багатопотоковому оточенні це можливо тільки при виклику з головного потоку.

### Список параметрів

`handler`

Функція зворотного дзвінка, яка буде встановлена ​​або видалена. Ця функція буде викликатись при настанні подій `CTRL+C` і `CTRL+BREAK`. Функція повинна мати таку сигнатуру:

```methodsynopsis
handler(int $event): void
```

`event`

Отримана подія `CTRL` **`PHP_WINDOWS_EVENT_CTRL_C`** або **`PHP_WINDOWS_EVENT_CTRL_BREAK`**

Встановлення параметра `handler` на значення **`null`** призведе до ігнорування подій `CTRL+C`, але не `CTRL+BREAK`

`add`

Якщо **`true`**, то обробник буде встановлено. Якщо **`false`**, Видалений.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Використання **sapiwindowssetctrlhandler()****

У цьому прикладі показано, як перехоплювати події `CTRL`

```php
<?php
function ctrl_handler(int $event)
{
    switch ($event) {
        case PHP_WINDOWS_EVENT_CTRL_C:
            echo "Вы нажали CTRL+C\n";
            break;
        case PHP_WINDOWS_EVENT_CTRL_BREAK:
            echo "Вы нажали CTRL+BREAK\n";
            break;
    }
}

sapi_windows_set_ctrl_handler('ctrl_handler');
while (true); // Бесконечный цикл
?>
```

### Дивіться також

-   [sapiwindowsgeneratectrlevent()](function.sapi-windows-generate-ctrl-event.md) - Надіслати подію CTRL іншому процесу
