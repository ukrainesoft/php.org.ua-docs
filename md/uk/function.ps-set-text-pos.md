---
navigation:
  - function.ps-set-parameter.md: «pssetparameter
  - function.ps-set-value.md: псsetvalue »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псsettextpos
---
# псsettextpos

(PECL ps >= 1.1.0)

псsettextpos — Встановлює позицію для виведення тексту

### Опис

```methodsynopsis
ps_set_text_pos(resource $psdoc, float $x, float $y): bool
```

Встановлює позицію наступного виведення тексту. Можна встановити значення X та Y окремо, викликавши [псsetvalue()](function.ps-set-value.md) і вибравши `textx` або `texty` відповідно як ім'я значення.

Для виведення тексту в певному місці зручніше використовувати [псshowxy()](function.ps-show-xy.md) замість встановлення позиції тексту та виклику [псshow()](function.ps-show.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

`x`

Координата X нова позиція тексту.

`y`

Координата Y нова позиція тексту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Розміщення тексту на заданій позиції**

```php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "text.ps")) {
  print "Не удается открыть файл PostScript\n";
  exit;
}

ps_set_info($ps, "Creator", "rectangle.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример размещения текста");

ps_begin_page($ps, 596, 842);
$psfont = ps_findfont($ps, "Helvetica", "", 0);
ps_setfont($ps, $psfont, 8.0);
ps_show_xy($ps, "Some text at (100, 100)", 100, 100);

ps_set_value($ps, "textx", 100);
ps_set_value($ps, "texty", 120);
ps_show($ps, "Some text at (100, 120)");
ps_end_page($ps);

ps_delete($ps);
?>
```

### Дивіться також

-   [псsetvalue()](function.ps-set-value.md) - Встановлює певні значення
-   [псshow()](function.ps-show.md) - Виводить текст
