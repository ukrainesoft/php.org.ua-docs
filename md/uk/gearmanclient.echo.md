Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод

-   [« GearmanClient::doStatus](gearmanclient.dostatus.md)
    
-   [GearmanClient::error »](gearmanclient.error.md)
    
-   [PHP Manual](index.md)
    
-   [GearmanClient](class.gearmanclient.md)
    
-   Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод
    

# GearmanClient::echo

(PECL gearman >= 0.5.0)

GearmanClient::echo — Надсилає дані всім серверам завдань, щоб перевірити відгук Застарілий метод

### Опис

```methodsynopsis
public GearmanClient::echo(string $workload): bool
```

Метод **GearmanClient::echo()** застарів з pecl/gearman 1.0.0. Використовуйте [GearmanClient::ping()](gearmanclient.ping.md)

### Список параметрів

`workload`

Деякі довільні серіалізовані дані для отримання відгуку

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.