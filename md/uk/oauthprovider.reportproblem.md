Повідомити про проблему

-   [« OAuthProvider::removeRequiredParameter](oauthprovider.removerequiredparameter.html)
    
-   [OAuthProvider::setParam »](oauthprovider.setparam.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   Повідомити про проблему
    

# OAuthProvider::reportProblem

(PECL OAuth >= 1.0.0)

OAuthProvider::reportProblem — Повідомити про проблему

### Опис

```methodsynopsis
final public static OAuthProvider::reportProblem(string $oauthexception, bool $send_headers = true): string
```

Передати проблему як виняток [OAuthException](class.oauthexception.html). Допустимі проблеми перераховані в секції [константи OAuth](oauth.constants.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`oauthexception`

Об'єкт виключення [OAuthException](class.oauthexception.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [OAuthProvider::checkOAuthRequest()](oauthprovider.checkoauthrequest.html) - Перевірка запиту oauth
-   [OAuthProvider::isRequestTokenEndpoint()](oauthprovider.isrequesttokenendpoint.html) - Установка isRequestTokenEndpoint