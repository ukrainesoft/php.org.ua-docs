Налаштування під час виконання

-   [« Установка](apache.installation.html)
    
-   [Типы ресурсов »](apache.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](apache.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка модуля Apache PHP залежить від налаштувань у php.ini. Налаштування конфігурації з php.ini можуть бути перевизначені через налаштування прапора [php\_flag](configuration.changes.html#configuration.changes.apache) у конфігураційному файлі сервера або локальному файлі .htaccess.

**Приклад #1 Відключення PHP-сервера для директорії за допомогою .htaccess**

```
php_flag engine off
```

**Установки конфігурації Apache**

| Имя                                                               | По умолчанию | Место изменения | Список изменений |
|-------------------------------------------------------------------|--------------|-----------------|------------------|
| [engine](apache.configuration.html#ini.engine)                    | "1"          | PHPINIALL       |                  |
| [child\_terminate](apache.configuration.html#ini.child-terminate) | "0"          | PHPINIALL       |                  |
| [last\_modified](apache.configuration.html#ini.last-modified)     | "0"          | PHPINIALL       |                  |
| [xbithack](apache.configuration.html#ini.xbithack)                | "0"          | PHPINIALL       |                  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`engine` bool

Включає чи вимикає інтерпретатор PHP. Ця директива насправді дуже корисна у модулі Apache PHP. Вона використовується сайтами, яким необхідно дозволити чи заборонити інтерпретатор PHP на основі директорій чи віртуальних хостів. Встановлююча **`engine off`** за потребою у файлі httpd.conf можна дозволити або заборонити інтерпретатор PHP.

`child_terminate` bool

Ця установка керує тим, чи можуть скрипти PHP вимагати закінчення дочірніх процесів після завершення запиту. Дивіться також [apache\_child\_terminate()](function.apache-child-terminate.html)

`last_modified` bool

Надсилає скриптам PHP дату модифікації як заголовок Last-Modified для цього запиту.

`xbithack` bool

Виконання файлів з бітом, що запускається як PHP, незалежно від розширення.