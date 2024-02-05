---
navigation:
  - function.realpath.md: « realpath
  - function.rewind.md: rewind »
  - index.md: PHP Manual
  - ref.filesystem.md: Функції файлової системи
title: rename
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# rename

(PHP 4, PHP 5, PHP 7, PHP 8)

rename — Перейменує файл або директорію

### Опис

```methodsynopsis
rename(string $from, string $to, ?resource $context = null): bool
```

Намагається перейменувати `from`в`to`, переносячи файл між директоріями, якщо потрібно. Якщо `to`существует, то он будет перезаписан. При переименовании директории с существующим`to` буде виведено попередження.

### Список параметрів

`from`

Старе ім'я.

> **Зауваження** :
> 
> Обгортка, що використовується в `from` *повинна* збігатися з обгорткою, що використовується в `to`

`to`

Нове ім'я

> **Зауваження**: У Windows, якщо `to` вже існує, він повинен бути доступним для запису. В іншому випадку **rename()** завершиться помилкою та видасть **`E_WARNING`**

`context`

Ресурс (resource) с[контекстом потоку](stream.contexts.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання функції** rename()\*\*\*\*

```php
<?php
rename("/tmp/tmp_file.txt", "/home/user/login/docs/my_file.txt");
?>
```

### Дивіться також

-   [copy()](function.copy.md) \- Копіює файл
-   [unlink()](function.unlink.md) \- Видаляє файл
-   [move\_uploaded\_file()](function.move-uploaded-file.md) \- Переміщує завантажений файл у нове місце
