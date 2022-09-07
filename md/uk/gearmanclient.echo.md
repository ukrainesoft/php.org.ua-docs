---
navigation:
  - gearmanclient.dostatus.md: '« GearmanClient::doStatus'
  - gearmanclient.error.md: 'GearmanClient::error »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::echo'
---
# GearmanClient::echo

(PECL gearman >= 0.5.0)

GearmanClient::echo — Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод

### Опис

```methodsynopsis
public GearmanClient::echo(string $workload): bool
```

Метод **GearmanClient::echo()** застарів з pecl/gearman 1.0.0. Використовуйте [GearmanClient::ping()](gearmanclient.ping.md)

### Список параметрів

`workload`

Деякі довільні серіалізовані дані для отримання відгуку

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
