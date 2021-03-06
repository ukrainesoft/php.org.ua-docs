- [«Phar::count](phar.count.md)
- [Phar::decompress »](phar.decompress.md)

- [PHP Manual](index.md)
- [Phar](class.phar.md)
- Створити заглушку у форматі phar-архіву

# Phar::createDefaultStub

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL phar = 2.0.0)

Phar::createDefaultStub — Створити заглушку у форматі phar-архіву

### Опис

final public static **Phar::createDefaultStub**(?string `$index` =
**`null`**, ?string `$webIndex` = **`null`**): string

Цей метод створює код заглушку (stub) у специфічному для phar-архіву
форматі та не призначений для використання з файловими архівами на
основі tar або zip.

Phar-архіви містять завантажувач (`stub`), написаний на PHP, який
запускається при запуску архіву, коли його підключають через include:

`<?phpinclude ''myphar.phar';?> `

або просто запускають:

php myphar.phar

Цей метод надає простий спосіб для створення заглушку, який
буде відпрацьовувати під час запуску phar-архіву. Крім того, можна вказувати
різні файли для запуску phar-архіву через веб-сервер та через командну
рядок. Заглушка також викликає
[Phar::interceptFileFuncs()](phar.interceptfilefuncs.md) для простого
створення програм PHP з доступом до файлової системи. Якщо модуль phar
відсутня, то заглушка розпакує phar-архів у тимчасову директорію та
запустить програму звідти. Функція завершення роботи видалить все
тимчасові файли.

### Список параметрів

`index`
Відносний шлях у phar-архіві для запуску при доступі з командної
рядки

`webIndex`
Відносний шлях у phar-архіві для запуску при доступі через браузер

### Значення, що повертаються

Повертає текст із кодом заглушку, який дозволить Phar-архіву
запускатися незалежно від того, підключений модуль Phar чи ні.

### Помилки

Викине виняток
[UnexpectedValueException](class.unexpectedvalueexception.md), якщо
будь-який з параметрів буде довшим за 400 байт.

### Список змін

| Версія | Опис                                              |
| ------ | ------------------------------------------------- |
| 8.0.0  | index та webIndex тепер допускають значення null. |

### Приклади

**Приклад #1 Приклад використання **Phar::createDefaultStub()****

`<?phptry {   $phar = new Phar('myphar.phar'); $phar->setStub($phar->createDefaultStub('cli.php', 'web/index.php'));} catch (Exception $e) {    // обробка помилок}?> `

### Дивіться також

- [Phar::setStub()](phar.setstub.md) - Встановити завантажувач або
завантажувальну заглушку в Phar-архів
- [Phar::getStub()](phar.getstub.md) - Отримати завантажувач PHP або
завантажувач заглушки Phar-архіву
