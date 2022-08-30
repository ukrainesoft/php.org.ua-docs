Включає gzip-стиснення відповіді.

-   [« SwooleHttpResponse::end](swoole-http-response.end.html)
    
-   [SwooleHttpResponse::header »](swoole-http-response.header.html)
    
-   [PHP Manual](index.md)
    
-   [SwooleHttpResponse](class.swoole-http-response.html)
    
-   Включає gzip-стиснення відповіді.
    

# SwooleHttpResponse::gzip

(PECL swoole >= 1.9.0)

SwooleHttpResponse::gzip — Включає gzip-стиснення вмісту відповіді.

### Опис

```methodsynopsis
public Swoole\Http\Response::gzip(string $compress_level = ?): ReturnType
```

Заголовок про Content-Encoding буде додано автоматично.

### Список параметрів

`compress_level`

### Значення, що повертаються