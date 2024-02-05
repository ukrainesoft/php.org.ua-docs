---
navigation:
  - function.ps-add-launchlink.md: « ps\_add\_launchlink
  - function.ps-add-note.md: ps\_add\_note »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_add\_locallink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_add\_locallink

(PECL ps >= 1.1.0)

ps\_add\_locallink — Додає посилання на сторінку того самого документа

### Опис

```methodsynopsis
ps_add_locallink(    resource $psdoc,    float $llx,    float $lly,    float $urx,    float $ury,    int $page,    string $dest): bool
```

Додає гіперпосилання у заданому місці, що вказує на сторінку того самого документа. Натискання на посилання призведе до переходу на цю сторінку. Номер першої сторінки документа – 1.

Вихідна позиція гіперпосилання є прямокутником з нижнім лівим кутом в (`llx` `lly`) та його правим верхнім кутом в (`urx` `ury`). У прямокутника за промовчанням є тонка синя рамка.

Примітка не відображатиметься під час друку або перегляду документа, але буде показана під час конвертування документа в pdf за допомогою Acrobat Distiller™ або Ghostview.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`llx`

Координата X лівого нижнього кута.

`lly`

Координата Y лівого нижнього кута.

`urx`

Координата X правого верхнього кута.

`ury`

Координата Y правого верхнього кута.

`page`

Номер сторінки, що відображається під час переходу за посиланням.

`dest`

Параметр`dest` визначає спосіб перегляду документа. Може бути: `fitpage` `fitwidth` `fitheight`или`fitbbox`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_add\_launchlink()](function.ps-add-launchlink.md) \- Додає посилання, яке запускає файл
-   [ps\_add\_pdflink()](function.ps-add-pdflink.md) \- Додає посилання на сторінку в іншому PDF-документі
-   [ps\_add\_weblink()](function.ps-add-weblink.md) \- Додає посилання на веб-сторінку
