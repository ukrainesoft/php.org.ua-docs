---
navigation:
  - function.gzinflate.md: « gzinflate
  - function.gzpassthru.md: gzpassthru »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: gzopen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# gzopen

(PHP 4, PHP 5, PHP 7, PHP 8)

gzopen — Відкрити файл gz

### Опис

```methodsynopsis
gzopen(string $filename, string $mode, int $use_include_path = 0): resource|false
```

Відкриває файл gzip (.gz) для читання чи запису.

**gzopen()** також можна використовувати для читання стиснених файлів (тобто не у форматі gzip). В цьому випадку [gzread()](function.gzread.md) безпосередньо читати файл без будь-якої обробки.

### Список параметрів

`filename`

Ім'я файлу.

`mode`

Як в [fopen()](function.fopen.md) `rb`или`wb`), але також може включати рівень стиснення (`wb9`) або стратегію: `f` для фільтрації даних як у `wb6f` `h`для сжатия`тільки за алгоритмом Хаффмана`, як в `wb1h` (Для більш детальної інформації про параметр стратегії дивіться опис `deflateInit2`в zlib.h).

`use_include_path`

Якщо ви хочете, щоб пошук файлу виконувався також у директоріях [include\_path](ini.core.md#ini.include-path), встановіть значення цього аргументу в

### Значення, що повертаються

Повертає покажчик на відкритий файл, після чого все, що ви читаєте з цього дескриптора, автоматично розпаковуватиметься, а все, що ви записуєте - упаковуватиметеся.

В случае возникновения ошибки функция возвращает\*\*`false`\*\*

### Приклади

**Приклад #1 Приклад використання** gzopen()\*\*\*\*

```php
<?php
$fp = gzopen("/tmp/file.gz", "r");
?>
```

### Дивіться також

-   [gzclose()](function.gzclose.md) \- Закрити вказівник відкритого gz-файлу
