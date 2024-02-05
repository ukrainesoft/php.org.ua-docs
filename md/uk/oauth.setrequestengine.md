---
navigation:
  - oauth.setnonce.md: '« OAuth::setNonce'
  - oauth.setrsacertificate.md: 'OAuth::setRSACertificate »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::setRequestEngine'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`reqengine`

Вибраний механізм запитів. Задайте **`OAUTH_REQENGINE_STREAMS`**, якщо хочете використовувати потоки PHP, або \*\*`OAUTH_REQENGINE_CURL`\*\*для использования[Curl](book.curl.md)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викидає виняток [OAuthException](class.oauthexception.md) під час вибору некоректного механізму запитів.

### Приклади

**Пример #1 Пример использования**OAuth::setRequestEngine()\*\*\*\*

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
