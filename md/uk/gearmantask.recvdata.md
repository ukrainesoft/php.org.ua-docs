Читання даних роботи чи результату завдання у буфер

-   [« GearmanTask::jobHandle](gearmantask.jobhandle.html)
    
-   [GearmanTask::returnCode »](gearmantask.returncode.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanTask](class.gearmantask.html)
    
-   Читання даних роботи чи результату завдання у буфер
    

# GearmanTask::recvData

(PECL gearman >= 0.5.0)

GearmanTask::recvData — Читання даних роботи або результату завдання у буфер

### Опис

```methodsynopsis
public GearmanTask::recvData(int $data_len): array
```

**Увага**

Ця функція є *ЕКСПЕРИМЕНТАЛЬНОЇ*. Поведінка цієї функції, її ім'я та документація, що до неї належить, можуть змінитися в наступних версіях PHP без повідомлення. Використовуйте цю функцію на свій страх та ризик.

### Список параметрів

`data_len`

Розмір даних для читання.

### Значення, що повертаються

Масив, в якому перший елемент представляє розмір прочитаних даних, а другий буферизовані дані. У разі невдачі при читанні метод поверне **`false`**

### Дивіться також

-   [GearmanTask::sendData()](gearmantask.senddata.html) - Надсилання даних завдання (застарілий метод)