---
navigation:
  - context.params.md: « Параметри контексту
  - context.zlib.md: Zlib context options »
  - index.md: PHP Manual
  - context.md: Контекстні опції та параметри
title: Опції контексту Zip
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Опції контексту Zip

Опції контексту Zip - Список опцій контексту Zip

### Опис

Опції контексту Zip доступні для обгорток `zip`

### Опції

`password`

Використовується для вказівки пароля, який використовується для зашифрованих архівів.

### список змін

| Версия | Опис |
| --- | --- |
| PHP 7.2.0, PECL zip 1.14.0 | Добавлен параметр`password` |

### Приклади

**Приклад #1 Простий приклад використання `password`**

```php
<?php
// Читаем зашифрованный архив
$opts = array(
    'zip' => array(
        'password' => 'secret',
    ),
);
// создаём контекст...
$context = stream_context_create($opts);

// ...и используем его для получения данных
echo file_get_contents('zip://test.zip#test.txt', false, $context);

?>
```
