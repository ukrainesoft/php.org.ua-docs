Надсилання попередження (застарілий метод)

-   [« GearmanJob::unique](gearmanjob.unique.html)
    
-   [GearmanJob::workload »](gearmanjob.workload.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanJob](class.gearmanjob.html)
    
-   Надсилання попередження (застарілий метод)
    

# GearmanJob::warning

(PECL gearman <= 0.5.0)

GearmanJob::warning — Надсилання попередження (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::warning(string $warning): bool
```

Під час виконання завдання надсилає попередження.

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendWarning()](gearmanjob.sendwarning.html) у версії 0.6.0 модуля Gearman.

### Список параметрів

`warning`

Повідомлення попередження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendComplete()](gearmanjob.sendcomplete.html) - Відправлення результату та статусу завершення
-   [GearmanJob::sendException()](gearmanjob.sendexception.html) - Відправлення виключення завдання, що виконується
-   [GearmanJob::sendFail()](gearmanjob.sendfail.html) - Відправлення статусу невдалої операції