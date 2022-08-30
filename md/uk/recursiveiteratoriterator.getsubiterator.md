Отримання активного вкладеного ітератора

-   [« RecursiveIteratorIterator::getMaxDepth](recursiveiteratoriterator.getmaxdepth.md)
    
-   [RecursiveIteratorIterator::key »](recursiveiteratoriterator.key.md)
    
-   [PHP Manual](index.md)
    
-   [RecursiveIteratorIterator](class.recursiveiteratoriterator.md)
    
-   Отримання активного вкладеного ітератора
    

# RecursiveIteratorIterator::getSubIterator

(PHP 5, PHP 7, PHP 8)

RecursiveIteratorIterator::getSubIterator — Отримання активного вкладеного ітератора

### Опис

```methodsynopsis
public RecursiveIteratorIterator::getSubIterator(?int $level = null): ?RecursiveIterator
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`level`

### Значення, що повертаються

Активний вкладений ітератор у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                              |
|--------|---------------------------------------|
|        | `level` тепер допускає значення null. |