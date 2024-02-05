---
navigation:
  - stomp.getreadtimeout.md: '« Stomp::getReadTimeout'
  - stomp.hasframe.md: 'Stomp::hasFrame »'
  - index.md: PHP Manual
  - class.stomp.md: Stomp
title: 'Stomp::getSessionId'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Stomp::getSessionId

# stomp\_get\_session\_id

(PECL stomp >= 0.1.0)

Stomp::getSessionId -- stomp\_get\_session\_id — Повертає ідентифікатор поточної сесії Stomp

### Опис

Об'єктно-орієнтований стиль (метод):

```methodsynopsis
public Stomp::getSessionId(): string|false
```

Процедурний стиль:

```methodsynopsis
stomp_get_session_id(resource $link): string|false
```

Повертає ідентифікатор сесії Stomp.

### Список параметрів

`link`

Тільки для процедурного стилю: ідентифікатор з'єднання stomp, отриманий з [stomp\_connect()](stomp.construct.md)

### Значення, що повертаються

Ідентифікатор сесії (string) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Об'єктно-орієнтований стиль**

```php
<?php

/* подключение */
try {
    $stomp = new Stomp('tcp://localhost:61613');
} catch(StompException $e) {
    die('Ошибка соединения: ' . $e->getMessage());
}

var_dump($stomp->getSessionId());

/* закрытие подключения */
unset($stomp);

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(35) "ID:php.net-52873-1257291895530-4:14"
```

**Приклад #2 Процедурний стиль**

```php
<?php

/* подключение */
$link = stomp_connect('ssl://localhost:61612');

/* проверка соединения */
if (!$link) {
    die('Ошибка соединения: ' . stomp_connect_error());
}

var_dump(stomp_get_session_id($link));

/* закрытие подключения */
stomp_close($link);

?>
```

Висновок наведеного прикладу буде схожим на:

```
string(35) "ID:php.net-52873-1257291895530-4:14"
```
