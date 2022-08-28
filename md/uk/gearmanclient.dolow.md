Запускає виконання завдання з низьким пріоритетом

-   [« GearmanClient::doJobHandle](gearmanclient.dojobhandle.html)
    
-   [GearmanClient::doLowBackground »](gearmanclient.dolowbackground.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Запускає виконання завдання з низьким пріоритетом
    

# GearmanClient::doLow

(PECL gearman >= 0.5.0)

GearmanClient::doLow - Запускає на виконання завдання з низьким пріоритетом

### Опис

```methodsynopsis
public GearmanClient::doLow(string $function_name, string $workload, string $unique = ?): string
```

Запускає виконання завдання з низьким пріоритетом і повертає рядок, що містить результат. Функція залежить від [GearmanClient](class.gearmanclient.html) і [GearmanWorker](class.gearmanworker.html)оскільки необхідно забезпечити єдиний формат результату. Високопріоритетні завдання мають перевагу над звичайними та низькопріоритетними завданнями у черзі завдань. Завдання нормального та високого пріоритету мають перевагу над низькопріоритетними завданнями у черзі завдань.

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Рядок, що містить результат виконання завдання.

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.html) - Виконує одиночне завдання та повертає результат
-   [GearmanClient::doHigh()](gearmanclient.dohigh.html) - Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.html) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doHighBackground()](gearmanclient.dohighbackground.html) - Запускає на виконання із високим пріоритетом завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.html) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі