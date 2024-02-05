---
navigation:
  - function.ps-set-parameter.md: « ps\_set\_parameter
  - function.ps-set-value.md: ps\_set\_value »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_set\_text\_pos
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_set\_text\_pos

(PECL ps >= 1.1.0)

ps\_set\_text\_pos — Встановлює позицію для виведення тексту

### Опис

```methodsynopsis
ps_set_text_pos(resource $psdoc, float $x, float $y): bool
```

Встановлює позицію наступного виведення тексту. Можна встановити значення X та Y окремо, викликавши [ps\_set\_value()](function.ps-set-value.md) і вибравши `textx`или`texty`соответственно в качестве имени значения.

Для виведення тексту в певному місці зручніше використовувати [ps\_show\_xy()](function.ps-show-xy.md) замість встановлення позиції тексту та виклику [ps\_show()](function.ps-show.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`x`

Координата X нова позиція тексту.

`y`

Координата Y нова позиція тексту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Розміщення тексту на заданій позиції**

```php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "text.ps")) {
  print "Не удается открыть файл PostScript\n";
  exit;
}

ps_set_info($ps, "Creator", "rectangle.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Приклад размещения текста");

ps_begin_page($ps, 596, 842);
$psfont = ps_findfont($ps, "Helvetica", "", 0);
ps_setfont($ps, $psfont, 8.0);
ps_show_xy($ps, "Some text at (100, 100)", 100, 100);

ps_set_value($ps, "textx", 100);
ps_set_value($ps, "texty", 120);
ps_show($ps, "Some text at (100, 120)");
ps_end_page($ps);

ps_delete($ps);
?>
```

### Дивіться також

-   [ps\_set\_value()](function.ps-set-value.md) \- Встановлює певні значення
-   [ps\_show()](function.ps-show.md) \- Виводить текст
