---
navigation:
  - function.bind-textdomain-codeset.md: « bind\_textdomain\_codeset
  - function.dcgettext.md: dcgettext »
  - index.md: PHP Manual
  - ref.gettext.md: Функції gettext
title: bindtextdomain
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# bindtextdomain

(PHP 4, PHP 5, PHP 7, PHP 8)

bindtextdomain — Встановлює або отримує шлях для домену

### Опис

```methodsynopsis
bindtextdomain(string $domain, ?string $directory): string|false
```

Функция**bindtextdomain()** встановлює чи отримує шлях для домену.

### Список параметрів

`domain`

Домен.

`directory`

Шлях до директорії. Порожній рядок означає поточний каталог. Якщо **`null`**, повертається поточний встановлений каталог.

### Значення, що повертаються

Повний шлях для домену, встановленого параметром `domain`или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.3 | `directory` тепер допускає значення null. Раніше неможливо було отримати поточний встановлений каталог. |

### Приклади

**Пример #1 Пример использования**bindtextdomain()\*\*\*\*

```php
<?php

$domain = 'myapp';
echo bindtextdomain($domain, '/usr/share/myapp/locale');

?>
```

Результат виконання наведеного прикладу:

```
/usr/share/myapp/locale
```

### Примітки

> **Зауваження** :
> 
> Інформація **bindtextdomain()** зберігається кожному за процесу, а чи не для потоку.
