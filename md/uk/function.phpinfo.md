---
navigation:
  - function.phpcredits.md: « phpcredits
  - function.phpversion.md: phpversion »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: phpinfo
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

phpinfo — Виводить інформацію про поточну конфігурацію PHP

### Опис

```methodsynopsis
phpinfo(int $flags = INFO_ALL): true
```

Виводить велику кількість інформації про поточний стан PHP. Сюди входить інформація про налаштування компіляції PHP, про модулі, про версію, інформація про сервер та середовище виконання (якщо PHP компілювався як модуль), оточення PHP, версії ОС, про шляхи, про основні та локальні значення налаштувань конфігурації, про HTTP-заголовки та ліцензії PHP.

Так как каждая система имеет свои особенности,**phpinfo()** використовується в основному для перевірки [налаштувань конфігурації](configuration.md) та для перегляду доступних [зумовлених констант](language.variables.predefined.md) у цій системі.

**phpinfo()** також використовується з метою налагодження, оскільки містить усі дані EGPCS (Environment, GET, POST, Cookie, Server).

### Список параметрів

`flags`

Виведення функції можна налаштовувати, передаючи бітову маску з однієї або більше наведених нижче констант (*constants*). Ця маска передається як необов'язковий аргумент `flags`. Окремі константи або бітові значення можна комбінувати за допомогою [побітового оператора АБО](language.operators.bitwise.md)

**Налаштування **phpinfo()****

| Имя (константа) | Значение | Опис |
| --- | --- | --- |
| INFO\_GENERAL |  | Рядок конфігурації, розташування php.ini, дата складання, сервер, система та ін. |
| INFO\_CREDITS |  | Розробники PHP. Дивіться також [phpcredits()](function.phpcredits.md) |
| INFO\_CONFIGURATION | 4 | Поточні значення основних та локальних PHP директив. Дивіться також [ini\_get()](function.ini-get.md) |
| INFO\_MODULES | 8 | Завантажені модулі та їх налаштування. Дивіться також [get\_loaded\_extensions()](function.get-loaded-extensions.md) |
| INFO\_ENVIRONMENT | 16 | Інформація про змінні оточення, яка також доступна в [$\_ENV](reserved.variables.environment.md) |
| INFO\_VARIABLES | 32 | Виводить все [зумовлені змінні](language.variables.predefined.md) з EGPCS (Environment, GET, POST, Cookie, Server). |
| INFO\_LICENSE | 64 | Інформація про ліцензію PHP. Дивіться також [» license FAQ](https://www.php.net/license/) |
| INFO\_ALL | \- | Виводить все наведене вище. |

### Значення, що повертаються

Функція завжди повертає **`true`**

### Приклади

**Пример #1 Пример использования**phpinfo()\*\*\*\*

```php
<?php

// Показывать всю информацию, по умолчанию INFO_ALL
phpinfo();

// Показывать информацию только о загруженных модулях.
// phpinfo(8) выдаёт тот же результат.
phpinfo(INFO_MODULES);

?>
```

### Примітки

> **Зауваження** :
> 
> У версіях PHP до 5.5 частина інформації не виводиться, якщо налаштування [expose\_php](ini.core.md#ini.expose-php)установлена в`off`. Це PHP та Zend логотипи та інформація про розробників.

> **Зауваження** :
> 
> В режиме CLI**phpinfo()** виводить звичайний текст замість HTML.

### Дивіться також

-   [phpversion()](function.phpversion.md) \- Отримує поточну версію PHP
-   [phpcredits()](function.phpcredits.md) \- Виводить список розробників PHP
-   [ini\_get()](function.ini-get.md) \- Отримує значення налаштування конфігурації
-   [ini\_set()](function.ini-set.md) \- Встановлює налаштування конфігурації
-   [get\_loaded\_extensions()](function.get-loaded-extensions.md) \- Повертає масив імен усіх скомпілованих та завантажених модулів
-   [Зумовлені змінні](language.variables.predefined.md)
