---
navigation:
  - function.apache-note.md: « apache\_note
  - function.apache-response-headers.md: apache\_response\_headers »
  - index.md: PHP Manual
  - ref.apache.md: Функції Apache
title: apache\_request\_headers
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# apache\_request\_headers

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

apache\_request\_headers — Отримує список усіх заголовків HTTP-запиту

### Опис

```methodsynopsis
apache_request_headers(): array
```

Отримує список усіх заголовків HTTP поточного запиту. Працює на веб-серверах Apache та FastCGI.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив, що містить усі HTTP-заголовки поточного запиту, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.3.0 | Ця функція стала доступною у SAPI FPM. |

### Приклади

**Приклад #1 Приклад використання** apache\_request\_headers()\*\*\*\*

```php
<?php
$headers = apache_request_headers();

foreach ($headers as $header => $value) {
    echo "$header: $value <br />\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
Accept: */*
Accept-Language: en-us
Accept-Encoding: gzip, deflate
User-Agent: Mozilla/4.0
Host: www.example.com
Connection: Keep-Alive
```

### Примітки

> **Зауваження** :
> 
> Також можна отримати значення широко використовуваних CGI-змінних, отримавши їх із оточення сервера; це працює незалежно від того, встановлений PHP як модуль Apache чи ні. Для того, щоб отримати список усіх доступних [змінних оточення](language.variables.predefined.md), используйте функцию[phpinfo()](function.phpinfo.md)

### Дивіться також

-   [apache\_response\_headers()](function.apache-response-headers.md) \- Повертає список усіх HTTP-заголовків відповіді Apache
