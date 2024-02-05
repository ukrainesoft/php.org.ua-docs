---
navigation:
  - ps.constants.md: « Зумовлені константи
  - function.ps-add-bookmark.md: ps\_add\_bookmark »
  - index.md: PHP Manual
  - book.ps.md: PS
title: Функції PS
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції PS

## Контакти

Коментарі, виправлення та пропозиції щодо покращення модуля або бібліотеки pslib надсилайте на пошту [» steinm@php.net](mailto:steinm@php.net). Вітається будь-яка допомога.

## Зміст

-   [ps\_add\_bookmark](function.ps-add-bookmark.md)— Додає закладку на поточну сторінку
-   [ps\_add\_launchlink](function.ps-add-launchlink.md)— Додає посилання, яке запускає файл
-   [ps\_add\_locallink](function.ps-add-locallink.md)— Додає посилання на сторінку того самого документа
-   [ps\_add\_note](function.ps-add-note.md)— Додає примітку до поточної сторінки
-   [ps\_add\_pdflink](function.ps-add-pdflink.md)— Додає посилання на сторінку в іншому PDF-документі
-   [ps\_add\_weblink](function.ps-add-weblink.md)— Додає посилання на веб-сторінку
-   [ps\_arc](function.ps-arc.md)— Малює дугу проти годинникової стрілки
-   [ps\_arcn](function.ps-arcn.md)— Малює дугу за годинниковою стрілкою
-   [ps\_begin\_page](function.ps-begin-page.md)— Починає нову сторінку
-   [ps\_begin\_pattern](function.ps-begin-pattern.md) \- Починає новий візерунок
-   [ps\_begin\_template](function.ps-begin-template.md)— Починає новий шаблон
-   [ps\_circle](function.ps-circle.md)— Малює коло
-   [ps\_clip](function.ps-clip.md)— Відображення кліпів поточним шляхом
-   [ps\_close\_image](function.ps-close-image.md)— Закриває зображення та звільняє пам'ять
-   [ps\_close](function.ps-close.md)— Закриває документ PostScript
-   [ps\_closepath\_stroke](function.ps-closepath-stroke.md)— Замикає та обводить контур
-   [ps\_closepath](function.ps-closepath.md) \- Замикає шлях
-   [ps\_continue\_text](function.ps-continue-text.md)— Продовжує текст у наступному рядку
-   [ps\_curveto](function.ps-curveto.md)— Малює криву
-   [ps\_delete](function.ps-delete.md)— Видаляє всі ресурси документа PostScript
-   [ps\_end\_page](function.ps-end-page.md) \- Завершує сторінку
-   [ps\_end\_pattern](function.ps-end-pattern.md) \- Завершує шаблон
-   [ps\_end\_template](function.ps-end-template.md) \- Завершує шаблон
-   [ps\_fill\_stroke](function.ps-fill-stroke.md)— Заповнює та обводить поточний шлях
-   [ps\_fill](function.ps-fill.md) \- Заповнює поточний шлях
-   [ps\_findfont](function.ps-findfont.md)— Завантажує шрифт
-   [ps\_get\_buffer](function.ps-get-buffer.md)— Отримує повний буфер, що містить згенеровані дані PS
-   [ps\_get\_parameter](function.ps-get-parameter.md)— Отримує певні параметри
-   [ps\_get\_value](function.ps-get-value.md)— Отримує певні значення
-   [ps\_hyphenate](function.ps-hyphenate.md) \- Переносить слово
-   [ps\_include\_file](function.ps-include-file.md)— Читає зовнішній файл із необробленим кодом PostScript
-   [ps\_lineto](function.ps-lineto.md)— Малює лінію
-   [ps\_makespotcolor](function.ps-makespotcolor.md) \- Створює плашковий колір
-   [ps\_moveto](function.ps-moveto.md) \- Встановлює поточну точку
-   [ps\_new](function.ps-new.md)— Створює новий об'єкт документа PostScript
-   [ps\_open\_file](function.ps-open-file.md)— Відкриває файл для виводу
-   [ps\_open\_image\_file](function.ps-open-image-file.md)— Відкриває зображення із файлу
-   [ps\_open\_image](function.ps-open-image.md)— Зчитує зображення для подальшого розміщення
-   [ps\_open\_memory\_image](function.ps-open-memory-image.md)— Бере зображення GD та повертає зображення для розміщення в документі PS
-   [ps\_place\_image](function.ps-place-image.md)— Розміщує зображення на сторінці
-   [ps\_rect](function.ps-rect.md)— Малює прямокутник
-   [ps\_restore](function.ps-restore.md)— Відновлює раніше збережений контекст
-   [ps\_rotate](function.ps-rotate.md) \- Встановлює коефіцієнт обертання
-   [ps\_save](function.ps-save.md)— Зберігає поточний контекст
-   [ps\_scale](function.ps-scale.md) \- Встановлює коефіцієнт масштабування
-   [ps\_set\_border\_color](function.ps-set-border-color.md) \- Встановлює колір межі анотацій
-   [ps\_set\_border\_dash](function.ps-set-border-dash.md) \- Встановлює довжину тире для межі анотації.
-   [ps\_set\_border\_style](function.ps-set-border-style.md)— Встановлює стиль межі анотацій
-   [ps\_set\_info](function.ps-set-info.md) \- Встановлює інформаційні поля документа
-   [ps\_set\_parameter](function.ps-set-parameter.md)— Встановлює певні параметри
-   [ps\_set\_text\_pos](function.ps-set-text-pos.md)— Встановлює позицію для виведення тексту
-   [ps\_set\_value](function.ps-set-value.md) \- Встановлює певні значення
-   [ps\_setcolor](function.ps-setcolor.md)— Встановлює поточний колір
-   [ps\_setdash](function.ps-setdash.md) \- Встановлює зовнішній вигляд пунктирної лінії
-   [ps\_setflat](function.ps-setflat.md) \- Встановлює площинність
-   [ps\_setfont](function.ps-setfont.md)— Встановлює шрифт, який використовуватиметься для наступного висновку
-   [ps\_setgray](function.ps-setgray.md) \- Встановлює значення сірого
-   [ps\_setlinecap](function.ps-setlinecap.md) \- Встановлює зовнішній вигляд закінчення лінії
-   [ps\_setlinejoin](function.ps-setlinejoin.md)— Встановлює спосіб з'єднання ліній
-   [ps\_setlinewidth](function.ps-setlinewidth.md) \- Встановлює ширину лінії
-   [ps\_setmiterlimit](function.ps-setmiterlimit.md) \- Встановлює межу скосу
-   [ps\_setoverprintmode](function.ps-setoverprintmode.md)— Встановлює режим накладання
-   [ps\_setpolydash](function.ps-setpolydash.md) \- Встановлює зовнішній вигляд пунктирної лінії
-   [ps\_shading\_pattern](function.ps-shading-pattern.md) \- Створює візерунок на основі затінення
-   [ps\_shading](function.ps-shading.md)— Створює затінення для подальшого використання
-   [ps\_shfill](function.ps-shfill.md) \- Заповнює область затіненням
-   [ps\_show\_boxed](function.ps-show-boxed.md) \- Виводить текст у поле
-   [ps\_show\_xy2](function.ps-show-xy2.md)— Виводить текст у заданій позиції
-   [ps\_show\_xy](function.ps-show-xy.md)— Виводить текст у заданій позиції
-   [ps\_show2](function.ps-show2.md)— Виводить текст у поточній позиції
-   [ps\_show](function.ps-show.md) \- Виводить текст
-   [ps\_string\_geometry](function.ps-string-geometry.md)— Отримує геометрію рядка
-   [ps\_stringwidth](function.ps-stringwidth.md)— Отримує ширину рядка
-   [ps\_stroke](function.ps-stroke.md)— Малює поточний шлях
-   [ps\_symbol\_name](function.ps-symbol-name.md)— Отримує ім'я гліфа
-   [ps\_symbol\_width](function.ps-symbol-width.md)— Отримує ширину гліфа
-   [ps\_symbol](function.ps-symbol.md) \- Виводить гліф
-   [ps\_translate](function.ps-translate.md) \- Змінює систему координат
