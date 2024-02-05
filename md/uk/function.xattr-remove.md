---
navigation:
  - function.xattr-list.md: « xattr\_list
  - function.xattr-set.md: xattr\_set »
  - index.md: PHP Manual
  - ref.xattr.md: xattr Функції
title: xattr\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xattr\_remove

(PECL xattr >= 0.9.0)

xattr\_remove — Видалення розширених атрибутів файлу

### Опис

```methodsynopsis
xattr_remove(string $filename, string $name, int $flags = 0): bool
```

Ця функція видаляє розширений атрибут файлу.

У розширених атрибутів два простори імен: і кореневе (root). Користувальницький простір імен доступний для всіх користувачів, в той час як кореневе - тільки для користувачів з root-привілеями. За умовчанням xattr оперує в просторі імен, але ви можете змінити цю поведінку за допомогою аргументу `flags`

### Список параметрів

`filename`

Файл, атрибут якого потрібно видалити.

`name`

Ім'я атрибута, що видаляється.

`flags`

<table class="doctable table"><caption><strong>Підтримувані xattr-прапори</strong></caption><tbody class="tbody"><tr><td><strong><code>XATTR_DONTFOLLOW</code></strong></td><td>Не розіменовувати символічні посилання, працювати з самим посиланням.</td></tr><tr><td><strong><code>XATTR_ROOT</code></strong></td><td>Встановити атрибут у кореневому просторі імен. Потрібні права суперкористувача.</td></tr></tbody></table>

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Видалити всі розширені атрибути файлу**

```php
<?php
$file = 'some_file';
$attributes = xattr_list($file);

foreach ($attributes as $attr_name) {
    xattr_remove($file, $attr_name);
}
?>
```

### Дивіться також

-   [xattr\_list()](function.xattr-list.md) \- Перегляд списку розширених атрибутів файлу
-   [xattr\_set()](function.xattr-set.md) \- Встановлення розширених атрибутів файлу
-   [xattr\_get()](function.xattr-get.md) \- Отримання розширених атрибутів файлу
