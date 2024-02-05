---
navigation:
  - oauth.setauthtype.md: '« OAuth::setAuthType'
  - oauth.setnonce.md: 'OAuth::setNonce »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::setCAPath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::setCAPath

(PECL OAuth >= 0.99.8)

OAuth::setCAPath — Встановити CA для шляху та інформації

### Опис

```methodsynopsis
public OAuth::setCAPath(string $ca_path = ?, string $ca_info = ?): mixed
```

Встановити центр сертифікації (CA) для шляхів та інформації.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`ca_path`

CA шляху.

`ca_info`

CA інформації.

### Значення, що повертаються

Повертає \*\*`true`**или**`false`\*\*якщо будь-який з параметрів `ca_path`или`ca_info`задан некорректно.

### список змін

| Версия | Опис |
| --- | --- |
| PECL oauth 1.0.0 | Раніше у разі виникнення помилки повертався **`null`** замість **`false`** |

### Дивіться також

-   [OAuth::getCaPath()](oauth.getcapath.md) \- Отримати інформацію CA
