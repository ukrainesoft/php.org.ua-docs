---
navigation:
  - ref.xattr.md: « xattr Функції
  - function.xattr-list.md: xattr\_list »
  - index.md: PHP Manual
  - ref.xattr.md: xattr Функції
title: xattr\_get
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xattr\_get

(PECL xattr >= 0.9.0)

xattr\_get — отримання розширених атрибутів файлу

### Опис

```methodsynopsis
xattr_get(string $filename, string $name, int $flags = 0): string
```

Ця функція повертає значення розширеного атрибута файлу.

У розширених атрибутів два простори імен: і кореневе (root). Користувальницький простір імен доступний для всіх користувачів, в той час як кореневе - тільки для користувачів з root-привілеями. За умовчанням xattr оперує в просторі імен, але ви можете змінити цю поведінку за допомогою аргументу `flags`

### Список параметрів

`filename`

Файл, атрибут якого потрібно прочитати.

`name`

Ім'я атрибуту.

`flags`

<table class="doctable table"><caption><strong>Підтримувані xattr-прапори</strong></caption><tbody class="tbody"><tr><td><strong><code>XATTR_DONTFOLLOW</code></strong></td><td>Не розіменовувати символічні посилання, працювати з самим посиланням.</td></tr><tr><td><strong><code>XATTR_ROOT</code></strong></td><td>Встановити атрибут у кореневому просторі імен. Потрібні права суперкористувача.</td></tr></tbody></table>

### Значення, що повертаються

Функція повертає рядок, що містить значення \*\*`false`\*\*якщо атрибут не існує.

### Приклади

**Приклад #1 Перевірити, чи підписано файл системним адміністратором**

```php
<?php
$file = '/usr/local/sbin/some_binary';
$signature = xattr_get($file, 'Root signature', XATTR_ROOT);

/* ... check if $signature is valid ... */

?>
```

### Дивіться також

-   [xattr\_list()](function.xattr-list.md) \- Перегляд списку розширених атрибутів файлу
-   [xattr\_set()](function.xattr-set.md) \- Встановлення розширених атрибутів файлу
-   [xattr\_remove()](function.xattr-remove.md) \- Видалення розширених атрибутів файлу
