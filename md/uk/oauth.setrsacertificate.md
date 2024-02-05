---
navigation:
  - oauth.setrequestengine.md: '« OAuth::setRequestEngine'
  - oauth.setsslchecks.md: 'OAuth::setSSLChecks »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::setRSACertificate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::setRSACertificate

(PECL OAuth >= 1.0.0)

OAuth::setRSACertificate — Встановити сертифікат RSA

### Опис

```methodsynopsis
public OAuth::setRSACertificate(string $cert): mixed
```

Встановлює сертифікат RSA.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`cert`

Сертифікат RSA

### Значення, що повертаються

Повертає **`true`**или**`false`** (наприклад, якщо встановлено неправильний сертифікат RSA)

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |

### Приклади

**Пример #1 Пример использования**OAuth::setRsaCertificate()\*\*\*\*

```php
<?php
$consume = new OAuth('1234', '', OAUTH_SIG_METHOD_RSASHA1);

$consume->setRSACertificate(file_get_contents('test.pem'));
?>
```

### Дивіться також

-   [OAuth::setCaPath()](oauth.setcapath.md) \- Встановити CA для шляху та інформації
