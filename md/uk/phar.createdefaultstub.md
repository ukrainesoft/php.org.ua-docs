Створити заглушку у форматі phar-архіву

-   [« Phar::count](phar.count.html)
    
-   [Phar::decompress »](phar.decompress.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Створити заглушку у форматі phar-архіву
    

# Phar::createDefaultStub

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::createDefaultStub — Створити заглушку у форматі phar-архіву

### Опис

```methodsynopsis
final public static Phar::createDefaultStub(?string $index = null, ?string $webIndex = null): string
```

Цей метод створює код заглушку (stub) у специфічному для phar-архіву форматі та не призначений для використання з файловими архівами на основі tar чи zip.

Phar-архіви містять завантажувач (`stub`), написаний на PHP, який запускається при запуску архіву, коли його підключають через include:

```php
<?php
include 'myphar.phar';
?>
```

або просто запускають:

```
php myphar.phar
```

Цей метод надає простий спосіб створення заглушку, який буде відпрацьовувати при запуску phar-архіву. Крім того, можна вказувати різні файли для запуску phar-архіву через веб-сервер та через командний рядок. Заглушка також викликає [Phar::interceptFileFuncs()](phar.interceptfilefuncs.html) для простого створення програм PHP з доступом до файлової системи. Якщо модуль phar відсутній, то заглушка розпакує phar-архів у тимчасову директорію та запустить програму звідти. Функція завершення роботи видаляє всі тимчасові файли.

### Список параметрів

`index`

Відносний шлях у phar-архіві для запуску при доступі з командного рядка

`webIndex`

Відносний шлях у phar-архіві для запуску при доступі через браузер

### Значення, що повертаються

Повертає текст із кодом заглушку, який дозволить Phar-архіву запускатися незалежно від того, підключений модуль Phar чи ні.

### Помилки

Викине виняток [UnexpectedValueException](class.unexpectedvalueexception.html)якщо будь-який з параметрів буде довше 400 байт.

### список змін

| Версия | Описание                                             |
|--------|------------------------------------------------------|
|        | `index` і `webIndex` тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::createDefaultStub()****

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [Phar::setStub()](phar.setstub.html) - Встановити завантажувач або завантажувальну заглушку в Phar-архів
-   [Phar::getStub()](phar.getstub.html) - Отримати завантажувач PHP або завантажувач заглушки Phar-архіву