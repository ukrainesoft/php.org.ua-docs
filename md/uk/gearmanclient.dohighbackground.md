Запускає виконання з високим пріоритетом завдання у фоновому режимі

-   [« GearmanClient::doHigh](gearmanclient.dohigh.html)
    
-   [GearmanClient::doJobHandle »](gearmanclient.dojobhandle.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Запускає виконання з високим пріоритетом завдання у фоновому режимі
    

# GearmanClient::doHighBackground

(PECL gearman >= 0.5.0)

GearmanClient::doHighBackground — Запускає на виконання з високим пріоритетом завдання у фоновому режимі

### Опис

```methodsynopsis
public GearmanClient::doHighBackground(string $function_name, string $workload, string $unique = ?): string
```

Запускає виконання з високим пріоритетом завдання у фоновому режимі, повертаючи дескриптор завдання, який може бути надалі використаний для запиту стану завдання, що виконується. Завдання високого пріоритету мають перевагу над нормальними та низькопріоритетними завданнями у черзі завдань.

### Список параметрів

`function_name`

Зареєстрована функція, що викликається робочим процесом

`workload`

Серіалізовані дані, що підлягають обробці

`unique`

Унікальний ID, який призначається певному завданню

### Значення, що повертаються

Дескриптор відправленого завдання.

### Дивіться також

-   [GearmanClient::doNormal()](gearmanclient.donormal.html) - Виконує одиночне завдання та повертає результат
-   [GearmanClient::doHigh()](gearmanclient.dohigh.html) - Запускає на виконання завдання із високим пріоритетом
-   [GearmanClient::doLow()](gearmanclient.dolow.html) - Запускає виконання завдання з низьким пріоритетом
-   [GearmanClient::doBackground()](gearmanclient.dobackground.html) - Запускає виконання завдання у фоновому режимі
-   [GearmanClient::doLowBackground()](gearmanclient.dolowbackground.html) - Запускає на виконання з низьким пріоритетом завдання у фоновому режимі