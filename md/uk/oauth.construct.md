Створює новий об'єкт OAuth

-   [« OAuth](class.oauth.html)
    
-   [OAuth::\_\_destruct »](oauth.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Створює новий об'єкт OAuth
    

# OAuth::construct

(PECL OAuth >= 0.99.1)

OAuth::construct — Створює новий об'єкт OAuth

### Опис

public **OAuth::construct**  
string `$consumer_key`  
string `$consumer_secret`  
string `$signature_method` **`OAUTH_SIG_METHOD_HMACSHA1`**  
int `$auth_type`  

Створює новий об'єкт OAuth

### Список параметрів

`consumer_key`

Ключ споживача наданий сервіс провайдером.

`consumer_secret`

Секрет споживача наданий сервіс провайдером.

`signature_method`

Цей необов'язковий параметр визначає, який метод підпису буде використано. За замовчуванням використовується **`OAUTH_SIG_METHOD_HMACSHA1`** (HMAC-SHA1).

`auth_type`

Цей необов'язковий параметр визначає, як передавати параметри OAuth споживачеві. За замовчуванням використовується **`OAUTH_AUTH_TYPE_AUTHORIZATION`** (У заголовку `Authorization`