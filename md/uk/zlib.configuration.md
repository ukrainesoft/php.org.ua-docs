---
navigation:
  - zlib.installation.md: « Установка
  - zlib.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - zlib.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

Модуль zlib надає можливість стиснення сторінок, що передаються (в т.ч. динамічних) на льоту, якщо браузер це підтримує. За стиск відповідають три параметри в [конфігураційному файлі](configuration.file.md) php.ini.

**Параметри конфігурації Zlib**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [zlib.outputcompression](zlib.configuration.md#ini.zlib.output-compression) | "0" | PHPINIALL |  |
| [zlib.outputcompressionlevel](zlib.configuration.md#ini.zlib.output-compression-level) | "-1" | PHPINIALL |  |
| [zlib.outputhandler](zlib.configuration.md#ini.zlib.output-handler) | "" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`zlib.output_compression` bool/int

Чи слід стискати сторінки. Якщо значення дорівнює "On" у php.ini (або в налаштуваннях Apache), сторінки стискатимуться, якщо браузер посилає заголовок "Accept-Encoding: gzip" або "deflate". При цьому висновок будуть додані заголовки "Content-Encoding: gzip" (відповідно "deflate") і "Vary: Accept-Encoding". У режимі виконання заголовок повинен бути встановлений до моменту відправки.

Ця опція також приймає цілі числа замість логічних On/Off, за допомогою цього ви можете встановлювати розмір вихідного буфера (за замовчуванням дорівнює 4 КБ).

> **Зауваження**
> 
> [outputhandler](outcontrol.configuration.md#ini.output-handler) має бути порожнім, якщо вибрано значення 'On'! Замість нього слід використовувати `zlib.output_handler`

`zlib.output_compression_level` int

Рівень стиснення використовується для прозорого стиснення. Вкажіть значення між 0 (без стиснення) та 9 (максимальне стиснення). За замовчуванням -1 дозволяє серверу вирішувати, який рівень використовувати.

`zlib.output_handler` string

Якщо zlib.outputcompression активовано, не можна вказувати додаткові обробники виводу. Цей параметр виконує те саме, що і [outputhandler](outcontrol.configuration.md#ini.output-handler)але в іншому порядку.
