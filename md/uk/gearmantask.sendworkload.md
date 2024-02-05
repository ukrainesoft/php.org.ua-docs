---
navigation:
  - gearmantask.senddata.md: '« GearmanTask::sendData'
  - gearmantask.taskdenominator.md: 'GearmanTask::taskDenominator »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::sendWorkload'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# GearmanTask::sendWorkload

(PECL gearman >= 0.6.0)

GearmanTask::sendWorkload — Надсилання даних завдання

### Опис

```methodsynopsis
public GearmanTask::sendWorkload(string $data): int|false
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`data`

Передані обробнику дані.

### Значення, що повертаються

Розмір переданих даних або \*\*`false`\*\*в случае неудачи.

### Дивіться також

-   [GearmanTask::recvData()](gearmantask.recvdata.md) \- Читання даних роботи чи результату завдання у буфер
