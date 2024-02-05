---
navigation:
  - oauth.getaccesstoken.md: '« OAuth::getAccessToken'
  - oauth.getlastresponse.md: 'OAuth::getLastResponse »'
  - index.md: PHP Manual
  - class.oauth.md: OAuth
title: 'OAuth::getCAPath'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# OAuth::getCAPath

(PECL OAuth >= 0.99.8)

OAuth::getCAPath — Отримати інформацію CA

### Опис

```methodsynopsis
public OAuth::getCAPath(): array
```

Повертає інформацію про центр сертифікації, що включає ca\_path та ca\_info, встановлені [OAuth::setCaPath()](oauth.setcapath.md)

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив з інформацією про центр сертифікації з ключами `ca_path`и`ca_info`

### Дивіться також

-   [OAuth::setCAPath()](oauth.setcapath.md) \- Встановити CA для шляху та інформації
-   [OAuth::getLastResponseInfo()](oauth.getlastresponseinfo.md) \- Отримати HTTP-інформацію про останню відповідь
