---
navigation:
  - function.ps-add-pdflink.html: «psaddpdflink
  - function.ps-arc.html: псarc »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псaddweblink
---
# псaddweblink

(PECL ps >= 1.1.0)

псaddweblink — Додає посилання на веб-сторінку

### Опис

```methodsynopsis
ps_add_weblink(    resource $psdoc,    float $llx,    float $lly,    float $urx,    float $ury,    string $url): bool
```

Додає гіперпосилання у вказаному місці, яке вказує на веб-сторінку. Вихідна позиція гіперпосилання є прямокутником з нижнім лівим кутом в (`llx` `lly`) та його правим верхнім кутом в (`urx` `ury`). У прямокутника за промовчанням є тонка синя рамка.

Примітка не відображатиметься під час друку або перегляду документа, але буде показана під час конвертування документа в pdf за допомогою Acrobat Distiller™ або Ghostview.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.html)

`llx`

Координата X лівого нижнього кута.

`lly`

Координата Y лівого нижнього кута.

`urx`

Координата X правого верхнього кута.

`ury`

Координата Y правого верхнього кута.

`url`

URL-адреса гіперпосилання, яка відкривається при натисканні на посилання, наприклад, `http://www.php.net`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псaddlaunchlink()](function.ps-add-launchlink.html) - Додає посилання, яке запускає файл
-   [псaddlocallink()](function.ps-add-locallink.html) - Додає посилання на сторінку того самого документа
-   [псaddpdflink()](function.ps-add-pdflink.html) - Додає посилання на сторінку в іншому PDF-документі
