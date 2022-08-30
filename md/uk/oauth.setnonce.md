Встановити nonce для наступних запитів

-   [« OAuth::setCAPath](oauth.setcapath.html)
    
-   [OAuth::setRequestEngine »](oauth.setrequestengine.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Встановити nonce для наступних запитів
    

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

Значення oauthnonce.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, або **`false`**, якщо параметр `nonce` заданий некоректно.

### список змін

| Версия           | Описание                                                                   |
|------------------|----------------------------------------------------------------------------|
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |

### Дивіться також

-   [OAuth::setToken()](oauth.settoken.html) - Задати токен та його пароль
-   [OAuth::setAuthType()](oauth.setauthtype.html) - встановити тип авторизації
-   [OAuth::setVersion()](oauth.setversion.html) - Встановити версію OAuth