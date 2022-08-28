Перевірка запиту oauth

-   [« OAuthProvider::calltokenHandler](oauthprovider.calltokenhandler.html)
    
-   [OAuthProvider::\_\_construct »](oauthprovider.construct.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   Перевірка запиту oauth
    

# OAuthProvider::checkOAuthRequest

(PECL OAuth >= 1.0.0)

OAuthProvider::checkOAuthRequest — Перевірка запиту oauth

### Опис

```methodsynopsis
public OAuthProvider::checkOAuthRequest(string $uri = ?, string $method = ?): void
```

Перевіряє запит OAuth.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`uri`

Необов'язковий URI, або кінцева точка.

`method`

Необов'язковий параметр, який визначає метод HTTP. Одна з **`OAUTH_HTTP_METHOD_*`** [констант OAuth](oauth.constants.html)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Викликає помилку рівня **`E_ERROR`** якщо HTTP-метод заданий некоректно.

### Дивіться також

-   [OAuthProvider::reportProblem()](oauthprovider.reportproblem.html) - Повідомити про проблему