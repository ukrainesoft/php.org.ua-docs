---
navigation:
  - wkhtmltox-pdf-converter.add.md: '« wkhtmltox\\PDF\\Converter::add'
  - wkhtmltox-pdf-converter.convert.md: 'wkhtmltox\\PDF\\Converter::convert »'
  - index.md: PHP Manual
  - class.wkhtmltox-pdf-converter.md: wkhtmltox\\PDF\\Converter
title: 'wkhtmltox\\PDF\\Converter::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wkhtmltox\\PDF\\Converter::\_\_construct

(wkhtmltox >= 0.1.0)

wkhtmltox\\PDF\\Converter::\_\_construct — Створити новий PDF-конвертер

### Опис

public **wkhtmltox\\PDF\\Converter::\_\_construct**(array`$settings`

Створює PDF-конвертер, використовуючи додаткові параметри конфігурації

### Список параметрів

`settings`

| Название | Опис | Значения | Версия |
| --- | --- | --- | --- |
| size.pageSize | розмір паперу вихідного документа | A4 | \>= 0.1.0 |
| size.width | ширина вихідного документа | 210mm | \>= 0.1.0 |
| size.height | висота вихідного документа | 297mm | \>= 0.1.0 |
| orientation | орієнтація вихідного документа |  |  |

<table class="doctable table"><tbody class="tbody"><tr><td>Landscape</td></tr><tr><td>Portrait</td></tr></tbody></table>

\>= 0.1.0 | | colorMode | колірний режим вихідного документа

<table class="doctable table"><tbody class="tbody"><tr><td>Color</td></tr><tr><td>Greyscale</td></tr></tbody></table>

\>= 0.1.0 | | resolution | дозвіл вихідного документа most likely has no effect | >= 0.1.0 | | dpi | dpi to use while printing | 80 |>= 0.1.0 | | pageOffset | ціле число, додане до номерів сторінок, що генерують верхні та нижні колонтитули та зміст | | >= 0.1.0 | | copies |   |   |>= 0.1.0 | | collate | розібрати за копіями boolean | >= 0.1.0 | | outline | створити контур PDF | boolean | >= 0.1.0 | | outlineDepth | максимальна глибина контуру | | >= 0.1.0 | | dumpOutline | шлях до файлу дампа структури XML | >= 0.1.0 | | out | шлях до вихідного файлу, якщо "-", то використовується стандартний висновок | >= 0.1.0 | | documentTitle | назва вихідного документа | >= 0.1.0 | | useCompression | увімкнути або вимкнути стиск без втрат | boolean | >= 0.1.0 | | margin.top | розмір верхнього поля 2cm | >= 0.1.0 | | margin.bottom | розмір нижнього поля 2cm | >= 0.1.0 | | margin.left | розмір лівого поля 2cm | >= 0.1.0 | | margin.right | размер правого поля | 2cm |>= 0.1.0 | | imageDPI | максимальне DPI для зображень у вихідному документі | >= 0.1.0 | | imageQuality | Коефіцієнт стиснення JPEG для зображень у вихідному документі | 94 | >= 0.1.0 | | load.cookieJar | шлях до файлу, що використовується для завантаження та зберігання cookie /tmp/cookies.txt | >= 0.1.0 |
