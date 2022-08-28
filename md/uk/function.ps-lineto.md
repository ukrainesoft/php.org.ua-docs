Малює лінію

-   [« ps\_include\_file](function.ps-include-file.html)
    
-   [ps\_makespotcolor »](function.ps-makespotcolor.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PS](ref.ps.html)
    
-   Малює лінію
    

# псlineto

(PECL ps >= 1.1.0)

псlineto — Малює лінію

### Опис

```methodsynopsis
ps_lineto(resource $psdoc, float $x, float $y): bool
```

Додає до поточного шляху пряму лінію від точки до заданих координат. Використовуйте [ps\_moveto()](function.ps-moveto.html), щоб встановити початкову точку лінії.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.html)

`x`

Координата X кінцевої точки лінії.

`y`

Координата Y кінцевої точки лінії.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Малювання прямокутника**

```php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "rectangle.ps")) {
  print "Не удаётся открыть файл PostScript\n";
  exit;
}

ps_set_info($ps, "Creator", "rectangle.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример Линето");

ps_begin_page($ps, 596, 842);
ps_moveto($ps, 100, 100);
ps_lineto($ps, 100, 200);
ps_lineto($ps, 200, 200);
ps_lineto($ps, 200, 100);
ps_lineto($ps, 100, 100);
ps_stroke($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

### Дивіться також

-   [ps\_moveto()](function.ps-moveto.html) - Встановлює поточну точку