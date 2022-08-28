Надсилання статусу невдалої операції (застарілий метод)

-   [« GearmanJob::exception](gearmanjob.exception.html)
    
-   [GearmanJob::functionName »](gearmanjob.functionname.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanJob](class.gearmanjob.html)
    
-   Надсилання статусу невдалої операції (застарілий метод)
    

# GearmanJob::fail

(PECL gearman <= 0.5.0)

GearmanJob::fail — Надсилання статусу невдалої операції (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::fail(): bool
```

Посилає статус про невдалу обробку, вказуючи, що завдання завершилося невдало з відомих причин (на відміну невдалого завершення, коли викидається виняток).

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendFail()](gearmanjob.sendfail.html) у версії 0.6.0 модуля Gearman.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendException()](gearmanjob.sendexception.html) - Відправлення виключення завдання, що виконується
-   [GearmanJob::setReturn()](gearmanjob.setreturn.html) - Встановлення значення, що повертається
-   [GearmanJob::sendStatus()](gearmanjob.sendstatus.html) - Надсилання статусу
-   [GearmanJob::sendWarning()](gearmanjob.sendwarning.html) - Відправлення попередження