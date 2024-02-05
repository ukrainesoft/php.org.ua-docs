---
navigation:
  - function.ps-add-bookmark.md: « ps\_add\_bookmark
  - function.ps-add-locallink.md: ps\_add\_locallink »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_add\_launchlink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_add\_launchlink

(PECL ps >= 1.1.0)

ps\_add\_launchlink — Додає посилання, яке запускає файл

### Опис

```methodsynopsis
ps_add_launchlink(    resource $psdoc,    float $llx,    float $lly,    float $urx,    float $ury,    string $filename): bool
```

Поміщає гіперпосилання у задану позицію, яка вказує на файлову програму, яка запускається при натисканні. Вихідна позиція гіперпосилання - це прямокутник з нижнім лівим кутом позиції (llx, lly) і верхнім правим кутом позиції (urx, ury). У прямокутника за промовчанням тонка синя рамка.

Примітка не відображатиметься під час друку або перегляду документа, але буде показана під час конвертування документа в pdf за допомогою Acrobat Distiller™ або Ghostview.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`llx`

Координата X лівого нижнього кута.

`lly`

Координата Y лівого нижнього кута.

`urx`

Координата X правого верхнього кута.

`ury`

Координата Y правого верхнього кута.

`filename`

Шлях до програми, що запускається при натисканні на посилання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_add\_locallink()](function.ps-add-locallink.md) \- Додає посилання на сторінку того самого документа
-   [ps\_add\_pdflink()](function.ps-add-pdflink.md) \- Додає посилання на сторінку в іншому PDF-документі
-   [ps\_add\_weblink()](function.ps-add-weblink.md) \- Додає посилання на веб-сторінку
