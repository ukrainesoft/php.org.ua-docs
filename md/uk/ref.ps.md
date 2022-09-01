---
navigation:
  - ps.constants.md: « Обумовлені константи
  - function.ps-add-bookmark.html: псaddbookmark »
  - index.md: PHP Manual
  - book.ps.md: ПС
title: Функції PS
---
# Функції PS

## Контакти

Коментарі, виправлення та пропозиції щодо покращення модуля або бібліотеки pslib надсилайте на пошту [» steinm@php.net](mailto:steinm@php.net). Вітається будь-яка допомога.

## Зміст

-   [псaddbookmark](function.ps-add-bookmark.html) — Додає закладку на поточну сторінку
-   [псaddlaunchlink](function.ps-add-launchlink.html) — Додає посилання, яке запускає файл
-   [псaddlocallink](function.ps-add-locallink.html) — Додає посилання на сторінку того самого документа
-   [псaddnote](function.ps-add-note.html) — Додає примітку до поточної сторінки
-   [псaddpdflink](function.ps-add-pdflink.html) — Додає посилання на сторінку в іншому PDF-документі
-   [псaddweblink](function.ps-add-weblink.html) — Додає посилання на веб-сторінку
-   [псarc](function.ps-arc.html) — Малює дугу проти годинникової стрілки
-   [псarcn](function.ps-arcn.html) — Малює дугу за годинниковою стрілкою
-   [псbeginpage](function.ps-begin-page.html) — Починає нову сторінку
-   [псbeginpattern](function.ps-begin-pattern.html) - Починає новий візерунок
-   [псbegintemplate](function.ps-begin-template.html) — Починає новий шаблон
-   [псcircle](function.ps-circle.html) — Малює коло
-   [псclip](function.ps-clip.html) — Відображення кліпів поточним шляхом
-   [псcloseimage](function.ps-close-image.html) — Закриває зображення та звільняє пам'ять
-   [псclose](function.ps-close.html) — Закриває документ PostScript
-   [псclosepathstroke](function.ps-closepath-stroke.html) — Замикає та обводить контур
-   [псclosepath](function.ps-closepath.html) - Замикає шлях
-   [псcontinuetext](function.ps-continue-text.html) — Продовжує текст у наступному рядку
-   [псcurveto](function.ps-curveto.html) — Малює криву
-   [псdelete](function.ps-delete.html) — Видаляє всі ресурси документа PostScript
-   [псendpage](function.ps-end-page.html) - Завершує сторінку
-   [псendpattern](function.ps-end-pattern.html) - Завершує шаблон
-   [псendtemplate](function.ps-end-template.html) - Завершує шаблон
-   [псfillstroke](function.ps-fill-stroke.html) — Заповнює та обводить поточний шлях
-   [псfill](function.ps-fill.html) - Заповнює поточний шлях
-   [псfindfont](function.ps-findfont.html) — Завантажує шрифт
-   [псgetbuffer](function.ps-get-buffer.html) — Отримує повний буфер, що містить згенеровані дані PS
-   [псgetparameter](function.ps-get-parameter.html) — Отримує певні параметри
-   [псgetvalue](function.ps-get-value.html) — Отримує певні значення
-   [псhyphenate](function.ps-hyphenate.html) - Переносить слово
-   [псincludefile](function.ps-include-file.html) — Читає зовнішній файл із необробленим кодом PostScript
-   [псlineto](function.ps-lineto.html) — Малює лінію
-   [псmakespotcolor](function.ps-makespotcolor.html) - Створює плашковий колір
-   [псmoveto](function.ps-moveto.html) — Встановлює поточну точку
-   [псnew](function.ps-new.html) — Створює новий об'єкт документа PostScript
-   [псopenfile](function.ps-open-file.html) — Відкриває файл для виводу
-   [псopenimagefile](function.ps-open-image-file.html) — Відкриває зображення із файлу
-   [псopenimage](function.ps-open-image.html) — Зчитує зображення для подальшого розміщення
-   [псopenmemoryimage](function.ps-open-memory-image.html) — Бере зображення GD та повертає зображення для розміщення в документі PS
-   [псplaceimage](function.ps-place-image.html) — Розміщує зображення на сторінці
-   [псrect](function.ps-rect.html) — Малює прямокутник
-   [псrestore](function.ps-restore.html) — Відновлює раніше збережений контекст
-   [псrotate](function.ps-rotate.html) - Встановлює коефіцієнт обертання
-   [псsave](function.ps-save.html) — Зберігає поточний контекст
-   [псscale](function.ps-scale.html) - Встановлює коефіцієнт масштабування
-   [псsetbordercolor](function.ps-set-border-color.html) - Встановлює колір межі анотацій
-   [псsetborderdash](function.ps-set-border-dash.html) - Встановлює довжину тире для межі анотації.
-   [псsetborderstyle](function.ps-set-border-style.html) — Встановлює стиль межі анотацій
-   [псsetinfo](function.ps-set-info.html) - Встановлює інформаційні поля документа
-   [псsetparameter](function.ps-set-parameter.html) — Встановлює певні параметри
-   [псsettextpos](function.ps-set-text-pos.html) — Встановлює позицію для виведення тексту
-   [псsetvalue](function.ps-set-value.html) - Встановлює певні значення
-   [псsetcolor](function.ps-setcolor.html) — Встановлює поточний колір
-   [псsetdash](function.ps-setdash.html) - Встановлює зовнішній вигляд пунктирної лінії
-   [псsetflat](function.ps-setflat.html) - Встановлює площинність
-   [псsetfont](function.ps-setfont.html) — Встановлює шрифт, який використовуватиметься для наступного висновку
-   [псsetgray](function.ps-setgray.html) - Встановлює значення сірого
-   [псsetlinecap](function.ps-setlinecap.html) - Встановлює зовнішній вигляд закінчення лінії
-   [псsetlinejoin](function.ps-setlinejoin.html) — Встановлює спосіб з'єднання ліній
-   [псsetlinewidth](function.ps-setlinewidth.html) - Встановлює ширину лінії
-   [псsetmiterlimit](function.ps-setmiterlimit.html) - Встановлює межу скосу
-   [псsetoverprintmode](function.ps-setoverprintmode.html) — Встановлює режим накладання
-   [псsetpolydash](function.ps-setpolydash.html) - Встановлює зовнішній вигляд пунктирної лінії
-   [псshadingpattern](function.ps-shading-pattern.html) - Створює візерунок на основі затінення
-   [псshading](function.ps-shading.html) — Створює затінення для подальшого використання
-   [псshfill](function.ps-shfill.html) - Заповнює область затіненням
-   [псshowboxed](function.ps-show-boxed.html) - Виводить текст у поле
-   [псshowxy2](function.ps-show-xy2.html) — Виводить текст у заданій позиції
-   [псshowзі](function.ps-show-xy.html) — Виводить текст у заданій позиції
-   [псshow2](function.ps-show2.html) — Виводить текст у поточній позиції
-   [псshow](function.ps-show.html) - Виводить текст
-   [псstringgeometry](function.ps-string-geometry.html) — Отримує геометрію рядка
-   [псstringwidth](function.ps-stringwidth.html) — Отримує ширину рядка
-   [псstroke](function.ps-stroke.html) — Малює поточний шлях
-   [псsymbolname](function.ps-symbol-name.html) — Отримує ім'я гліфа
-   [псsymbolwidth](function.ps-symbol-width.html) — Отримує ширину гліфа
-   [псsymbol](function.ps-symbol.html) - Виводить гліф
-   [псtranslate](function.ps-translate.html) - Змінює систему координат
