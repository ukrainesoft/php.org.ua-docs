Додає посилання, яке запускає файл

-   [« ps\_add\_bookmark](function.ps-add-bookmark.html)
    
-   [ps\_add\_locallink »](function.ps-add-locallink.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Додає посилання, яке запускає файл
    

# псaddlaunchlink

(PECL ps >= 1.1.0)

псaddlaunchlink — Додає посилання, яке запускає файл

### Опис

```methodsynopsis
ps_add_launchlink(    resource $psdoc,    float $llx,    float $lly,    float $urx,    float $ury,    string $filename): bool
```

Поміщає гіперпосилання у задану позицію, яка вказує на файлову програму, яка запускається під час натискання. Вихідна позиція гіперпосилання - це прямокутник з нижнім лівим кутом позиції (llx, lly) і верхнім правим кутом позиції (urx, ury). У прямокутника за промовчанням тонка синя рамка.

Примітка не відображатиметься під час друку або перегляду документа, але буде показана під час конвертування документа в pdf за допомогою Acrobat Distiller™ або Ghostview.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ps\_add\_locallink()](function.ps-add-locallink.html) - Додає посилання на сторінку того самого документа
-   [ps\_add\_pdflink()](function.ps-add-pdflink.html) - Додає посилання на сторінку в іншому PDF-документі
-   [ps\_add\_weblink()](function.ps-add-weblink.html) - Додає посилання на веб-сторінку