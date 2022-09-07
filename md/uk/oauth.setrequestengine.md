---
navigation:
  - oauth.setnonce.md: '« OAuth::setNonce'
  - oauth.setrsacertificate.md: 'OAuth::setRSACertificate »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::setRequestEngine'
---
# OAuth::setRequestEngine

(PECL OAuth >= 1.0.0)

OAuth::setRequestEngine — Використовується для setRequestEngine

### Опис

```methodsynopsis
public OAuth::setRequestEngine(int $reqengine): void
```

Встановлює Request Engine (механізм запитів), який надсилатиме HTTP-запити.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`reqengine`

Вибраний механізм запитів. Задайте **`OAUTH_REQENGINE_STREAMS`**, якщо хочете використовувати потоки PHP, або **`OAUTH_REQENGINE_CURL`** для використання [Curl](book.curl.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OAuthException](class.oauthexception.md) під час вибору некоректного механізму запитів.

### Приклади

**Приклад #1 Приклад використання **OAuth::setRequestEngine()****

```php
<?php
$consumer = new OAuth();

$consumer->setRequestEngine(OAUTH_REQENGINE_STREAMS);
?>
```

### Дивіться також

-   [Curl](book.curl.md)
-   [потоки PHP](book.stream.md)
-   [OAuthException](class.oauthexception.md)
