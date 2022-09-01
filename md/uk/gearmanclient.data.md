---
navigation:
  - gearmanclient.context.md: '« GearmanClient::context'
  - gearmanclient.do.md: 'GearmanClient::do »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::data'
---
# GearmanClient::data

(PECL gearman <= 0.5.0)

GearmanClient::data — Повертає дані програми (функція застаріла)

### Опис

```methodsynopsis
public GearmanClient::data(): string
```

Повертає дані програми, встановлені раніше за допомогою [GearmanClient::setData()](gearmanclient.setdata.md)

> **Зауваження**
> 
> Цей метод було замінено на [GearmanClient::setContext()](gearmanclient.setcontext.md) у версії 0.6.0 модуля Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Деякі строкові дані, встановлені [GearmanClient::setData()](gearmanclient.setdata.md)

### Дивіться також

-   [GearmanClient::setData()](gearmanclient.setdata.md) - встановити дані програми (застарілий метод)
