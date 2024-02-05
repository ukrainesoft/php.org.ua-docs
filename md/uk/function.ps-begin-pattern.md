---
navigation:
  - function.ps-begin-page.md: « ps\_begin\_page
  - function.ps-begin-template.md: ps\_begin\_template »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_begin\_pattern
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_begin\_pattern

(PECL ps >= 1.2.0)

ps\_begin\_pattern — Починає новий візерунок

### Опис

```methodsynopsis
ps_begin_pattern(    resource $psdoc,    float $width,    float $height,    float $xstep,    float $ystep,    int $painttype): int|false
```

Починає новий візерунок. Візерунок схожий на сторінку, що містить, наприклад, малюнок, який можна використовувати для заливання областей. Він використовується як колір, викликаючи [ps\_setcolor()](function.ps-setcolor.md)и устанавливая цветовое пространство в`pattern`

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`width`

Ширина візерунка у пікселях.

`height`

Висота візерунка в пікселях.

`x-step`

Відстань у пікселях розміщення візерунка по горизонталі.

`y-step`

Відстань у пікселях розміщення візерунка по вертикалі.

`painttype`

Можливо 1 або 2.

### Значення, що повертаються

Ідентифікатор візерунка або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Створення та використання візерунка**

```php
<?php
$ps = ps_new();

if (!ps_open_file($ps, "pattern.ps")) {
  print "Не удаётся открыть файл PostScript\n";
  exit;
}

ps_set_parameter($ps, "warning", "true");
ps_set_info($ps, "Creator", "pattern.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример узора");


$pspattern = ps_begin_pattern($ps, 10.0, 10.0, 10.0, 10.0, 1);
ps_setlinewidth($ps, 0.2);
ps_setcolor($ps, "stroke", "rgb", 0.0, 0.0, 1.0, 0.0);
ps_moveto($ps, 0, 0);
ps_lineto($ps, 7, 7);
ps_stroke($ps);
ps_moveto($ps, 0, 7);
ps_lineto($ps, 7, 0);
ps_stroke($ps);
ps_end_pattern($ps);

ps_begin_page($ps, 596, 842);
ps_setcolor($ps, "both", "pattern", $pspattern, 0.0, 0.0, 0.0);
ps_rect($ps, 50, 400, 200, 200);
ps_fill($ps);
ps_end_page($ps);

ps_close($ps);
ps_delete($ps);
?>
```

### Дивіться також

-   [ps\_end\_pattern()](function.ps-end-pattern.md) \- Завершує шаблон
-   [ps\_setcolor()](function.ps-setcolor.md) \- Встановлює поточний колір
-   [ps\_shading\_pattern()](function.ps-shading-pattern.md) \- Створює візерунок на основі затінення
