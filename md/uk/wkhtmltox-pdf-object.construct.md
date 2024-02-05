---
navigation:
  - class.wkhtmltox-pdf-object.md: « wkhtmltox\\PDF\\Object
  - class.wkhtmltox-image-converter.md: wkhtmltox\\Image\\Converter »
  - index.md: PHP Manual
  - class.wkhtmltox-pdf-object.md: wkhtmltox\\PDF\\Object
title: 'wkhtmltox\\PDF\\Object::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wkhtmltox\\PDF\\Object::\_\_construct

(wkhtmltox >= 0.1.0)

wkhtmltox\\PDF\\Object::\_\_construct — Створити новий об'єкт PDF

### Опис

public**wkhtmltox\\PDF\\Object::\_\_construct**(string`$buffer`, array`$settings`

Створює новий об'єкт PDF із зазначеного буфера та додаткові конфігураційні налаштування

### Список параметрів

`buffer`

HTML

`settings`

| Название | Опис | Значения | Версия |
| --- | --- | --- | --- |
| page | URL або шлях HTML для перетворення |  | \>= 0.1.0 |
| useExternalLinks | встановити значення true, щоб перетворити зовнішні посилання вхідних даних у зовнішні посилання PDF у вихідні дані | boolean | \>= 0.1.0 |
| useLocalLinks | встановити значення true, щоб перетворити внутрішні посилання вхідних даних у внутрішні посилання PDF у вихідні дані | boolean | \>= 0.1.0 |
| produceForms | встановити true, щоб перетворити HTML-форми на PDF-форми | boolean | \>= 0.1.0 |
| replacements | undocumented |  | \>= 0.1.0 |
| includeInOutline | встановити значення true, щоб включити розділи з цього об'єкта в структуру (outline) та зміст | boolean | \>= 0.1.0 |
| pagesCount | встановити значення true, щоб кількість сторінок у змісті включала кількість сторінок у цьому об'єкті | boolean | \>= 0.1.0 |
| tocXsl | встановити таблицю стилів для перетворення цього об'єкта на об'єкт змісту |  | \>= 0.1.0 |
| toc.useDottedLines | встановити значення true для використання пунктирних ліній у змісті | boolean | \>= 0.1.0 |
| toc.captionText | текст заголовка для змісту |  | \>= 0.1.0 |
| toc.forwardLinks | встановити значення true для створення посилань із змісту у вміст | boolean | \>= 0.1.0 |
| toc.backLinks | встановити значення true для створення посилань із вмісту в зміст | boolean | \>= 0.1.0 |
| toc.indentation | відступ для змісту | 2em | \>= 0.1.0 |
| toc.fontScale | коефіцієнт зменшення шрифту на кожному рівні змісту | 0.8 | \>= 0.1.0 |
| header.fontSize | розмір шрифту для заголовка | 13 | \>= 0.1.0 |
| header.fontName | назва шрифту в заголовку | times | \>= 0.1.0 |
| header.left | текст зліва від заголовка |  | \>= 0.1.0 |
| header.center | текст по центру заголовка |  | \>= 0.1.0 |
| header.right | текст праворуч від заголовка |  | \>= 0.1.0 |
| header.line | увімкнути або вимкнути горизонтальну лінію під заголовком | boolean | \>= 0.1.0 |
| header.spacing | пробіл між заголовком та вмістом | 1.8 | \>= 0.1.0 |
| header.mdUrl | URL або шлях HTML для використання у заголовку |  | \>= 0.1.0 |
| footer.fontSize | розмір шрифту для нижнього колонтитулу | 13 | \>= 0.1.0 |
| footer.fontName | назва шрифту для нижнього колонтитулу | times | \>= 0.1.0 |
| footer.left | текст зліва від нижнього колонтитулу |  | \>= 0.1.0 |
| footer.center | текст по центру нижнього колонтитулу |  | \>= 0.1.0 |
| footer.right | текст праворуч від нижнього колонтитулу |  | \>= 0.1.0 |
| footer.line | увімкнути або вимкнути горизонтальну лінію під нижнім колонтитулом | boolean | \>= 0.1.0 |
| footer.spacing | пробіл між футером та контентом | 1.8 | \>= 0.1.0 |
| footer.mdUrl | URL або шлях HTML для використання в нижньому колонтитулі |  | \>= 0.1.0 |
| load.username | ім'я користувача, яке використовується при вході на веб-сайт | bart | \>= 0.1.0 |
| load.password | пароль, який використовується при вході на веб-сайт | elbarto | \>= 0.1.0 |
| load.jsdelay | кількість часу в мілісекундах для очікування після завантаження сторінки, доки вона не буде захоплена | 1200 | \>= 0.1.0 |
| load.zoomFactor | наскільки масштабувати контент | 2.2 | \>= 0.1.0 |
| load.customHeaders | заголовки для відправки при запиті головної веб-сторінки |  | \>= 0.1.0 |
| load.repertCustomHeaders | встановіть true для надсилання з усіма запитами | boolean | \>= 0.1.0 |
| load.cookies | рядок cookie для надсилання при запиті головної веб-сторінки |  | \>= 0.1.0 |
| load.post | рядок post для надсилання при запиті головної веб-сторінки |  | \>= 0.1.0 |
| load.blockLocalFileAccess | заборонити локальним та переданим файлам доступ до інших локальних файлів | boolean | \>= 0.1.0 |
| load.stopSlowScript | зупинити повільний javascript | boolean |  |
| load.debugJavascript | дозволити javascript видавати попередження | boolean | \>= 0.1.0 |
| load.loadErrorHandling | встановити стратегію обробки помилок |  |  |

<table class="doctable table"><tbody class="tbody"><tr><td>abort</td><td>перервати процес перетворення</td></tr><tr><td>skip&lt; /td&gt;</td><td>не додавати об'єкт до кінцевого висновку</td></tr><tr><td>ignore</td><td>спробувати додати об'єкт до кінцевого висновку</td></tr></tbody></table>

\>= 0.1.0 | | load.proxy |   |   |>= 0.1.0 | | web.background | включити фонове зображення до висновку | boolean | >= 0.1.0 | | web.loadImages | увімкнути зображення у висновок | boolean | >= 0.1.0 | | web.enableJavascript | увімкнути або вимкнути javascript | boolean | >= 0.1.0 | | web.enableIntelligentShrinking | увімкнути для спроби вмістити більше вмісту на сторінці, застосовується лише до вихідних PDF-файлів | boolean | >= 0.1.0 | | web.minimumFontSize | мінімальний допустимий розмір шрифту 9 | >= 0.1.0 | | web.printMediaType | друкувати вміст, використовуючи тип носія print замість screen | boolean | >= 0.1.0 | | web.defaultEncoding | Вміст для використання без вказівки кодування | utf-8 | >= 0.1.0 | | web.userStyleSheet | URL або шлях до вказаної користувачем таблиці стилів /path/to/style.css | >= 0.1.0 | | web.enablePlugins | увімкнути або вимкнути плагіни NS | boolean | >= 0.1.0 |
