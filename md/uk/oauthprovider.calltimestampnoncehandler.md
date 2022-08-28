Викликати callback-функцію timestampNonceHandler

-   [« OAuthProvider::callconsumerHandler](oauthprovider.callconsumerhandler.html)
    
-   [OAuthProvider::calltokenHandler »](oauthprovider.calltokenhandler.html)
    
-   [PHP Manual](index.html)
    
-   [OAuthProvider](class.oauthprovider.html)
    
-   Викликати callback-функцію timestampNonceHandler
    

# OAuthProvider::callTimestampNonceHandler

(PECL OAuth >= 1.0.0)

OAuthProvider::callTimestampNonceHandler — Викликати callback-функцію timestampNonceHandler

### Опис

```methodsynopsis
public OAuthProvider::callTimestampNonceHandler(): void
```

Викликати зареєстровану callback-функцію обробника мітки часу, яка була задана за допомогою [OAuthProvider::timestampNonceHandler()](oauthprovider.timestampnoncehandler.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

Якщо callback-функція може бути викликана чи відсутня, то генерується помилка рівня **`E_ERROR`**

### Дивіться також

-   [OAuthProvider::timestampNonceHandler()](oauthprovider.timestampnoncehandler.html) - Встановити обробник timestampNonceHandler