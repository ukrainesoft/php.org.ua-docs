Отримання унікального ідентифікатора завдання (застарілий метод)

-   [« GearmanTask::unique](gearmantask.unique.html)
    
-   [GearmanWorker »](class.gearmanworker.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanTask](class.gearmantask.html)
    
-   Отримання унікального ідентифікатора завдання (застарілий метод)
    

# GearmanTask::uuid

(PECL gearman <= 0.5.0)

GearmanTask::uuid — Отримання унікального ідентифікатора завдання (застарілий метод)

### Опис

```methodsynopsis
public GearmanTask::uuid(): string
```

Повертає унікальний ідентифікатор цього завдання. Цей ідентифікатор надає [GearmanClient](class.gearmanclient.html), на відміну ідентифікатора об'єкта завдання, який встановлює сервер завдань.

> **Зауваження**
> 
> Цей метод було замінено на [GearmanTask::unique()](gearmantask.unique.html) у версії 0.6.0 модуля Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Унікальний ідентифікатор або **`false`**якщо ідентифікатор не призначений.

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.html) - Виконує одне завдання та повертає результат Застарілий метод
-   [GearmanClient::addTask()](gearmanclient.addtask.html) - Додати завдання, яке буде виконано у паралельному режимі