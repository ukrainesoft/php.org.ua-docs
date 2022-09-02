---
navigation:
  - function.ps-begin-pattern.md: «psbeginpattern
  - function.ps-circle.md: псcircle »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псbegintemplate
---
# псbegintemplate

(PECL ps >= 1.2.0)

псbegintemplate — Починає новий шаблон

### Опис

```methodsynopsis
ps_begin_template(resource $psdoc, float $width, float $height): int
```

Починає новий шаблон. На мові postscript шаблон називається формою. Він створюється аналогічно візерунку, але використовується як зображення. Шаблони часто використовуються для малюнків, які розміщуються в документі кілька разів, наприклад, як логотип компанії. У шаблоні можна використовувати усі функції малювання. Шаблон не буде намальований, поки він не буде розміщений за допомогою [псplaceimage()](function.ps-place-image.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

`width`

Ширина шаблону в пікселях.

`height`

Висота шаблону в пікселях.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Створення та використання шаблону**

```php
<?php
$ps = ps_new();

if (!ps_open_file($ps, "template.ps")) {
  print "Не удаётся открыть файл PostScript\n";
  exit;
}

ps_set_parameter($ps, "warning", "true");
ps_set_info($ps, "Creator", "template.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример шаблона");

$pstemplate = ps_begin_template($ps, 30.0, 30.0);
ps_moveto($ps, 0, 0);
ps_lineto($ps, 30, 30);
ps_moveto($ps, 0, 30);
ps_lineto($ps, 30, 0);
ps_stroke($ps);
ps_end_template($ps);

ps_begin_page($ps, 596, 842);
ps_place_image($ps, $pstemplate, 20.0, 20.0, 1.0);
ps_place_image($ps, $pstemplate, 50.0, 30.0, 0.5);
ps_place_image($ps, $pstemplate, 70.0, 70.0, 0.6);
ps_place_image($ps, $pstemplate, 30.0, 50.0, 1.3);
ps_end_page($ps);

ps_close($ps);
ps_delete($ps);
?>
```

### Дивіться також

-   [псendtemplate()](function.ps-end-template.md) - Завершує шаблон
