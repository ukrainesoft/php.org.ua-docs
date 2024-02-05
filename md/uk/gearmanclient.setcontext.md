---
navigation:
  - gearmanclient.setcompletecallback.md: '« GearmanClient::setCompleteCallback'
  - gearmanclient.setcreatedcallback.md: 'GearmanClient::setCreatedCallback »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setContext'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setContext

(PECL gearman >= 0.6.0)

GearmanClient::setContext — Встановити контекст програми

### Опис

```methodsynopsis
public GearmanClient::setContext(string $data): bool
```

Встановлює довільний рядок для надання контексту програми, яка може бути пізніше отримана за допомогою [GearmanClient::context()](gearmanclient.context.md)

### Список параметрів

`data`

Довільні дані контексту

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanClient::context()](gearmanclient.context.md) \- Повертає контекст програми
