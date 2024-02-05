---
navigation:
  - oauth.setcapath.md: '« OAuth::setCAPath'
  - oauth.setrequestengine.md: 'OAuth::setRequestEngine »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::setNonce'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::setNonce

(PECL OAuth >= 0.99.1)

OAuth::setNonce — Встановити nonce для подальших запитів.

### Опис

```methodsynopsis
public OAuth::setNonce(string $nonce): mixed
```

Встановлює nonce для подальших запитів.

### Список параметрів

`nonce`

Значення oauth\_nonce.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`**, якщо параметр `nonce`задан некорректно.

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |

### Дивіться також

-   [OAuth::setToken()](oauth.settoken.md) \- Задати токен та його пароль
-   [OAuth::setAuthType()](oauth.setauthtype.md) \- встановити тип авторизації
-   [OAuth::setVersion()](oauth.setversion.md) \- Встановити версію OAuth
