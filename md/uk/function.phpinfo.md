---
navigation:
  - function.phpcredits.md: « phpcredits
  - function.phpversion.md: phpversion »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: phpinfo
---
# phpinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

phpinfo — Виводить інформацію про поточну конфігурацію PHP

### Опис

```methodsynopsis
phpinfo(int $flags = INFO_ALL): bool
```

Виводить велику кількість інформації про поточний стан PHP. Сюди входить інформація про налаштування компіляції PHP, про модулі, про версію, інформація про сервер та середовище виконання (якщо PHP компілювався як модуль), оточення PHP, версії ОС, про шляхи, про основні та локальні значення налаштувань конфігурації, про HTTP-заголовки та ліцензії PHP.

Так як кожна система має свої особливості, **phpinfo()** використовується в основному для перевірки [налаштувань конфігурації](configuration.md) та для перегляду доступних [зумовлених констант](language.variables.predefined.md) у цій системі.

**phpinfo()** також використовується з метою налагодження, оскільки містить усі дані EGPCS (Environment, GET, POST, Cookie, Server).

### Список параметрів

`flags`

Виведення функції можна налаштовувати, передаючи бітову маску з однієї або більше наведених нижче констант (*constants*). Ця маска передається як необов'язковий аргумент `flags`. Окремі константи або бітові значення можна комбінувати за допомогою оператора [побітового оператора АБО](language.operators.bitwise.md)

**Налаштування **phpinfo()****

| Имя (константа) | Значение | Описание |
| --- | --- | --- |
| INFOGENERAL |  | Рядок конфігурації, розташування php.ini, дата складання, сервер, система та ін. |
| INFOCREDITS |  | Розробники PHP. Дивіться також [phpcredits()](function.phpcredits.md) |
| INFOCONFIGURATION |  | Поточні значення основних та локальних PHP директив. Дивіться також [iniget()](function.ini-get.md) |
| INFOMODULES |  | Завантажені модулі та їх налаштування. Дивіться також [getloadedextensions()](function.get-loaded-extensions.md) |
| INFOENVIRONMENT |  | Інформація про змінні оточення, яка також доступна в [ENV](reserved.variables.environment.md) |
| INFOVARIABLES |  | Виводить все [зумовлені змінні](language.variables.predefined.md) з EGPCS (Environment, GET, POST, Cookie, Server). |
| INFOLICENSE |  | Інформація про ліцензію PHP. Дивіться також [» license FAQ](https://www.php.net/license/) |
| INFOALL |  | Виводить все наведене вище. |

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **phpinfo()****

```php
<?php

// Показывать всю информацию, по умолчанию INFO_ALL
phpinfo();

// Показывать информацию только о загруженных модулях.
// phpinfo(8) выдаёт тот же результат.
phpinfo(INFO_MODULES);

?>
```

### Примітки

> **Зауваження**
> 
> У версіях PHP до 5.5 частина інформації не виводиться, якщо налаштування [exposephp](ini.core.html#ini.expose-php) встановлена ​​в `off`. Це PHP та Zend логотипи та інформація про розробників.

> **Зауваження**
> 
> У режимі CLI **phpinfo()** виводить звичайний текст замість HTML.

### Дивіться також

-   [phpversion()](function.phpversion.md) - Отримує поточну версію PHP
-   [phpcredits()](function.phpcredits.md) - Виводить список розробників PHP
-   [iniget()](function.ini-get.md) - Отримує значення налаштування конфігурації
-   [iniset()](function.ini-set.md) - Встановлює налаштування конфігурації
-   [getloadedextensions()](function.get-loaded-extensions.md) - Повертає масив імен усіх скомпілованих та завантажених модулів
-   [Зумовлені змінні](language.variables.predefined.md)
