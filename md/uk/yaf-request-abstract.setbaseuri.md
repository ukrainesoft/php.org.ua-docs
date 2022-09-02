---
navigation:
  - yaf-request-abstract.setactionname.md: '« YafRequestAbstract::setActionName'
  - yaf-request-abstract.setcontrollername.md: 'YafRequestAbstract::setControllerName »'
  - index.md: PHP Manual
  - class.yaf-request-abstract.md: YafRequestAbstract
title: 'YafRequestAbstract::setBaseUri'
---
# YafRequestAbstract::setBaseUri

(Yaf >=1.0.0)

YafRequestAbstract::setBaseUri — Встановлює базовий URI

### Опис

```methodsynopsis
public Yaf_Request_Abstract::setBaseUri(string $uir): bool
```

Встановлює базовий URI, базовий URI використовується для виконання маршрутизації, у фазі маршрутизації URI запиту використовується для маршрутизації запиту, а базовий URI використовується для пропуску провідної частини (базового URI) URI запиту. Тобто, якщо надходить запит із URI запиту a/b/c, то якщо ви встановите базовий URI на "a/b", на етапі маршрутизації використовуватиметься лише "/c".

> **Зауваження**
> 
> Як правило, вам не потрібно встановлювати його, Yaf визначить автоматично.

### Список параметрів

`uir`

Базовий URI

### Значення, що повертаються

Повертає логічне значення (boolean)
