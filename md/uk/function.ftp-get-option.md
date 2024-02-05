---
navigation:
  - function.ftp-fput.md: « ftp\_fput
  - function.ftp-get.md: ftp\_get »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_get\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_get\_option

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ftp\_get\_option — Отримує поточні параметри FTP-з'єднання.

### Опис

```methodsynopsis
ftp_get_option(FTP\Connection $ftp, int $option): int|bool
```

Ця функція повертає значення запитаної опції `option` для зазначеного FTP-з'єднання.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`option`

На даний момент підтримуються такі опції:

<table class="doctable table"><caption><strong>Підтримувані поточні опції FTP</strong></caption><tbody class="tbody"><tr><td><strong><code>FTP_TIMEOUT_SEC</code></strong></td><td>Повертає поточний час очікування, що використовується в мережевих операціях.</td></tr><tr><td><strong><code>FTP_AUTOSEEK</code></strong></td><td>Повертає <strong><code>true</code></strong>, якщо цю опцію увімкнено, інакше <strong><code>false</code></strong>.. td&gt;</td></tr></tbody></table>

### Значення, що повертаються

Повертає значення у разі успішного виконання, або **`false`**, якщо вказана опція `option` не підтримується. У разі також викликається попередження.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** ftp\_get\_option()\*\*\*\*

```php
<?php
// Получаем время ожидания соединения
$timeout = ftp_get_option($ftp, FTP_TIMEOUT_SEC);
?>
```

### Дивіться також

-   [ftp\_set\_option()](function.ftp-set-option.md) \- Встановлює параметри з'єднання з FTP-сервером
