Отримання чисельника відсотка виконаної роботи

-   [« GearmanTask::taskDenominator](gearmantask.taskdenominator.md)
    
-   [GearmanTask::unique »](gearmantask.unique.md)
    
-   [PHP Manual](index.md)
    
-   [GearmanTask](class.gearmantask.md)
    
-   Отримання чисельника відсотка виконаної роботи
    

# GearmanTask::taskNumerator

(PECL gearman >= 0.5.0)

GearmanTask::taskNumerator — Отримання чисельника відсотка виконаної роботи

### Опис

```methodsynopsis
public GearmanTask::taskNumerator(): int
```

Повертає чисельник дробу, який використовується для обчислення відсотка виконаної роботи.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Число від 0 до 100 або \*\*`false`\*\*якщо значення визначити не вдалося.

### Дивіться також

-   [GearmanTask::taskDenominator()](gearmantask.taskdenominator.md) - отримати знаменник відсотка виконаної роботи