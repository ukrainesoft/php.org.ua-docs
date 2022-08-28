Задає режим вилучення вузлів

-   [« SplPriorityQueue::rewind](splpriorityqueue.rewind.html)
    
-   [SplPriorityQueue::top »](splpriorityqueue.top.html)
    
-   [PHP Manual](index.html)
    
-   [SplPriorityQueue](class.splpriorityqueue.html)
    
-   Задає режим вилучення вузлів
    

# SplPriorityQueue::setExtractFlags

(PHP 5> = 5.3.0, PHP 7, PHP 8)

SplPriorityQueue::setExtractFlags — Задає режим вилучення вузлів

### Опис

```methodsynopsis
public SplPriorityQueue::setExtractFlags(int $flags): int
```

### Список параметрів

`flags`

Визначає, що витягуватиметься методами [SplPriorityQueue::current()](splpriorityqueue.current.html) [SplPriorityQueue::top()](splpriorityqueue.top.html) і [SplPriorityQueue::extract()](splpriorityqueue.extract.html)

-   **`SplPriorityQueue::EXTR_DATA`** (0x00000001): Витягувати дані
-   **`SplPriorityQueue::EXTR_PRIORITY`** (0x00000002): Отримувати пріоритет
-   **`SplPriorityQueue::EXTR_BOTH`** (0x00000003): Витягувати дані та пріоритет у вигляді масиву

За замовчуванням працює режим **`SplPriorityQueue::EXTR_DATA`**

### Значення, що повертаються

Повертає прапори вилучення.