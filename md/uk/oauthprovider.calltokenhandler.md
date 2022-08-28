Викликати callback-функцію tokenNonceHandler

-   [« OAuthProvider::callTimestampNonceHandler](oauthprovider.calltimestampnoncehandler.html)
    
-   [OAuthProvider::checkOAuthRequest »](oauthprovider.checkoauthrequest.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   Викликати callback-функцію tokenNonceHandler
    

# OAuthProvider::calltokenHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::calltokenHandler — Викликати callback-функцію tokenNonceHandler

### Опис

```methodsynopsis
public OAuthProvider::calltokenHandler(): void
```

Викликати зареєстровану callback-функцію обробника токена, яка була задана за допомогою [OAuthProvider::tokenHandler()](oauthprovider.tokenhandler.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо callback-функція може бути викликана чи відсутня, то генерується помилка рівня **`E_ERROR`**

### Дивіться також

-   [OAuthProvider::tokenHandler()](oauthprovider.tokenhandler.html) - Встановити обробник tokenHandler