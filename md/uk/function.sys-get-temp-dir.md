---
navigation:
  - function.set-time-limit.md: « set\_time\_limit
  - function.version-compare.md: version\_compare »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: sys\_get\_temp\_dir
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sys\_get\_temp\_dir

(PHP 5 >= 5.2.1, PHP 7, PHP 8)

sys\_get\_temp\_dir — Повертає шлях до директорії тимчасових файлів

### Опис

```methodsynopsis
sys_get_temp_dir(): string
```

Повертає шлях до директорії, де PHP за замовчуванням зберігає тимчасові файли.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає шлях до директорії тимчасових файлів.

### Приклади

**Пример #1 Пример использования**sys\_get\_temp\_dir()\*\*\*\*

```php
<?php
// Создание временного файла в директории
// временных файлов, используя sys_get_temp_dir()
$temp_file = tempnam(sys_get_temp_dir(), 'Tux');

echo $temp_file;
?>
```

Висновок наведеного прикладу буде схожим на:

```
C:\Windows\Temp\TuxA318.tmp
```

### Дивіться також

-   [tmpfile()](function.tmpfile.md) \- Створює тимчасовий файл
-   [tempnam()](function.tempnam.md) \- Створює файл із унікальним ім'ям
