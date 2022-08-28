Надсилання даних завдання

-   [« GearmanTask::sendData](gearmantask.senddata.html)
    
-   [GearmanTask::taskDenominator »](gearmantask.taskdenominator.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanTask](class.gearmantask.html)
    
-   Надсилання даних завдання
    

# GearmanTask::sendWorkload

(PECL gearman >= 0.6.0)

GearmanTask::sendWorkload — Надсилання даних завдання

### Опис

```methodsynopsis
public GearmanTask::sendWorkload(string $data): int
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`data`

Передані обробнику дані.

### Значення, що повертаються

Розмір переданих даних або **`false`** у разі невдачі.

### Дивіться також

-   [GearmanTask::recvData()](gearmantask.recvdata.html) - Читання даних роботи чи результату завдання у буфер