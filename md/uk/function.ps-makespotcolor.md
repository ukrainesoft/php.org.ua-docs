Створює плашковий колір

-   [«pslineto](function.ps-lineto.html)
    
-   [псmoveto »](function.ps-moveto.html)
    
-   [PHP Manual](index.html)
    
-   [Функції PS](ref.ps.html)
    
-   Створює плашковий колір
    

# псmakespotcolor

(PECL ps >= 1.1.0)

псmakespotcolor — Створює плашковий колір

### Опис

```methodsynopsis
ps_makespotcolor(resource $psdoc, string $name, int $reserved = 0): int
```

Створює плашковий колір із поточного кольору заливки. Колір заливки має бути визначений у колірному просторі rgb, cmyk або gray. Назва плашкового кольору може бути довільною. Плашковий колір може бути встановлений як будь-який колір за допомогою [псsetcolor()](function.ps-setcolor.html). Якщо документ не друкується, а відображається програмою перегляду PostScript, використовується заданий колір у зазначеному просторі.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу PostScript-файлу, повернутий функцією [псnew()](function.ps-new.html)

`name`

Назва плашкового кольору, наприклад Pantone 5565.

### Значення, що повертаються

Ідентифікатор нового плашкового кольору або 0 у разі виникнення помилки.

### Приклади

**Приклад #1 Створення та використання плашкового кольору**

```php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "spotcolor.ps")) {
  print "Не удаётся открыть файл PostScript\n";
  exit;
}

ps_set_info($ps, "Creator", "spotcolor.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример плашечного цвета");

ps_begin_page($ps, 596, 842);
ps_setcolor($ps, "fill", "cmyk", 0.37, 0.0, 0.34, 0.34);
$spotcolor = ps_makespotcolor($ps, "PANTONE 5565 C", 0);
ps_setcolor($ps, "fill", "spot", $spotcolor, 0.5, 0.0, 0.0);
ps_moveto($ps, 100, 100);
ps_lineto($ps, 100, 200);
ps_lineto($ps, 200, 200);
ps_lineto($ps, 200, 100);
ps_lineto($ps, 100, 100);
ps_fill($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

У цьому прикладі створюється плашковий колір "PANTONE 5565 C", який є темно-зеленим (оливковим) і заповнює прямокутник з інтенсивністю 50%.

### Дивіться також

-   [псsetcolor()](function.ps-setcolor.html) - Встановлює поточний колір