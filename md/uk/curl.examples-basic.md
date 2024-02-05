---
navigation:
  - curl.examples.md: « Приклади
  - ref.curl.md: Функції cURL »
  - index.md: PHP Manual
  - curl.examples.md: Приклади
title: Простий приклад використання curl
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Простий приклад використання curl

Як тільки ви зібрали PHP з підтримкою cURL, вже можна використовувати функції cURL. Робота з cURL завжди починається з виклику [curl\_init()](function.curl-init.md), потім встановлюються необхідні параметри за допомогою [curl\_setopt()](function.curl-setopt.md), і виконується потрібна операція викликом [curl\_exec()](function.curl-exec.md), після чого викликом [curl\_close()](function.curl-close.md) сеанс роботи завершується. Нижче наведений приклад використовує функції cURL для збереження стартової сторінки сайту example.com у файл:

**Приклад #1 Використання модуля cURL для збереження стартової сторінки example.com**

```php
<?php

$ch = curl_init("http://www.example.com/");
$fp = fopen("example_homepage.txt", "w");

curl_setopt($ch, CURLOPT_FILE, $fp);
curl_setopt($ch, CURLOPT_HEADER, 0);

curl_exec($ch);
if(curl_error($ch)) {
    fwrite($fp, curl_error($ch));
}
curl_close($ch);
fclose($fp);
?>
```
