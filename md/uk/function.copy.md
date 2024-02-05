---
navigation:
  - function.clearstatcache.md: « clearstatcache
  - function.delete.md: delete »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# copy

(PHP 4, PHP 5, PHP 7, PHP 8)

copy — Копіює файл

### Опис

```methodsynopsis
copy(string $from, string $to, ?resource $context = null): bool
```

Копирует файл`from` у файл з ім'ям `to`

Якщо потрібно перейменувати файл, використовуйте функцію [rename()](function.rename.md)

### Список параметрів

`from`

Шлях до вихідного файлу.

`to`

Путь к целевому файлу. Если`to` є URL, то копіювання може завершитися помилкою, якщо обгортка URL не підтримує перезаписування існуючих файлів.

**Увага**

Якщо цільовий файл вже існує, він буде перезаписаний.

`context`

Коректний ресурс контексту, створений функцією [stream\_context\_create()](function.stream-context-create.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад использования функции**copy()\*\*\*\*

```php
<?php
$file = 'example.txt';
$newfile = 'example.txt.bak';

if (!copy($file, $newfile)) {
    echo "не удалось скопировать $file...\n";
}
?>
```

### Дивіться також

-   [move\_uploaded\_file()](function.move-uploaded-file.md) \- Переміщує завантажений файл у нове місце
-   [rename()](function.rename.md) \- Перейменовує файл або директорію
-   Розділ керівництва[Завантаження файлів](features.file-upload.md)"
