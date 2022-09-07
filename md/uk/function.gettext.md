---
navigation:
  - function.dngettext.md: « dngettext
  - function.ngettext.md: ngettext »
  - index.md: PHP Manual
  - ref.gettext.md: Функции gettext
title: gettext
---
# gettext

(PHP 4, PHP 5, PHP 7, PHP 8)

gettext — Шукає повідомлення у поточному домені

### Опис

```methodsynopsis
gettext(string $message): string
```

Шукає повідомлення у поточному домені.

### Список параметрів

`message`

Повідомлення, що перекладається.

### Значення, що повертаються

Повертає переведений рядок (string), якщо він знайдений у таблиці перекладу, інакше - передане повідомлення.

### Приклади

\*\*Приклад #1 \*\*gettext()**check**

```php
<?php
// Устанавливаем русский язык
putenv('LC_ALL=ru_RU');
setlocale(LC_ALL, 'ru_RU');

// Указываем путь к таблицам переводов
bindtextdomain("myPHPApp", "./locale");

// Выбираем домен
textdomain("myPHPApp");

// Теперь поиск переводов будет идти в ./locale/ru_RU/LC_MESSAGES/myPHPApp.mo

// Выводим тестовое сообщение
echo gettext("Welcome to My PHP Application");

// Или с использованием псевдонима _()
echo _("Have a nice day");
?>
```

### Примітки

> **Зауваження**
> 
> Можна використовувати символ підкреслення '' як псевдонім цієї функції.

> **Зауваження**
> 
> На деяких системах може бути недостатньо вказівки мови, у таких випадках використовуйте [putenv()](function.putenv.md) для вказівки поточної локалі.

### Дивіться також

-   [setlocale()](function.setlocale.md) - Встановлює налаштування локалі
