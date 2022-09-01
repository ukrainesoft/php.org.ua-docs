---
navigation:
  - oauth.setrequestengine.md: '« OAuth::setRequestEngine'
  - oauth.setsslchecks.md: 'OAuth::setSSLChecks »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::setRSACertificate'
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

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`cert`

Сертифікат RSA

### Значення, що повертаються

Повертає **`true`** або **`false`** (наприклад, якщо встановлено неправильний сертифікат RSA)

### список змін

| Версия | Описание |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |

### Приклади

**Приклад #1 Приклад використання **OAuth::setRsaCertificate()****

```php
<?php
$consume = new OAuth('1234', '', OAUTH_SIG_METHOD_RSASHA1);

$consume->setRSACertificate(file_get_contents('test.pem'));
?>
```

### Дивіться також

-   [OAuth::setCaPath()](oauth.setcapath.md) - Встановити CA для шляху та інформації
