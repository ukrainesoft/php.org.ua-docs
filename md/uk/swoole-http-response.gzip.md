---
navigation:
  - swoole-http-response.end.md: '« SwooleHttpResponse::end'
  - swoole-http-response.header.md: 'SwooleHttpResponse::header »'
  - index.md: PHP Manual
  - class.swoole-http-response.md: SwooleHttpResponse
title: 'SwooleHttpResponse::gzip'
---
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
