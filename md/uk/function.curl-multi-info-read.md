---
navigation:
  - function.curl-multi-getcontent.md: « curl\_multi\_getcontent
  - function.curl-multi-init.md: curl\_multi\_init »
  - index.md: PHP Manual
  - ref.curl.md: Опції cURL
title: curl\_multi\_info\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# curl\_multi\_info\_read

(PHP 5, PHP 7, PHP 8)

curl\_multi\_info\_read — Повертає інформацію про поточні операції

### Опис

```methodsynopsis
curl_multi_info_read(CurlMultiHandle $multi_handle, int &$queued_messages = null): array|false
```

Запитує набір дескрипторів про наявність повідомлень або інформації від індивідуальних передач. Повідомлення можуть містити таку інформацію як код помилки передачі або просто факт завершення передачі.

Виклики цієї функції, що повторюються, щоразу повертатимуть новий результат, доки не буде повернено **`false`** як сигнал закінчення повідомлень. Ціле число, що міститься в `queued_messages`, вказує кількість повідомлень, що залишилися після виклику цієї функції.

**Увага**

Дані, на які вказує ресурс, що повертається, будуть затерті викликом [curl\_multi\_remove\_handle()](function.curl-multi-remove-handle.md)

### Список параметрів

`multi_handle`

Мультидескриптор cURL, отриманий з [curl\_multi\_init()](function.curl-multi-init.md)

`queued_messages`

Кількість повідомлень, що залишилися в черзі

### Значення, що повертаються

У разі успішного виконання повертає асоціативний масив повідомлень або \*\*`false`\*\*в случае возникновения ошибки.

**Вміст масиву, що повертається**

| Ключ: | Значение: |
| --- | --- |
| `msg` | Константа\*\*`CURLMSG_DONE`\*\*. . Інші значення, що повертаються, поки недоступні. |
| `result` | Одна из констант\*\*`CURLE_*`\*\*. . Якщо все добре, результатом буде константа **`CURLE_OK`** |
| `handle` | Ресурс типу curl, що вказує на дескриптор, до якого належить. |

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `multi_handle` тепер чекає екземпляр; раніше, очікувався ресурс (resource). |

### Приклади

**Пример #1 Пример использования**curl\_multi\_info\_read()\*\*\*\*

```php
<?php

$urls = array(
   "http://www.cnn.com/",
   "http://www.bbc.co.uk/",
   "http://www.yahoo.com/"
);

$mh = curl_multi_init();

foreach ($urls as $i => $url) {
    $conn[$i] = curl_init($url);
    curl_setopt($conn[$i], CURLOPT_RETURNTRANSFER, 1);
    curl_multi_add_handle($mh, $conn[$i]);
}

do {
    $status = curl_multi_exec($mh, $active);
    if ($active) {
        curl_multi_select($mh);
    }
    while (false !== ($info = curl_multi_info_read($mh))) {
        var_dump($info);
    }
} while ($active && $status == CURLM_OK);

foreach ($urls as $i => $url) {
    $res[$i] = curl_multi_getcontent($conn[$i]);
    curl_close($conn[$i]);
}

var_dump(curl_multi_info_read($mh));

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  ["msg"]=>
  int(1)
  ["result"]=>
  int(0)
  ["handle"]=>
  resource(5) of type (curl)
}
array(3) {
  ["msg"]=>
  int(1)
  ["result"]=>
  int(0)
  ["handle"]=>
  resource(7) of type (curl)
}
array(3) {
  ["msg"]=>
  int(1)
  ["result"]=>
  int(0)
  ["handle"]=>
  resource(6) of type (curl)
}
bool(false)
```

### Дивіться також

-   [curl\_multi\_init()](function.curl-multi-init.md) \- Створює набір cURL-дескрипторів
