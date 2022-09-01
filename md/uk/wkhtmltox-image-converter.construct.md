---
navigation:
  - class.wkhtmltox-image-converter.html: « wkhtmltoxImageConverter
  - wkhtmltox-image-converter.convert.html: 'wkhtmltoxImageConverter::convert »'
  - index.html: PHP Manual
  - class.wkhtmltox-image-converter.html: wkhtmltoxImageConverter
title: 'wkhtmltoxImageConverter::construct'
---
# wkhtmltoxImageConverter::construct

(wkhtmltox >= 0.1.0)

wkhtmltoxImageConverter::construct — Створити новий конвертер зображень

### Опис

public **wkhtmltoxImageConverter::construct**(string `$buffer` = ?, array `$settings`

Створює конвертер зображень, додатково використовуючи вхідний буфер та налаштування конфігурації

### Список параметрів

`buffer`

HTML

`settings`

| Название | Описание | Значения | Версия |
| --- | --- | --- | --- |
| ін | URL або шлях вхідного файлу, якщо "-", то використовується стандартне введення | /патх/то/маркуп.хтмл | \> |
| out | шлях до вихідного файлу, якщо "-", то використовується стандартний висновок, за замовчуванням використовується внутрішній буфер | /патх/то/оутпут.пнг | \> |
| fmt | формат виводу для використання |  |  |

<table class="doctable table"><tbody class="tbody"><tr><td>""</td><td>за замовчуванням</td></tr><tr><td>jpg&lt; /td&gt;</td><td>висновок у форматі JPEG</td></tr><tr><td>png</td><td>висновок у форматі PNG</td></tr><tr><td>bmp</td><td>виведення у форматі растрового зображення</td></tr><tr><td>svg</td><td>виведення у форматі SVG</td></tr></tbody></table>

\>= 0.1.0 | | transparent | при виведенні PNG або SVG зробити білий фон прозорим | boolean | >= 0.1.0 | | screenWidth | ширина екрану, що використовується для відтворення пікселів | 800 | >= 0.1.0 | | smartWidth | коли true, screenWidth розширюється до ширини вмісту | boolean | >= 0.1.0 | | quality | коефіцієнт стиснення, використовуваний під час виведення JPEG-зображення | 94 | >= 0.1.0 | | crop.left | ліва x-координата вікна для захоплення в пікселях 200 | >= 0.1.0 | | crop.top верхня y-координата вікна для захоплення в пікселях 200 | >= 0.1.0 | | crop.width | ширина вікна для захоплення в пікселях 200 | >= 0.1.0 | | crop.height | ширина вікна для захоплення в пікселях 200 | >= 0.1.0 | | load.cookieJar | шлях до файлу, що використовується для завантаження та зберігання cookie /tmp/cookies.txt | >= 0.1.0 | | load.username | ім'я користувача, яке використовується при вході на веб-сайт | bart | >= 0.1.0 | | load.password | пароль, який використовується при вході на сайт | Elbarto | >= 0.1.0 | | load.jsdelay | кількість часу в мілісекундах для очікування після завантаження сторінки, доки вона не буде захоплена | 1200 | >= 0.1.0 | | load.zoomFactor | наскільки масштабувати контент 2.2 | >= 0.1.0 | | load.customHeaders | заголовки для відправки при запиті головної веб-сторінки | | >= 0.1.0 | | load.repertCustomHeaders | встановити true для відправки з усіма запитами | boolean | >= 0.1.0 | | load.cookies | рядок cookie для надсилання при запиті на головну веб-сторінку | | >= 0.1.0 | | load.post | рядок post для надсилання за запитом головної веб-сторінки | | >= 0.1.0 | | load.blockLocalFileAccess | заборонити локальним та переданим файлам доступ до інших локальних файлів | boolean | >= 0.1.0 | | load.stopSlowScript | зупинити повільний javascript boolean | | | load.debugJavascript | дозволити JavaScript видавати попередження | boolean | >= 0.1.0 | | load.loadErrorHandling | встановити стратегію обробки помилок

<table class="doctable table"><tbody class="tbody"><tr><td>abort</td><td>перервати процес перетворення</td></tr><tr><td>skip&lt; /td&gt;</td><td>не додавати об'єкт до кінцевого висновку</td></tr><tr><td>ignore</td><td>спробувати додати об'єкт до кінцевого висновку</td></tr></tbody></table>

\>= 0.1.0 | | load.proxy | | | >= 0.1.0 | | web.background | включити фонове зображення до висновку | boolean | >= 0.1.0 | | web.loadImages | увімкнути зображення у висновок | boolean | >= 0.1.0 | | web.enableJavascript | увімкнути або вимкнути javascript | boolean | >= 0.1.0 | | web.enableIntelligentShrinking | увімкнути для спроби вмістити більше вмісту на сторінці, застосовується лише до вихідних PDF-файлів | boolean | >= 0.1.0 | | web.minimumFontSize | мінімальний допустимий розмір шрифту 9 | >= 0.1.0 | | web.printMediaType | друкувати вміст, використовуючи тип носія print замість screen | boolean | >= 0.1.0 | | web.defaultEncoding | Вміст для використання без вказівки кодування | utf-8 | >= 0.1.0 | | web.userStyleSheet | URL або шлях до вказаної користувачем таблиці стилів /path/to/style.css | >= 0.1.0 | | web.enablePlugins | увімкнути чи вимкнути плагіни NS | boolean | >
