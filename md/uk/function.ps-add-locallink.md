- [«ps_add_launchlink](function.ps-add-launchlink.md)
- [ps_add_note »](function.ps-add-note.md)

- [PHP Manual](index.md)
- [Функції PS](ref.ps.md)
- Додає посилання на сторінку того самого документа

#ps_add_locallink

(PECL ps \>= 1.1.0)

ps_add_locallink — Додає посилання на сторінку того самого документа

### Опис

**ps_add_locallink**(
resource `$psdoc`,
float `$llx`,
float `$lly`,
float `$urx`,
float `$ury`,
int `$page`,
string `$dest`
): bool

Додає гіперпосилання в заданому місці, що вказує на сторінку того ж
документа. Натискання на посилання призведе до переходу на цю сторінку.
Номер першої сторінки документа – 1.

Вихідна позиція гіперпосилання є прямокутником з нижнім
лівим кутом в (`llx`, `lly`) та його правим верхнім кутом у (`urx`,
`ury`). У прямокутника є тонка синя рамка.

Примітка не відображатиметься під час друку або перегляду документа, але
буде показано при конвертуванні документа в PDF за допомогою Acrobat
Distiller™ або Ghostview.

### Список параметрів

`psdoc`
Ідентифікатор ресурсу файлу postscript, повернутий функцією
[ps_new()](function.ps-new.md).

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
Параметр `dest` визначає спосіб перегляду документа. Може бути:
`fitpage`, `fitwidth`, `fitheight` або `fitbbox`.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Дивіться також

- [ps_add_launchlink()](function.ps-add-launchlink.md) - Додає
посилання, що запускає файл
- [ps_add_pdflink()](function.ps-add-pdflink.md) - Додає посилання
на сторінку в іншому PDF-документі
- [ps_add_weblink()](function.ps-add-weblink.md) - Додає посилання
на веб-сторінку
