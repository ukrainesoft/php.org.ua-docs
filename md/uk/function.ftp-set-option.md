Встановлює параметри з'єднання з сервером FTP

-   [« ftprmdir](function.ftp-rmdir.html)
    
-   [ftpsite »](function.ftp-site.html)
    
-   [PHP Manual](index.html)
    
-   [Функції FTP](ref.ftp.html)
    
-   Встановлює параметри з'єднання з сервером FTP
    

# ftpsetoption

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ftpsetoption — Встановлює параметри з'єднання з сервером FTP

### Опис

```methodsynopsis
ftp_set_option(FTP\Connection $ftp, int $option, int|bool $value): bool
```

Ця функція визначає параметри з'єднання з FTP-сервером.

### Список параметрів

`ftp`

Ан [FTPConnection](class.ftp-connection.html) instance.

`option`

В даний час підтримуються такі параметри:

<table class="doctable table"><caption><strong>Підтримувані параметри</strong></caption><tbody class="tbody"><tr><td><strong><code>FTP_TIMEOUT_SEC</code></strong></td><td>Встановлює час очікування мережевих операцій у секундах. Аргумент <code class="parameter">value</code> повинен бути цілим, більше 0. За замовчуванням час очікування дорівнює 90 секундам.</td></tr><tr><td><strong><code>FTP_AUTOSEEK</code></strong></td><td>При встановленні цього параметра перед виконанням запитів GET або PUT з параметром <code class="parameter">resumepos</code> або <code class="parameter">startpos </code>покажчик файлу буде встановлений на запитану позицію. Цей параметр встановлено за замовчуванням.</td></tr><tr><td><strong><code>FTP_USEPASVADDRESS</code></strong></td><td>Якщо вимкнено, то PHP ігноруватиме IP -адреса, повернена сервером у відповідь на команду PASV і замість нього буде використовувати IP-адресу, передану в ftp_connect(). Параметр <code class="parameter">value</code> має містити логічне значення.</td></tr></tbody></table>

`value`

Призначення цього аргументу залежить від значення параметра `option`

### Значення, що повертаються

Повертає **`true`** якщо параметр було встановлено; **`false`** в іншому випадку. Якщо значення аргументу `option` не підтримується або значення аргументу `value` не відповідає значенню аргументу `option`, буде виведено попередження

### список змін

| Версия | Описание                                                                                                                                            |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
|        | Параметр `ftp` тепер чекає екземпляр [FTPConnection](class.ftp-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **ftpsetoption()****

```php
<?php
// установка времени ожидания в 10 секунд
ftp_set_option($ftp, FTP_TIMEOUT_SEC, 10);
?>
```

### Дивіться також

-   [ftpgetoption()](function.ftp-get-option.html) - Отримує поточні параметри FTP-з'єднання