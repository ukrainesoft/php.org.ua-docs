---
navigation:
  - class.gearmanclient.md: « GearmanClient
  - gearmanclient.addserver.md: 'GearmanClient::addServer »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::addOptions'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::addOptions

(PECL gearman >= 0.6.0)

GearmanClient::addOptions — Додати опції клієнта

### Опис

```methodsynopsis
public GearmanClient::addOptions(int $option): bool
```

Додає одну або кілька опцій до встановлених.

### Список параметрів

`option`

Опції додавання. Одна з наступних констант або їх комбінація за допомогою бінарного оператора OR (|): **`GEARMAN_CLIENT_GENERATE_UNIQUE`** **`GEARMAN_CLIENT_NON_BLOCKING`** **`GEARMAN_CLIENT_UNBUFFERED_RESULT`** або **`GEARMAN_CLIENT_FREE_TASKS`**

### Значення, що повертаються

Завжди повертає **`true`**
