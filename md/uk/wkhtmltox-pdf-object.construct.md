Створити новий об'єкт PDF

-   [« wkhtmltox\\PDF\\Object](class.wkhtmltox-pdf-object.html)
    
-   [wkhtmltox\\Image\\Converter »](class.wkhtmltox-image-converter.html)
    
-   [PHP Manual](index.html)
    
-   [wkhtmltox\\PDF\\Object](class.wkhtmltox-pdf-object.html)
    
-   Створити новий об'єкт PDF
    

# wkhtmltoxPDFObject::construct

(wkhtmltox >= 0.1.0)

wkhtmltoxPDFObject::construct — Створити новий об'єкт PDF

### Опис

public **wkhtmltoxPDFObject::construct**(string `$buffer`, array `$settings`

Створює новий об'єкт PDF із зазначеного буфера та додаткові конфігураційні налаштування

### Список параметрів

`buffer`

HTML

`settings`

| Название | Описание | Значения | Версия |
| --- | --- | --- | --- |
| page | URL або шлях HTML для перетворення |  | \> |
| useExternalLinks | встановити значення true, щоб перетворити зовнішні посилання вхідних даних на зовнішні посилання PDF у вихідні дані | boolean | \> |
| useLocalLinks | встановити значення true, щоб перетворити внутрішні посилання вхідних даних у внутрішні посилання PDF у вихідні дані | boolean | \> |
| produceForms | встановити true, щоб перетворити HTML-форми на PDF-форми | boolean | \> |
| replacements | undocumented |  | \> |
| includeInOutline | встановити значення true, щоб включити розділи з цього об'єкта в структуру (outline) та зміст | boolean | \> |
| pagesCount | встановити значення true, щоб кількість сторінок у змісті включала кількість сторінок у цьому об'єкті | boolean | \> |
| tocXsl | встановити таблицю стилів для перетворення цього об'єкта на об'єкт змісту |  | \> |
| toc.useDottedLines | встановити значення true для використання пунктирних ліній у змісті | boolean | \> |
| toc.captionText | текст заголовка для змісту |  | \> |
| toc.forwardLinks | встановити значення true для створення посилань із змісту у вміст | boolean | \> |
| toc.backLinks | встановити значення true для створення посилань із вмісту в зміст | boolean | \> |
| toc.indentation | відступ для змісту | 2em | \> |
| toc.fontScale | коефіцієнт зменшення шрифту на кожному рівні змісту |  | \> |
| header.fontSize | розмір шрифту для заголовка |  | \> |
| header.fontName | назва шрифту в заголовку | times | \> |
| header.left | текст зліва від заголовка |  | \> |
| неадер.центр | текст по центру заголовка |  | \> |
| header.right | текст праворуч від заголовка |  | \> |
| header.line | увімкнути або вимкнути горизонтальну лінію під заголовком | boolean | \> |
| header.spacing | пробіл між заголовком та вмістом |  | \> |
| header.htmlUrl | URL або шлях HTML для використання у заголовку |  | \> |
| footer.fontSize | розмір шрифту для нижнього колонтитулу |  | \> |
| footer.fontName | назва шрифту для нижнього колонтитулу | times | \> |
| footer.left | текст зліва від нижнього колонтитулу |  | \> |
| футер.центр | текст по центру нижнього колонтитулу |  | \> |
| footer.right | текст праворуч від нижнього колонтитулу |  | \> |
| footer.line | увімкнути або вимкнути горизонтальну лінію під нижнім колонтитулом | boolean | \> |
| footer.spacing | пробіл між футером та контентом |  | \> |
| footer.htmlUrl | URL або шлях HTML для використання в нижньому колонтитулі |  | \> |
| load.username | ім'я користувача, яке використовується при вході на веб-сайт | bart | \> |
| load.password | пароль, який використовується при вході на веб-сайт | elbarto | \> |
| load.jsdelay | кількість часу в мілісекундах для очікування після завантаження сторінки, доки вона не буде захоплена |  | \> |
| load.zoomFactor | наскільки масштабувати контент |  | \> |
| load.customHeaders | заголовки для відправки при запиті головної веб-сторінки |  | \> |
| load.repertCustomHeaders | встановіть true для надсилання з усіма запитами | boolean | \> |
| load.cookies | рядок cookie для надсилання при запиті головної веб-сторінки |  | \> |
| лоад.пост | рядок post для надсилання при запиті головної веб-сторінки |  | \> |
| load.blockLocalFileAccess | заборонити локальним та переданим файлам доступ до інших локальних файлів | boolean | \> |
| load.stopSlowScript | зупинити повільний javascript | boolean |  |
| load.debugJavascript | дозволити javascript видавати попередження | boolean | \> |
| load.loadErrorHandling | встановити стратегію обробки помилок |  |  |

<table class="doctable table"><tbody class="tbody"><tr><td>abort</td><td>перервати процес перетворення</td></tr><tr><td>skip&lt; /td&gt;</td><td>не додавати об'єкт до кінцевого висновку</td></tr><tr><td>ignore</td><td>спробувати додати об'єкт до кінцевого висновку</td></tr></tbody></table>

\>= 0.1.0 | | load.proxy | | | >= 0.1.0 | | web.background | включити фонове зображення до висновку | boolean | >= 0.1.0 | | web.loadImages | увімкнути зображення у висновок | boolean | >= 0.1.0 | | web.enableJavascript | увімкнути або вимкнути javascript | boolean | >= 0.1.0 | | web.enableIntelligentShrinking | увімкнути для спроби вмістити більше вмісту на сторінці, застосовується лише до вихідних PDF-файлів | boolean | >= 0.1.0 | | web.minimumFontSize | мінімальний допустимий розмір шрифту 9 | >= 0.1.0 | | web.printMediaType | друкувати вміст, використовуючи тип носія print замість screen | boolean | >= 0.1.0 | | web.defaultEncoding | Вміст для використання без вказівки кодування | utf-8 | >= 0.1.0 | | web.userStyleSheet | URL або шлях до вказаної користувачем таблиці стилів /path/to/style.css | >= 0.1.0 | | web.enablePlugins | увімкнути чи вимкнути плагіни NS | boolean | >