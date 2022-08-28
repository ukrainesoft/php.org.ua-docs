Отримати HTTP-інформацію про останню відповідь

-   [« OAuth::getLastResponseHeaders](oauth.getlastresponseheaders.html)
    
-   [OAuth::getRequestHeader »](oauth.getrequestheader.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Отримати HTTP-інформацію про останню відповідь
    

# OAuth::getLastResponseInfo

(PECL OAuth >= 0.99.1)

OAuth::getLastResponseInfo — Отримати HTTP-інформацію про останню відповідь

### Опис

```methodsynopsis
public OAuth::getLastResponseInfo(): array
```

Повертає HTTP-інформацію про останню відповідь.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив з інформацією на останній запит. Можна використовувати константи [curl\_getinfo()](function.curl-getinfo.html)

### Дивіться також

-   [OAuth::fetch()](oauth.fetch.html) - Витягти захищений ресурс OAuth
-   [OAuth::getLastResponse()](oauth.getlastresponse.html) - Отримати останню відповідь