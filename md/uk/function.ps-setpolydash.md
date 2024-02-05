---
navigation:
  - function.ps-setoverprintmode.md: « ps\_setoverprintmode
  - function.ps-shading-pattern.md: ps\_shading\_pattern »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_setpolydash
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_setpolydash

(PECL ps >= 1.1.0)

ps\_setpolydash - Встановлює зовнішній вигляд пунктирної лінії

### Опис

```methodsynopsis
ps_setpolydash(resource $psdoc, float $arr): bool
```

Встановлює довжину чорних та білих частин пунктирної лінії. . **ps\_setpolydash()** використовується для встановлення складніших шаблонів тире.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`arr`

`arr` - це список елементів довжини по черзі для чорної та білої частини.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Малювання пунктирної лінії**

```php
<?php
$ps = ps_new();
if (!ps_open_file($ps, "polydash.ps")) {
   print "Не удаётся открыть файл PostScript\n";
     exit;
}

ps_set_info($ps, "Creator", "polydash.php");
ps_set_info($ps, "Author", "Уве Штайнманн");
ps_set_info($ps, "Title", "Пример множественного тире");

ps_begin_page($ps, 596, 842);
ps_setpolydash($ps, array(10, 5, 2, 5));
ps_moveto($ps, 100, 100);
ps_lineto($ps, 200, 200);
ps_stroke($ps);
ps_end_page($ps);

ps_delete($ps);
?>
```

У цьому прикладі малюється лінія з 10 і 2 точок з проміжками 5 точок між ними.

### Дивіться також

-   [ps\_setdash()](function.ps-setdash.md) \- Встановлює зовнішній вигляд пунктирної лінії
