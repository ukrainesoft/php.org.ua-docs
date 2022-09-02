---
navigation:
  - function.ftp-fput.md: « ftpfput
  - function.ftp-get.md: ftpget »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftpgetoption
---
# ftpgetoption

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ftpgetoption — Отримує поточні параметри FTP-з'єднання.

### Опис

```methodsynopsis
ftp_get_option(FTP\Connection $ftp, int $option): int|bool
```

Ця функція повертає значення запитаної опції `option` для зазначеного FTP-з'єднання.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.md) instance.

`option`

На даний момент підтримуються такі опції:

<table class="doctable table"><caption><strong>Підтримувані поточні опції FTP</strong></caption><tbody class="tbody"><tr><td><strong><code>FTP_TIMEOUT_SEC</code></strong></td><td>Повертає поточний час очікування, що використовується в мережевих операціях.</td></tr><tr><td><strong><code>FTP_AUTOSEEK</code></strong></td><td>Повертає <strong><code>true</code></strong>, якщо цю опцію увімкнено, інакше <strong><code>false</code></strong>.. td&gt;</td></tr></tbody></table>

### Значення, що повертаються

Повертає значення у разі успішного виконання, або **`false`**, якщо вказана опція `option` не підтримується. У разі також викликається попередження.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **ftpgetoption()****

```php
<?php
// Получаем время ожидания соединения
$timeout = ftp_get_option($ftp, FTP_TIMEOUT_SEC);
?>
```

### Дивіться також

-   [ftpsetoption()](function.ftp-set-option.md) - Встановлює параметри з'єднання з FTP-сервером
