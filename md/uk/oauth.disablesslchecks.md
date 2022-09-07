---
navigation:
  - oauth.disableredirects.md: '« OAuth::disableRedirects'
  - oauth.enabledebug.md: 'OAuth::enableDebug »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::disableSSLChecks'
---
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

| Версия | Описание |
| --- | --- |
| PECL oauth 0.99.8 | Було додано поле `sslChecks` |

### Дивіться також

-   [OAuth::enableSSLChecks()](oauth.enablesslchecks.md) - Увімкнути перевірки SSL
