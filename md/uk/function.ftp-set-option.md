---
navigation:
  - function.ftp-rmdir.md: « ftp\_rmdir
  - function.ftp-site.md: ftp\_site »
  - index.md: PHP Manual
  - ref.ftp.md: Функції FTP
title: ftp\_set\_option
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ftp\_set\_option

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ftp\_set\_option — Встановлює параметри з'єднання з сервером FTP

### Опис

```methodsynopsis
ftp_set_option(FTP\Connection $ftp, int $option, int|bool $value): bool
```

Ця функція визначає параметри з'єднання з FTP-сервером.

### Список параметрів

`ftp`

An[FTP\\Connection](class.ftp-connection.md)instance.

`option`

В даний час підтримуються такі параметри:

<table class="doctable table"><caption><strong>Підтримувані параметри</strong></caption><tbody class="tbody"><tr><td><strong><code>FTP_TIMEOUT_SEC</code></strong></td><td>Встановлює час очікування мережевих операцій у секундах. Аргумент <code class="parameter">value</code> повинен бути цілим, більше 0. За замовчуванням час очікування дорівнює 90 секундам.</td></tr><tr><td><strong><code>FTP_AUTOSEEK</code></strong></td><td>При встановленні цього параметра перед виконанням запитів GET або PUT з параметром <code class="parameter">resumepos</code> або <code class="parameter">startpos </code>покажчик файлу буде встановлений на запитану позицію. Цей параметр встановлено за замовчуванням.</td></tr><tr><td><strong><code>FTP_USEPASVADDRESS</code></strong></td><td>Якщо вимкнено, то PHP ігноруватиме IP -адреса, повернена сервером у відповідь на команду PASV і замість нього буде використовувати IP-адресу, передану в ftp_connect(). Параметр <code class="parameter">value</code> повинен містити логічне значення.</td></tr></tbody></table>

`value`

Призначення цього аргументу залежить від значення параметра `option`

### Значення, що повертаються

Повертає **`true`** якщо параметр було встановлено; **`false`** в іншому випадку. Якщо значення аргументу `option` не підтримується або значення аргументу `value`не соответствует значению аргумента`option`, буде виведено попередження

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ftp` тепер чекає екземпляр [FTP\\Connection](class.ftp-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**ftp\_set\_option()\*\*\*\*

```php
<?php
// установка времени ожидания в 10 секунд
ftp_set_option($ftp, FTP_TIMEOUT_SEC, 10);
?>
```

### Дивіться також

-   [ftp\_get\_option()](function.ftp-get-option.md) \- Отримує поточні параметри FTP-з'єднання
