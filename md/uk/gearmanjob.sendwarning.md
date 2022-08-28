Надсилання попередження

-   [« GearmanJob::sendStatus](gearmanjob.sendstatus.html)
    
-   [GearmanJob::setReturn »](gearmanjob.setreturn.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanJob](class.gearmanjob.html)
    
-   Надсилання попередження
    

# GearmanJob::sendWarning

(PECL gearman >= 0.6.0)

GearmanJob::sendWarning — Надсилання попередження

### Опис

```methodsynopsis
public GearmanJob::sendWarning(string $warning): bool
```

Під час виконання роботи надсилає попередження.

### Список параметрів

`warning`

Повідомлення попередження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendComplete()](gearmanjob.sendcomplete.html) - Відправлення результату та статусу завершення
-   [GearmanJob::sendException()](gearmanjob.sendexception.html) - Відправлення виключення завдання, що виконується
-   [GearmanJob::sendFail()](gearmanjob.sendfail.html) - Відправлення статусу невдалої операції