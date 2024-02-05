---
navigation:
  - oauth.enableredirects.md: '« OAuth::enableRedirects'
  - oauth.fetch.md: 'OAuth::fetch »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::enableSSLChecks'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::enableSSLChecks

(PECL OAuth >= 0.99.5)

OAuth::enableSSLChecks — Увімкнути перевірки SSL

### Опис

```methodsynopsis
public OAuth::enableSSLChecks(): bool
```

Включити звичайні перевірки сертифіката SSL кінцевої точки та хоста (ввімкнено за замовчуванням). Також можна встановити `sslChecks`в значение не-**`false`**, щоб вимкнути перевірки SSL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**`true`**

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 0.99.8 | Додано властивість `sslChecks` |

### Дивіться також

-   [OAuth::disableSSLChecks()](oauth.disablesslchecks.md) \- Вимкнути SSL перевірки
