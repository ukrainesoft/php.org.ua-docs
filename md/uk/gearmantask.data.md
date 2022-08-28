Отримати дані, повернені для завдання

-   [« GearmanTask::create](gearmantask.create.html)
    
-   [GearmanTask::dataSize »](gearmantask.datasize.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanTask](class.gearmantask.html)
    
-   Отримати дані, повернені для завдання
    

# GearmanTask::data

(PECL gearman >= 0.5.0)

GearmanTask::data — Отримати дані, повернені для завдання

### Опис

```methodsynopsis
public GearmanTask::data(): string
```

Отримує дані, що повертаються обробником після завершення роботи завдання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Серіалізовані дані або **`false`**якщо обробник не надав даних.

### Дивіться також

-   [GearmanTask::dataSize()](gearmantask.datasize.html) - Отримати розмір даних, що повертаються