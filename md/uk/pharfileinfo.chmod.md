---
navigation:
  - class.pharfileinfo.md: « PharFileInfo
  - pharfileinfo.compress.md: 'PharFileInfo::compress »'
  - index.md: PHP Manual
  - class.pharfileinfo.md: PharFileInfo
title: 'PharFileInfo::chmod'
---
# PharFileInfo::chmod

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

PharFileInfo::chmod — Встановлення прав доступу

### Опис

```methodsynopsis
public PharFileInfo::chmod(int $perms): void
```

**PharFileInfo::chmod()** дозволяє встановлювати біти дозволів на запуск та читання для файлів. Біти запису ігноруються, оскільки налаштовуються під час виконання на основі значення INI-змінної [phar.readonly](phar.configuration.md#ini.phar.readonly). Як і для будь-якого іншого функціоналу, що модифікує phar-архів, необхідно, щоб змінна [phar.readonly](phar.configuration.md#ini.phar.readonly) була відключена для успішної зміни прав на файл в архіві [Phar](class.phar.md). Архіви [PharData](class.phardata.md) немає таких обмежень.

### Список параметрів

`perms`

Дозволи (дивіться опис функції [chmod()](function.chmod.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Приклад використання **PharFileInfo::chmod()****

```php
<?php
// удалим, на всякий случай
@unlink('brandnewphar.phar');
try {
    $p = new Phar('brandnewphar.phar', 0, 'brandnewphar.phar');
    $p['file.sh'] = '#!/usr/local/lib/php
    <?php echo "привет"; ?>';
    // установим бит исполнрения
    $p['file.sh']->chmod(0555);
    var_dump($p['file.sh']->isExecutable());
} catch (Exception $e) {
    echo 'Не удалось создать/изменить phar: ', $e;
}
?>
```

Результат виконання цього прикладу:

```
bool(true)
```
