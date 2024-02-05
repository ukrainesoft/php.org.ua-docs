---
navigation:
  - gearmanclient.dostatus.md: '« GearmanClient::doStatus'
  - gearmanclient.error.md: 'GearmanClient::error »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::echo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::echo

(PECL gearman >= 0.5.0)

GearmanClient::echo — Надсилає дані всім серверам завдань, щоб перевірити відгук \[Застарілий метод\]

### Опис

```methodsynopsis
public GearmanClient::echo(string $workload): bool
```

Метод\*\*GearmanClient::echo()\*\*устарел начиная с pecl/gearman 1.0.0. Используйте[GearmanClient::ping()](gearmanclient.ping.md)

### Список параметрів

`workload`

Деякі довільні серіалізовані дані для отримання відгуку

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
