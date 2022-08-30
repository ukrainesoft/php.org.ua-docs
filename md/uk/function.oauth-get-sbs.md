Створити базовий рядок підпису (Signature Base String)

-   [« Функции OAuth](ref.oauth.html)
    
-   [oauthurlencode »](function.oauth-urlencode.html)
    
-   [PHP Manual](index.html)
    
-   [Функции OAuth](ref.oauth.html)
    
-   Створити базовий рядок підпису (Signature Base String)
    

# oauthgetsbs

(PECL OAuth >=0.99.7)

oauthgetsbs — Створити базовий рядок підпису (Signature Base String)

### Опис

```methodsynopsis
oauth_get_sbs(string $http_method, string $uri, array $request_parameters = ?): string
```

Створити базовий рядок підпису (Signature Base String) відповідно до pecl/oauth.

### Список параметрів

`http_method`

HTTP метод.

`uri`

URI для кодування.

`request_parameters`

Масив параметрів запиту.

### Значення, що повертаються

Повертає базовий рядок підпису (Signature Base String).