---
navigation:
  - oauth.setsslchecks.md: '« OAuth::setSSLChecks'
  - oauth.settoken.md: 'OAuth::setToken »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::setTimestamp'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::setTimestamp

(PECL OAuth >= 1.0.0)

OAuth::setTimestamp — Встановити позначку часу

### Опис

```methodsynopsis
public OAuth::setTimestamp(string $timestamp): mixed
```

Встановити позначку часу OAuth для наступних запитів.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`timestamp`

Мітки часу.

### Значення, що повертаються

Повертає **`true`** або **`false`**, якщо параметр `timestamp`задан некорректно.

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |

### Дивіться також

-   [OAuth::setNonce()](oauth.setnonce.md) \- Встановити nonce для наступних запитів
