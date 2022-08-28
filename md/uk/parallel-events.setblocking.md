Поведінка

-   [« parallel\\Events](class.parallel-events.html)
    
-   [parallel\\Events::setTimeout »](parallel-events.settimeout.html)
    
-   [PHP Manual](index.html)
    
-   [parallel\\Events](class.parallel-events.html)
    
-   Поведінка
    

# parallelEvents::setBlocking

parallelEvents::setBlocking — Поведінка

### Опис

За замовчуванням, коли опитуються події, блокування відбуватиметься (на рівні PHP) доти, доки не буде повернена перша подія: встановлення режиму блокування в **`false`** призведе до того, що опитування поверне управління, якщо перша мета не готова.

Відрізняється від часу очікування 0 за допомогою [parallel\\Events::setTimeout()](parallel-events.settimeout.html), оскільки час очікування 0, хоч і дозволено, викине виняток, який може бути надзвичайно повільним або марнотратним, якщо дійсно потрібна неблокуюча поведінка.

Неблокуючий цикл впливає на значення, що повертається [parallel\\Events::poll()](parallel-events.poll.html)так воно може бути **`null`** до того, як усі події будуть опрацьовані.

```methodsynopsis
public parallel\Events::setBlocking(bool $blocking): void
```

Встановлює режим блокування

### Помилки

**Увага**

Викидає parallelEventsError, якщо для циклу встановлено час очікування.