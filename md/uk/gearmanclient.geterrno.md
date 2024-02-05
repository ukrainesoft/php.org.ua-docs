---
navigation:
  - gearmanclient.error.md: '« GearmanClient::error'
  - gearmanclient.jobstatus.md: 'GearmanClient::jobStatus »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::getErrno'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::getErrno

(PECL gearman >= 0.5.0)

GearmanClient::getErrno — Отримати значення errno

### Опис

```methodsynopsis
public GearmanClient::getErrno(): int
```

Значення ERRNO у разі повертається значення GEARMAN\_ERRNO.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Допустимий Gearman errno.

### Дивіться також

-   [GearmanClient::error()](gearmanclient.error.md) \- Повернути рядок помилки для останньої виявленої помилки
