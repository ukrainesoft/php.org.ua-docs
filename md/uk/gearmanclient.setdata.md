---
navigation:
  - gearmanclient.setcreatedcallback.md: '« GearmanClient::setCreatedCallback'
  - gearmanclient.setdatacallback.md: 'GearmanClient::setDataCallback »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::setData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::setData

(PECL gearman <= 0.5.0)

GearmanClient::setData — Встановити дані програми (застарілий метод)

### Опис

```methodsynopsis
public GearmanClient::setData(string $data): bool
```

Встановлює деякі довільні дані програми, які згодом можуть бути вилучені [GearmanClient::data()](gearmanclient.data.md)

> **Зауваження** :
> 
> Цей метод було замінено на **GearmanCient::setContext()** у версії 0.6.0 модуля Gearman.

### Список параметрів

`data`

### Значення, що повертаються

Завжди повертає **`true`**

### Дивіться також

-   [GearmanClient::data()](gearmanclient.data.md) \- Повертає дані програми (функція застаріла)
