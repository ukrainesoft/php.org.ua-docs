---
navigation:
  - function.ps-add-pdflink.md: « ps\_add\_pdflink
  - function.ps-arc.md: ps\_arc »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_add\_weblink
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_add\_weblink

(PECL ps >= 1.1.0)

ps\_add\_weblink — Додає посилання на веб-сторінку

### Опис

```methodsynopsis
ps_add_weblink(    resource $psdoc,    float $llx,    float $lly,    float $urx,    float $ury,    string $url): bool
```

Додає гіперпосилання у вказаному місці, яке вказує на веб-сторінку. Вихідна позиція гіперпосилання є прямокутником з нижнім лівим кутом в (`llx` `lly`) та його правим верхнім кутом в (`urx` `ury`). У прямокутника за промовчанням є тонка синя рамка.

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

`url`

URL-адреса гіперпосилання, що відкривається при натисканні на посилання, наприклад, `http://www.php.net`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_add\_launchlink()](function.ps-add-launchlink.md) \- Додає посилання, яке запускає файл
-   [ps\_add\_locallink()](function.ps-add-locallink.md) \- Додає посилання на сторінку того самого документа
-   [ps\_add\_pdflink()](function.ps-add-pdflink.md) \- Додає посилання на сторінку в іншому PDF-документі
