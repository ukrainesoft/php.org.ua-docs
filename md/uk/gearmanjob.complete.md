Надсилання результату та статусу завершення (застарілий метод)

-   [« GearmanJob](class.gearmanjob.html)
    
-   [GearmanJob::\_\_construct »](gearmanjob.construct.html)
    
-   [PHP Manual](index.html)
    
-   [GearmanJob](class.gearmanjob.html)
    
-   Надсилання результату та статусу завершення (застарілий метод)
    

# GearmanJob::complete

(PECL gearman <= 0.5.0)

GearmanJob::complete — Надсилання результату та статусу завершення (застарілий метод)

### Опис

```methodsynopsis
public GearmanJob::complete(string $result): bool
```

Надсилає результати обробки клієнту та оновлює статус роботи на завершений.

> **Зауваження**
> 
> Цей метод було замінено на [GearmanJob::sendComplete()](gearmanjob.sendcomplete.html) у випуску модуля Gearman 0.6.0.

### Список параметрів

`result`

Серіалізовані результати опрацювання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [GearmanJob::sendFail()](gearmanjob.sendfail.html) - Відправлення статусу невдалої операції
-   [GearmanJob::setReturn()](gearmanjob.setreturn.html) - Встановлення значення, що повертається