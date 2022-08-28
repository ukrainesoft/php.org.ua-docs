Встановлює коефіцієнт обертання

-   [« ps\_restore](function.ps-restore.html)
    
-   [ps\_save »](function.ps-save.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Встановлює коефіцієнт обертання
    

# псrotate

(PECL ps >= 1.1.0)

псrotate - Встановлює коефіцієнт обертання

### Опис

```methodsynopsis
ps_rotate(resource $psdoc, float $rot): bool
```

Встановлює поворот системи координат.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.html)

`rot`

Кут повороту у градусах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Обертання системи координат**

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
if (!ps_open_file($ps, "rotation.ps")) {
  print "Не удаётся открыть файл PostScript\n";
  exit;
}

ps_set_info($ps, "Creator", "rotation.php");
ps_set_info($ps, "Author", "Uwe Steinmann");
ps_set_info($ps, "Title", "Rotation example");
ps_set_info($ps, "BoundingBox", "0 0 596 842");

$psfont = ps_findfont($ps, "Helvetica", "", 0);

ps_begin_page($ps, 596, 842);
ps_set_text_pos($ps, 100, 100);
ps_save($ps);
ps_translate($ps, 100, 100);
ps_rotate($ps, 45);
rectangle($ps);
ps_restore($ps);
ps_setfont($ps, $psfont, 8.0);
ps_show($ps, "Текст без поворота");
ps_end_page($ps);

ps_delete($ps);
?>
```

У наведеному вище прикладі показаний дуже поширений спосіб повороту зображення (у разі просто прямокутника) шляхом повороту системи координат. Оскільки система координат графіки передбачає, що (0,0) є початком координат, система координат сторінки також перекладається, щоб розмістити графіку над краю сторінки. Зверніть увагу на порядок [ps\_translate()](function.ps-translate.html) і **псrotate()**. У наведеному вище прикладі прямокутник обертається навколо точки (100, 100) у непереведеній системі координат. Перемикання двох операторів дає зовсім інший результат.

Щоб вивести наступний текст у вихідній позиції, всі модифікації системи координат інкапсулюються в [ps\_save()](function.ps-save.html) і [ps\_restore()](function.ps-restore.html)

### Дивіться також

-   [ps\_scale()](function.ps-scale.html) - Встановлює коефіцієнт масштабування
-   [ps\_translate()](function.ps-translate.html) - Змінює систему координат