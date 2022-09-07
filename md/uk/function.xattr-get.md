---
navigation:
  - ref.xattr.md: « xattr Функции
  - function.xattr-list.md: xattrlist »
  - index.md: PHP Manual
  - ref.xattr.md: xattr Функции
title: xattrget
---
# xattrget

(PECL xattr >= 0.9.0)

xattrget — отримання розширених атрибутів файлу

### Опис

```methodsynopsis
xattr_get(string $filename, string $name, int $flags = 0): string
```

Ця функція повертає значення розширеного атрибута файлу.

Розширені атрибути мають два різні простори імен: користувальницьке та кореневе (root). Користувальницький простір імен доступний для всіх користувачів, в той час як кореневе - тільки для користувачів з root-привілеями. За умовчанням xattr оперує в просторі імен, але ви можете змінити цю поведінку за допомогою аргументу `flags`

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

-   [xattrlist()](function.xattr-list.md) - Перегляд списку розширених атрибутів файлу
-   [xattrset()](function.xattr-set.md) - Встановлення розширених атрибутів файлу
-   [xattrremove()](function.xattr-remove.md) - Видалення розширених атрибутів файлу
