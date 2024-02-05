---
navigation:
  - ref.xdiff.md: « Функції xdiff
  - function.xdiff-file-bdiff.md: xdiff\_file\_bdiff »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_file\_bdiff\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_file\_bdiff\_size

(PECL xdiff >= 1.5.0)

xdiff\_file\_bdiff\_size — Отримати розмір файлу після застосування бінарного патчу

### Опис

```methodsynopsis
xdiff_file_bdiff_size(string $file): int
```

Повертає розмір файлу, який буде створено після застосування бінарного патчу з файлу `file`

### Список параметрів

`file`

Путь к бинарному патчу, созданному функциями[xdiff\_string\_bdiff()](function.xdiff-string-bdiff.md) або [xdiff\_string\_rabdiff()](function.xdiff-string-rabdiff.md)

### Значення, що повертаються

Повертає розмір файлу, який буде створено.

### Приклади

**Пример #1 Пример использования**xdiff\_file\_bdiff\_size()\*\*\*\*

Наступний код отримує розмір файлу, створеного після застосування патча.

```php
<?php
$length = xdiff_string_bdiff_size('file.bdiff');
echo "Размер результирующего файла будет $length байт";
?>
```

### Дивіться також

-   [xdiff\_file\_bdiff()](function.xdiff-file-bdiff.md) \- Створити бінарний патч порівнюючи два файли
-   [xdiff\_file\_rabdiff()](function.xdiff-file-rabdiff.md) \- Створити бінарний патч порівнюючи два файли за допомогою поліномінального алгоритму Rabin fingerprinting
-   [xdiff\_file\_bpatch()](function.xdiff-file-bpatch.md) \- Застосувати бінарний патч до файлу
