Отримує контекст потоку за промовчанням

-   [« streamcontextcreate](function.stream-context-create.html)
    
-   [streamcontextgetoptions »](function.stream-context-get-options.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з потоками](ref.stream.html)
    
-   Отримує контекст потоку за промовчанням
    

# streamcontextgetdefault

(PHP 5> = 5.1.0, PHP 7, PHP 8)

streamcontextgetdefault — Отримує контекст потоку за промовчанням

### Опис

```methodsynopsis
stream_context_get_default(?array $options = null): resource
```

Повертає контекст потоку за умовчанням, який використовується у будь-яких файлових операціях ([fopen()](function.fopen.html) [filegetcontents()](function.file-get-contents.html) і т.д.), викликаних без параметра контексту. Опції для контексту за умовчанням можуть бути опціонально вказані за допомогою цієї функції використовуючи той же синтаксис, що і для [streamcontextcreate()](function.stream-context-create.html)

### Список параметрів

`options`

`options` має бути асоціативним масивом асоціативних масивів у форматі `$arr['wrapper']['option'] = $value` або **`null`**

### Значення, що повертаються

Ресурс контексту потоку.

### список змін

| Версия | Описание                                         |
|--------|--------------------------------------------------|
|        | Параметр `options` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **streamcontextgetdefault()****

```php
<?php
$default_opts = array(
  'http'=>array(
    'method'=>"GET",
    'header'=>"Accept-language: en\r\n" .
              "Cookie: foo=bar",
    'proxy'=>"tcp://10.54.1.39:8000"
  )
);


$alternate_opts = array(
  'http'=>array(
    'method'=>"POST",
    'header'=>"Content-type: application/x-www-form-urlencoded\r\n" .
              "Content-length: " . strlen("baz=bomb"),
    'content'=>"baz=bomb"
  )
);

$default = stream_context_get_default($default_opts);
$alternate = stream_context_create($alternate_opts);

/* Отправляет обычный GET-запрос на прокси-сервер 10.54.1.39
 * Для www.example.com используются опции контекста, указанные в $default_opts
 */
readfile('http://www.example.com');

/* Отправляет POST-запрос напрямую к www.example.com
 * Используемые опции контекста определены в $alternate_opts
 */
readfile('http://www.example.com', false, $alternate);

?>
```

### Дивіться також

-   [streamcontextcreate()](function.stream-context-create.html) - Створює контекст потоку
-   [streamcontextsetdefault()](function.stream-context-set-default.html) - Встановити контекст потоку за промовчанням
-   Список підтримуваних обгорток з опціями контексту ([Підтримувані протоколи та обгортки](wrappers.html)