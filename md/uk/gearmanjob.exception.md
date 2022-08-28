Надсилання виключення (застарілий метод)

-   [« GearmanJob::data](gearmanjob.data.html)
    
-   [GearmanJob::fail »](gearmanjob.fail.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanJob](class.gearmanjob.html)
    
-   Надсилання виключення (застарілий метод)
    

# GearmanJob::exception

(PECL gearman <= 0.5.0)

GearmanJob::exception — Надсилання виключення (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::exception(string $exception): bool
```

Надсилає виняток, що виник під час виконання роботи.

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendException()](gearmanjob.sendexception.html) у модулі Gearman версії 0.6.0.

### Список параметрів

`exception`

Опис винятку.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::setReturn()](gearmanjob.setreturn.html) - Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.html) - Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.html) - Відправлення попередження