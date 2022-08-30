Отримання унікального ідентифікатора задачі

-   [« GearmanTask::taskNumerator](gearmantask.tasknumerator.html)
    
-   [GearmanTask::uuid »](gearmantask.uuid.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanTask](class.gearmantask.html)
    
-   Отримання унікального ідентифікатора задачі
    

# GearmanTask::unique

(PECL gearman >= 0.6.0)

GearmanTask::unique — Отримання унікального ідентифікатора задачі

### Опис

```methodsynopsis
public GearmanTask::unique(): string
```

Повертає унікальний ідентифікатор цього завдання. Цей ідентифікатор надає [GearmanClient](class.gearmanclient.html), на відміну дескриптора завдання, який встановлює сервер завдань Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Унікальний ідентифікатор або \*\*`false`\*\*якщо ідентифікатор не присвоєний.

### Дивіться також

-   [GearmanClient::do()](gearmanclient.do.html) - Виконує одне завдання та повертає результат Застарілий метод
-   [GearmanClient::addTask()](gearmanclient.addtask.html) - Додати завдання, яке буде виконано у паралельному режимі