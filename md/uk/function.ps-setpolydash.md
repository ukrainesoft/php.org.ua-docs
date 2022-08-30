Встановлює зовнішній вигляд пунктирної лінії

-   [«pssetoverprintmode](function.ps-setoverprintmode.html)
    
-   [псshadingpattern »](function.ps-shading-pattern.html)
    
-   [PHP Manual](index.md)
    
-   [Функції PS](ref.ps.md)
    
-   Встановлює зовнішній вигляд пунктирної лінії
    

# псsetpolydash

(PECL ps >= 1.1.0)

псsetpolydash - Встановлює зовнішній вигляд пунктирної лінії

### Опис

```methodsynopsis
ps_setpolydash(resource $psdoc, float $arr): bool
```

Встановлює довжину чорних та білих частин пунктирної лінії. . **псsetpolydash()** використовується для встановлення складніших шаблонів тире.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.html)

`arr`

`arr` - це список елементів довжини по черзі для чорної та білої частини.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Малювання пунктирної лінії**

```php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "polydash.ps")) {
   print "Не удаётся открыть файл PostScript\n";
     exit;
}

ps_set_info($ps, "Creator", "polydash.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример множественного тире");

ps_begin_page($ps, 596, 842);
ps_setpolydash($ps, array(10, 5, 2, 5));
ps_moveto($ps, 100, 100);
ps_lineto($ps, 200, 200);
ps_stroke($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

У цьому прикладі малюється лінія з 10 і 2 точок з проміжками 5 точок між ними.

### Дивіться також

-   [псsetdash()](function.ps-setdash.html) - Встановлює зовнішній вигляд пунктирної лінії