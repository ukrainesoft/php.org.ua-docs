---
navigation:
  - function.xattr-remove.md: « xattr\_remove
  - function.xattr-supported.md: xattr\_supported »
  - index.md: PHP Manual
  - ref.xattr.md: xattr Функції
title: xattr\_set
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xattr\_set

(PECL xattr >= 0.9.0)

xattr\_set — Встановлення розширених атрибутів файлу

### Опис

```methodsynopsis
xattr_set(    string $filename,    string $name,    string $value,    int $flags = 0): bool
```

Ця функція встановлює розширений атрибут файлу.

У розширених атрибутів два простори імен: і кореневе (root). Користувальницький простір імен доступний для всіх користувачів, в той час як кореневе - тільки для користувачів з root-привілеями. За умовчанням xattr оперує в просторі імен, але ви можете змінити цю поведінку за допомогою аргументу `flags`

### Список параметрів

`filename`

Ім'я файлу, атрибут якого потрібно встановити.

`name`

Назва розширеного атрибута. За його відсутності атрибут створюється, інакше - перезаписується. Ви можете змінити поведінку, використовуючи прапори (`flags`

`value`

Значення атрибуту.

`flags`

< td>Не розіменовувати символічні посилання, працювати з самим посиланням.

<table class="doctable table"><caption><strong>Підтримувані xattr-прапори</strong></caption><tbody class="tbody"><tr><td><strong><code>XATTR_CREATE</code></strong></td><td>Функція поверне помилку, якщо атрибут існує.</td></tr><tr><td><strong><code>XATTR_REPLACE</code></strong></td><td>Функція поверне помилку, якщо атрибут не існує.</td></tr><tr><td><strong><code>XATTR_DONTFOLLOW</code></strong></td></tr><tr><td><strong><code>XATTR_ROOT</code></strong></td><td>Встановити атрибут у кореневому просторі імен. Потрібні права суперкористувача.</td></tr></tbody></table>

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Встановити розширені атрибути .wav файлу**

```php
<?php
$file = 'my_favourite_song.wav';
xattr_set($file, 'Artist', 'Someone');
xattr_set($file, 'My ranking', 'Good');
xattr_set($file, 'Listen count', '34');

/* ... other code ... */

printf("You've played this song %d times", xattr_get($file, 'Listen count'));
?>
```

### Дивіться також

-   [xattr\_get()](function.xattr-get.md) \- Отримання розширених атрибутів файлу
-   [xattr\_remove()](function.xattr-remove.md) \- Видалення розширених атрибутів файлу
