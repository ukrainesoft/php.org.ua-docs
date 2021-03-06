- [« Встановлення](zlib.installation.md)
- [Типи ресурсів»](zlib.resources.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](zlib.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

Модуль zlib надає можливість стиснення сторінок, що передаються (у
т.ч. динамічні) на льоту, якщо браузер це підтримує. За стиск
відповідають три параметри в [конфігураційному файлі](configuration.file.md) `php.ini`.

| Ім'я За замовчуванням                                                                    | Місце зміни | Список змін |
| ---------------------------------------------------------------------------------------- | ----------- | ----------- |
| [zlib.output_compression](zlib.configuration.md#ini.zlib.output-compression)             | "0"         | PHP_INI_ALL |
| [zlib.output_compression_level](zlib.configuration.md#ini.zlib.output-compression-level) | "-1"        | PHP_INI_ALL |
| [zlib.output_handler](zlib.configuration.md#ini.zlib.output-handler)                     | ""          | PHP_INI_ALL |

**Конфігураційні параметри Zlib**

Для детального опису констант PHP_INI\_\*, зверніться до розділу [Де
можуть бути встановлені параметри конфігурації](configuration.changes.modes.md).

Коротке пояснення конфігураційних директив.

`zlib.output_compression` bool/int
Чи слід стискати сторінки. Якщо значення дорівнює "On" в `php.ini` (або
настройках Apache), сторінки стискатимуться, якщо браузер посилає
заголовок "Accept-Encoding: gzip" або "deflate". При цьому висновок будуть
додано заголовки "Content-Encoding: gzip" (відповідно "deflate")
та "Vary: Accept-Encoding". У режимі виконання, заголовок має бути
встановлений до моменту відправлення.

Ця опція також приймає цілі числа замість логічних "On/Off", з
за допомогою цього ви можете встановлювати розмір вихідного буфера
замовчуванням дорівнює 4 КБ).

> **Примітка**:
>
> [output_handler](outcontrol.configuration.md#ini.output-handler)
> має бути порожнім, якщо вибрано значення 'On'! Замість нього слід
> використовувати `zlib.output_handler`.

`zlib.output_compression_level` int
Рівень стиснення використовується для прозорого стиснення. Вкажіть
значення між 0 (без стиснення) та 9 (максимальне стиснення). За замовчуванням
-1 дозволяє серверу вирішувати, який рівень використовувати.

`zlib.output_handler` string
Якщо активовано zlib.output_compression, не можна вказувати
додаткові обробники виводу. Цей параметр виконує те саме, що і
[output_handler](outcontrol.configuration.md#ini.output-handler), але в
іншому порядку.
