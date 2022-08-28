Налаштування під час виконання

-   [« Установка](runkit7.installation.html)
    
-   [Типы ресурсов »](runkit7.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](runkit7.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації Runkit**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [runkit.superglobal](runkit7.configuration.html#ini.runkit7.superglobal) | "" | PHPINIPERDIR |  |
| [runkit.internal\_override](runkit7.configuration.html#ini.runkit7.internal-override) | "0" | PHPINISYSTEM |  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`runkit.superglobal` string

Розділений комами список імен змінних, які розглядатимуться як суперглобальні. Це значення має бути встановлене у загальносистемному файлі php.ini, але може працювати в контекстах конфігурації perdir залежно від вашого SAPI.

**Приклад #1 Користувальницькі суперглобальні файли з runkit.superglobal=FOO,BAR у php.ini**

```php
<?php
function show_values() {
  echo "Foo is $_FOO\n";
  echo "Bar is $_BAR\n";
  echo "Baz is $_BAZ\n";
}

$_FOO = 'foo';
$_BAR = 'bar';
$_BAZ = 'baz';

/* Отобразит foo и bar, но не baz */
show_values();
?>
```

`runkit.internal_override` bool

Дозволяє змінювати/перейменовувати/вилучати внутрішні функції.