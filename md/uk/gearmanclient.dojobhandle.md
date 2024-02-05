---
navigation:
  - gearmanclient.dohighbackground.md: '« GearmanClient::doHighBackground'
  - gearmanclient.dolow.md: 'GearmanClient::doLow »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::doJobHandle'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanClient::doJobHandle

(PECL gearman >= 0.5.0)

GearmanClient::doJobHandle — Отримати дескриптор завдання, що виконується

### Опис

```methodsynopsis
public GearmanClient::doJobHandle(): string
```

Отримує дескриптор завдання для завдання, що виконується. Цей метод повинен використовуватися між повторними викликами [GearmanClient::doNormal()](gearmanclient.donormal.md). Дескриптор завдання може використовуватися отримання інформації про завдання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Дескриптор завдання для завдання, що виконується.

### Дивіться також

-   [GearmanClient::jobStatus()](gearmanclient.jobstatus.md) \- Набуття статусу виконання фонового завдання
