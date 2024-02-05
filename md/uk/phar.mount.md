---
navigation:
  - phar.mapphar.md: '« Phar::mapPhar'
  - phar.mungserver.md: 'Phar::mungServer »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::mount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::mount

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::mount — Монтування зовнішнього шляху або файлу до віртуального шляху в phar-архіві

### Опис

```methodsynopsis
final public static Phar::mount(string $pharPath, string $externalPath): void
```

Дуже схоже на концепцію файлової системи unix щодо монтування зовнішнього пристрою в існуюче дерево директорій . **Phar::mount()** дозволяє посилатися на зовнішні файли та директорії, ніби вони знаходяться всередині архіву. Це дозволяє підвищити рівень абстракції, звертаючись до зовнішніх конфігураційних файлів так, ніби вони є частиною архіву.

### Список параметрів

`pharPath`

Внутрішній шлях в архіві, яким необхідно примонтувати зовнішній шлях. Це має бути неіснуючий відносний шлях усередині архіву.

`externalPath`

Шлях або URL зовнішнього файлу чи директорії

### Значення, що повертаються

Нічого не вертає. У разі виникнення помилки викидає виняток [PharException](class.pharexception.md)

### Помилки

Викидає виняток [PharException](class.pharexception.md)при возникновении ошибок.

### Приклади

**Пример #1 Пример использования**Phar::mount()\*\*\*\*

У наступному прикладі демонструється доступ до зовнішнього конфігураційного файлу, наче він знаходиться всередині архіву.

Для початку код, що міститься в архіві:

```php
<?php
$configuration = simplexml_load_string(file_get_contents(
    Phar::running(false) . '/config.xml'));
?>
```

Далі зовнішній код, який монтує файл в архів:

```php
<?php
// для начала настроим ассоциацию между абстрактным config.xml
// и конкретным файлом на диске
Phar::mount('phar://config.xml', '/home/example/config.xml');
// а теперь запускаем приложение
include '/path/to/archive.phar';
?>
```

Інший метод - помістити код, що монтує, в заглушку (stub) Phar-архіву. Приклад використання конфігураційного файлу за замовчуванням, якщо файл конфігурації не заданий:

```php
<?php
// для начала настроим связь между абстрактным config.xml
// и конкретным файлом на диске
if (defined('EXTERNAL_CONFIG')) {
    Phar::mount('config.xml', EXTERNAL_CONFIG);
    if (file_exists(__DIR__ . '/extra_config.xml')) {
        Phar::mount('extra.xml', __DIR__ . '/extra_config.xml');
    }
} else {
    Phar::mount('config.xml', 'phar://' . __FILE__ . '/default_config.xml');
    Phar::mount('extra.xml', 'phar://' . __FILE__ . '/default_extra.xml');
}
// а теперь запускаем приложение
include 'phar://' . __FILE__ . '/index.php';
__HALT_COMPILER();
?>
```

... та код для завантаження цього phar-архіву:

```php
<?php
define('EXTERNAL_CONFIG', '/home/example/config.xml');
// а теперь запускаем приложение
include '/path/to/archive.phar';
?>
```
