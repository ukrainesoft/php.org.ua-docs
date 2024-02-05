---
navigation:
  - function.ps-lineto.md: « ps\_lineto
  - function.ps-moveto.md: ps\_moveto »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_makespotcolor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_makespotcolor

(PECL ps >= 1.1.0)

ps\_makespotcolor — Створює плашковий колір

### Опис

```methodsynopsis
ps_makespotcolor(resource $psdoc, string $name, int $reserved = 0): int
```

Створює плашковий колір із поточного кольору заливки. Колір заливки має бути визначений у колірному просторі rgb, cmyk або gray. Назва плашкового кольору може бути довільною. Плашковий колір може бути встановлений як будь-який колір за допомогою [ps\_setcolor()](function.ps-setcolor.md). Якщо документ не друкується, а відображається програмою перегляду PostScript, використовується заданий колір у зазначеному колірному просторі.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу PostScript-файлу, повернутий функцією [ps\_new()](function.ps-new.md)

`name`

Назва плашкового кольору, наприклад Pantone 5565.

### Значення, що повертаються

Ідентифікатор нового плашкового кольору або 0 у разі виникнення помилки.

### Приклади

**Приклад #1 Створення та використання плашкового кольору**

```php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "spotcolor.ps")) {
  print "Не удаётся открыть файл PostScript\n";
  exit;
}

ps_set_info($ps, "Creator", "spotcolor.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Приклад плашечного цвета");

ps_begin_page($ps, 596, 842);
ps_setcolor($ps, "fill", "cmyk", 0.37, 0.0, 0.34, 0.34);
$spotcolor = ps_makespotcolor($ps, "PANTONE 5565 C", 0);
ps_setcolor($ps, "fill", "spot", $spotcolor, 0.5, 0.0, 0.0);
ps_moveto($ps, 100, 100);
ps_lineto($ps, 100, 200);
ps_lineto($ps, 200, 200);
ps_lineto($ps, 200, 100);
ps_lineto($ps, 100, 100);
ps_fill($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

У цьому прикладі створюється плашковий колір "PANTONE 5565 C", який є темно-зеленим (оливковим) і заповнює прямокутник з інтенсивністю 50%.

### Дивіться також

-   [ps\_setcolor()](function.ps-setcolor.md) \- Встановлює поточний колір
