Отримати дескриптор завдання, що виконується

-   [« GearmanClient::doHighBackground](gearmanclient.dohighbackground.html)
    
-   [GearmanClient::doLow »](gearmanclient.dolow.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Отримати дескриптор завдання, що виконується
    

# GearmanClient::doJobHandle

(PECL gearman >= 0.5.0)

GearmanClient::doJobHandle — Отримати дескриптор завдання, що виконується

### Опис

```methodsynopsis
public GearmanClient::doJobHandle(): string
```

Отримує дескриптор завдання для завдання, що виконується. Цей метод повинен використовуватися між повторними викликами [GearmanClient::doNormal()](gearmanclient.donormal.html). Дескриптор завдання може використовуватися отримання інформації про завдання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Дескриптор завдання для завдання, що виконується.

### Дивіться також

-   [GearmanClient::jobStatus()](gearmanclient.jobstatus.html) - Набуття статусу виконання фонового завдання