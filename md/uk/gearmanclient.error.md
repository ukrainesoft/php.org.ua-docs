---
navigation:
  - gearmanclient.echo.md: '« GearmanClient::echo'
  - gearmanclient.geterrno.md: 'GearmanClient::getErrno »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::error'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::error

(PECL gearman >= 0.5.0)

GearmanClient::error — Повернути рядок помилки для останньої виявленої помилки

### Опис

```methodsynopsis
public GearmanClient::error(): string|false
```

Повертає рядок помилки для останньої виявленої помилки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Удобочитаемая строка ошибки или\*\*`false`\*\*, якщо повідомлення про помилку відсутнє.

### Дивіться також

-   [GearmanClient::getErrno()](gearmanclient.geterrno.md) \- Отримати значення errno
