---
navigation:
  - gearmantask.returncode.md: '« GearmanTask::returnCode'
  - gearmantask.sendworkload.md: 'GearmanTask::sendWorkload »'
  - index.md: PHP Manual
  - class.gearmantask.md: GearmanTask
title: 'GearmanTask::sendData'
---
# GearmanTask::sendData

(PECL gearman <= 0.5.0)

GearmanTask::sendData — Надсилання даних завдання (застарілий метод)

### Опис

```methodsynopsis
public GearmanTask::sendData(string $data): int
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`data`

Передані обробнику дані.

### Значення, що повертаються

Розмір переданих даних або **`false`** у разі невдачі.

### Дивіться також

-   [GearmanTask::recvData()](gearmantask.recvdata.md) - Читання даних роботи чи результату завдання у буфер
