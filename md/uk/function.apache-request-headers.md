---
navigation:
  - function.apache-note.html: « apachenote
  - function.apache-response-headers.html: apacheresponseheaders »
  - index.html: PHP Manual
  - ref.apache.html: Функции Apache
title: apacherequestheaders
---
# apacherequestheaders

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

apacherequestheaders — Отримує список усіх заголовків HTTP-запиту

### Опис

```methodsynopsis
apache_request_headers(): array
```

Отримує список усіх заголовків HTTP поточного запиту. Працює на веб-серверах Apache та FastCGI.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив, що містить усі HTTP-заголовки поточного запиту, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Ця функція стала доступною у SAPI FPM. |

### Приклади

**Приклад #1 Приклад використання **apacherequestheaders()****

```php
<?php
$headers = apache_request_headers();

foreach ($headers as $header => $value) {
    echo "$header: $value <br />\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Accept: */*
Accept-Language: en-us
Accept-Encoding: gzip, deflate
User-Agent: Mozilla/4.0
Host: www.example.com
Connection: Keep-Alive
```

### Примітки

> **Зауваження**
> 
> Також можна отримати значення широко використовуваних CGIзмінних, отримавши їх із оточення сервера; це працює незалежно від того, встановлений PHP як модуль Apache чи ні. Для того, щоб отримати список усіх доступних [змінних оточення](language.variables.predefined.html), використовуйте функцію [phpinfo()](function.phpinfo.md)

### Дивіться також

-   [apacheresponseheaders()](function.apache-response-headers.md) - Повертає список усіх HTTP-заголовків відповіді Apache
