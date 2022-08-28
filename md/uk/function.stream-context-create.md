Створює контекст потоку

-   [« stream\_bucket\_prepend](function.stream-bucket-prepend.html)
    
-   [stream\_context\_get\_default »](function.stream-context-get-default.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Створює контекст потоку
    

# streamcontextcreate

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamcontextcreate — Створює контекст потоку

### Опис

```methodsynopsis
stream_context_create(?array $options = null, ?array $params = null): resource
```

Створює та повертає контекст потоку з опціями, вказаними в масиві `options`

### Список параметрів

`options`

Має бути асоціативним масивом у форматі `$arr['wrapper']['option'] = $value` або **`null`**. Список доступних обгорток та опцій дивіться у розділі [Опции контекста](context.html)

Значення за замовчуванням - **`null`**

`params`

Має бути асоціативним масивом у форматі `$arr['parameter'] = $value` або **`null`**. Зверніться до розділу [Опции контекста](context.params.html) за списком стандартних параметрів потоку.

### Значення, що повертаються

Ресурс контексту потоку.

### список змін

| Версия | Описание                                                       |
|--------|----------------------------------------------------------------|
|        | Параметри `options` і `params` тепер допускають значення null. |

### Приклади

**Приклад #1 Використання **streamcontextcreate()****

```php
<?php
$opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar\r\n"
  )
);

$context = stream_context_create($opts);

/* Отправляет http-запрос на домен www.example.com
   с дополнительными заголовкам, показанными выше */
$fp = fopen('http://www.example.com', 'r', false, $context);
fpassthru($fp);
fclose($fp);
?>
```

### Дивіться також

-   [stream\_context\_set\_option()](function.stream-context-set-option.html) - Встановлює опцію для потоку/обгортки/контексту
-   Список підтримуваних обгорток ([Поддерживаемые протоколы и обёртки](wrappers.html)
-   Опції контексту ([Контекстные опции и параметры](context.html)