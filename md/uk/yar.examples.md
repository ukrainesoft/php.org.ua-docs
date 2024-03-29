---
navigation:
  - yar.constants.md: « Зумовлені константи
  - class.yar-server.md: Yar\_Server »
  - index.md: PHP Manual
  - book.yar.md: Yar
title: Приклади
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Приклади

**Приклад #1 Приклад сервера Yar**

```php
<?php

/* Предположим, что это страница может быть доступна по http://example.com/operator.php */

class Operator {

    /**
     * Складываем два операнда
     * @param interge
     * @return interge
     */
    public function add($a, $b) {
        return $this->_add($a, $b);
    }

    /**
     * Вычитаем
     */
    public function sub($a, $b) {
        return $a - $b;
    }

    /**
     * Умножаем
     */
    public function mul($a, $b) {
        return $a * $b;
    }

    /**
     * Защищённый метод
     * @param interge
     * @return interge
     */
    protected function _add($a, $b) {
        return $a + $b;
    }
}

$server = new Yar_Server(new Operator());
$server->handle();
?>
```

**Приклад #2 Звертаємось до сервера з браузера (запит GET)**

Висновок наведеного прикладу буде схожим на:

![Інформація про сервер Yar](images/4fd86c7f1b197d1d954ad0f4b033dc93-yar.png)

**Приклад #3 Приклад клієнта Yar**

```php
<?php
$client = new yar_client("http://example.com/operator.php");

/* вызываем напрямую */
var_dump($client->add(1, 2));

/* вызываем через метод call */
var_dump($client->call("add", array(3, 2)));


/* невозможно вызвать __add */
var_dump($client->_add(1, 2));
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(3)
int(5)
PHP Fatal error:  Uncaught exception 'Yar_Server_Exception' with message 'call to api Operator::_add() failed' in *
```

**Приклад #4 Приклад конкуруючих клієнтів Yar**

```php
<?php
function callback($ret, $callinfo) {
    echo $callinfo['method'] , " result: ", $ret , "\n";
}

/* регистрируем асинхронные вызовы к удалённым сервисам */
Yar_Concurrent_Client::call("http://example.com/operator.php", "add", array(1, 2), "callback");
Yar_Concurrent_Client::call("http://example.com/operator.php", "sub", array(2, 1), "callback");
Yar_Concurrent_Client::call("http://example.com/operator.php", "mul", array(2, 2), "callback");

/* посылаем все запросы и ждём ответа */
Yar_Concurrent_Client::loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
mul result: 4
sub result: 1
add result: 3
```
