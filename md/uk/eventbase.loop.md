Надсилання очікуваних подій

-   [« EventBase::gotStop](eventbase.gotstop.md)
    
-   [EventBase::priorityInit »](eventbase.priorityinit.md)
    
-   [PHP Manual](index.md)
    
-   [EventBase](class.eventbase.md)
    
-   Надсилання очікуваних подій
    

# EventBase::loop

(PECL event >= 1.2.6-beta)

EventBase::loop — Надсилання очікуваних подій

### Опис

```methodsynopsis
public
   EventBase::loop(
    int
     $flags
    = ?): bool
```

Очікує, доки події стануть активними, і запускає їх callback-функції.

**Увага**

*НЕ* руйнуйте об'єкт [EventBase](class.eventbase.md) доки не звільнені пов'язані з `Event` ресурси. В іншому випадку це призведе до непередбачуваних результатів!

### Список параметрів

`flags`

Необов'язкові прапори. Одна з констант `EventBase::LOOP_*`. Дивіться [EventBase константи](class.eventbase.html#eventbase.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBase::dispatch()](eventbase.dispatch.md) - Відправляє очікувані події