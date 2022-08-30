Вимкнути SSL перевірки

-   [« OAuth::disableRedirects](oauth.disableredirects.md)
    
-   [OAuth::enableDebug »](oauth.enabledebug.md)
    
-   [PHP Manual](index.md)
    
-   [OAuth](class.oauth.md)
    
-   Вимкнути SSL перевірки
    

# OAuth::disableSSLChecks

(PECL OAuth >= 0.99.5)

OAuth::disableSSLChecks — Вимкнути SSL перевірки

### Опис

```methodsynopsis
public OAuth::disableSSLChecks(): bool
```

Вимикає звичайні перевірки клієнтських та хост сертифікатів. Не призначено для продуктивного середовища. Альтернативно можна встановити полю `sslChecks` значення **`false`**, щоб вимкнути SSL перевірки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**

### список змін

| Версия            | Описание                     |
|-------------------|------------------------------|
| PECL oauth 0.99.8 | Було додано поле `sslChecks` |

### Дивіться також

-   [OAuth::enableSSLChecks()](oauth.enablesslchecks.md) - Увімкнути перевірки SSL