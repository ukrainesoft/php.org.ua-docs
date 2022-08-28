Отримує список усіх заголовків HTTP-запиту

-   [« apache\_note](function.apache-note.html)
    
-   [apache\_response\_headers »](function.apache-response-headers.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Apache](ref.apache.html)
    
-   Отримує список усіх заголовків HTTP-запиту
    

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

| Версия | Описание                               |
|--------|----------------------------------------|
|        | Ця функція стала доступною у SAPI FPM. |

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
> Також можна отримати значення широко використовуваних CGIзмінних, отримавши їх із оточення сервера; це працює незалежно від того, встановлений PHP як модуль Apache чи ні. Для того, щоб отримати список усіх доступних [переменных окружения](language.variables.predefined.html), використовуйте функцію [phpinfo()](function.phpinfo.html)

### Дивіться також

-   [apache\_response\_headers()](function.apache-response-headers.html) - Повертає список усіх HTTP-заголовків відповіді Apache