Змінює систему координат

-   [« ps\_symbol](function.ps-symbol.html)
    
-   [RpmInfo »](book.rpminfo.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Змінює систему координат
    

# псtranslate

(PECL ps >= 1.1.0)

псtranslate — Змінює систему координат

### Опис

```methodsynopsis
ps_translate(resource $psdoc, float $x, float $y): bool
```

Встановлює нову початкову точку системи координат.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.html)

`x`

Координата X почала зміненої системи координат.

`y`

Координата Y почала зміненої системи координат.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Зміна системи координат**

```php
<?php
function rectangle($ps) {
    ps_moveto($ps, 0, 0);
    ps_lineto($ps, 0, 50);
    ps_lineto($ps, 50, 50);
    ps_lineto($ps, 50, 0);
    ps_lineto($ps, 0, 0);
    ps_stroke($ps);
}

$ps = ps_new();
if (!ps_open_file($ps, "translate.ps")) {
  print "Не удается открыть файл PostScript\n";
  exit;
}

ps_set_info($ps, "Creator", "translate.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример перевода");
ps_set_info($ps, "BoundingBox", "0 0 596 842");

$psfont = ps_findfont($ps, "Helvetica", "", 0);

ps_begin_page($ps, 596, 842);
ps_set_text_pos($ps, 100, 100);
ps_translate($ps, 500, 750);
rectangle($ps);
ps_translate($ps, -500, -750);
ps_setfont($ps, $psfont, 8.0);
ps_show($ps, "Текст в исходной позиции");
ps_end_page($ps);

ps_begin_page($ps, 596, 842);
ps_set_text_pos($ps, 100, 100);
ps_save($ps);
ps_translate($ps, 500, 750);
rectangle($ps);
ps_restore($ps);
ps_setfont($ps, $psfont, 8.0);
ps_show($ps, "Текст в исходной позиции");
ps_end_page($ps);

ps_delete($ps);
?>
```

Наведений вище приклад демонструє два можливі способи розмістити графіку (у разі просто прямокутник) у будь-якій позиції сторінці, тоді як сама графіка використовує власну систему координат. Хитрість у тому, щоб змінити початок поточної системи координат перед малюванням прямокутника. Зміну системи координат необхідно скасувати після того, як малюнок було намальовано.

На другій сторінці застосований дещо інший і елегантніший підхід. Замість скасування зміни другим викликом **псtranslate()**, графічний контекст зберігається до зміни системи координат та відновлюється після малювання прямокутника.

### Дивіться також

-   [ps\_scale()](function.ps-scale.html) - Встановлює коефіцієнт масштабування
-   [ps\_rotate()](function.ps-rotate.html) - Встановлює коефіцієнт обертання