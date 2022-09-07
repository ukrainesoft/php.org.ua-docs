---
navigation:
  - gearmanclient.setworkloadcallback.md: '« GearmanClient::setWorkloadCallback'
  - gearmanclient.wait.md: 'GearmanClient::wait »'
  - index.md: PHP Manual
  - class.gearmanclient.md: GearmanClient
title: 'GearmanClient::timeout'
---
# GearmanClient::timeout

(PECL gearman >= 0.6.0)

GearmanClient::timeout — Отримання часу очікування операцій введення/виводу

### Опис

```methodsynopsis
public GearmanClient::timeout(): int
```

Повертає час очікування операцій введення/виводу у мілісекундах.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Час очікування у мілісекундах. Негативне значення означає відсутність обмеження.

### Дивіться також

-   [GearmanClient::setTimeout()](gearmanclient.settimeout.md) - Встановлення часу очікування для операцій введення/виводу
