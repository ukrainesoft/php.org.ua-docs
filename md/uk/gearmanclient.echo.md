Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод

-   [« GearmanClient::doStatus](gearmanclient.dostatus.html)
    
-   [GearmanClient::error »](gearmanclient.error.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanClient](class.gearmanclient.html)
    
-   Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод
    

# GearmanClient::echo

(PECL gearman >= 0.5.0)

GearmanClient::echo — Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод

### Опис

```methodsynopsis
public GearmanClient::echo(string $workload): bool
```

Метод **GearmanClient::echo()** застарів з pecl/gearman 1.0.0. Використовуйте [GearmanClient::ping()](gearmanclient.ping.html)

### Список параметрів

`workload`

Деякі довільні серіалізовані дані для отримання відгуку

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.