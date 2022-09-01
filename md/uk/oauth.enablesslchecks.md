---
navigation:
  - oauth.enableredirects.md: '« OAuth::enableRedirects'
  - oauth.fetch.md: 'OAuth::fetch »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::enableSSLChecks'
---
# OAuth::enableSSLChecks

(PECL OAuth >= 0.99.5)

OAuth::enableSSLChecks — Увімкнути перевірки SSL

### Опис

```methodsynopsis
public OAuth::enableSSLChecks(): bool
```

Включити звичайні перевірки сертифіката SSL кінцевої точки та хоста (ввімкнено за замовчуванням). Також можна встановити `sslChecks` у значення не-**`false`**, щоб вимкнути перевірки SSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**

### список змін

| Версия | Описание |
| --- | --- |
| PECL oauth 0.99.8 | Додано властивість `sslChecks` |

### Дивіться також

-   [OAuth::disableSSLChecks()](oauth.disablesslchecks.md) - Вимкнути SSL перевірки
