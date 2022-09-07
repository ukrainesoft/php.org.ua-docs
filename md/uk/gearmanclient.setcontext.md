---
navigation:
  - gearmanclient.setcompletecallback.md: '« GearmanClient::setCompleteCallback'
  - gearmanclient.setcreatedcallback.md: 'GearmanClient::setCreatedCallback »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setContext'
---
# GearmanClient::setContext

(PECL gearman >= 0.6.0)

GearmanClient::setContext — Встановити контекст програми

### Опис

```methodsynopsis
public GearmanClient::setContext(string $context): bool
```

Встановлює довільний рядок для надання контексту програми, яка може бути пізніше отримана за допомогою [GearmanClient::context()](gearmanclient.context.md)

### Список параметрів

`context`

Довільні дані контексту

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanClient::context()](gearmanclient.context.md) - Повертає контекст програми
