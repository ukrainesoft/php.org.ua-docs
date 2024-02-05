---
navigation:
  - class.yar-server-exception.md: « Yar\_Server\_Exception
  - class.yar-client-exception.md: Yar\_Client\_Exception »
  - index.md: PHP Manual
  - class.yar-server-exception.md: Yar\_Server\_Exception
title: 'Yar\_Server\_Exception::getType'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Yar\_Server\_Exception::getType

(PECL yar >= 1.0.0)

Yar\_Server\_Exception::getType — Отримати тип виключення

### Опис

```methodsynopsis
public Yar_Server_Exception::getType(): string
```

Отримати початковий виняток, викинутий на сервері.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Рядок

### Приклади

**Пример #1 Пример использования**Yar\_Server\_Exception::getType()\*\*\*\*

```php
//Server.php
<?php
class Custom_Exception extends Exception {};

class API {
    public function throw_exception($name) {
        throw new Custom_Exception($name);
    }
}

$service = new Yar_Server(new API());
$service->handle();
?>

//Client.php
<?php
$client = new Yar_Client("http://host/api.php");

try {
    $client->throw_exception("client");
} catch (Yar_Server_Exception $e) {
    var_dump($e->getType());
    var_dump($e->getMessage());
}
```

Висновок наведеного прикладу буде схожим на:

```
string(16) "Custom_Exception"
string(6) "client"
```

### Дивіться також
