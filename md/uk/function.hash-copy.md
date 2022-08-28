Копіює контекст хешування

-   [« hash\_algos](function.hash-algos.html)
    
-   [hash\_equals »](function.hash-equals.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Hash](ref.hash.html)
    
-   Копіює контекст хешування
    

# hashcopy

(PHP 5> = 5.3.0, PHP 7, PHP 8)

hashcopy — Копіює контекст хешування

### Опис

```methodsynopsis
hash_copy(HashContext $context): HashContext
```

### Список параметрів

`context`

Контекст хешування, повернутий [hash\_init()](function.hash-init.html)

### Значення, що повертаються

Повертає копію контексту хешування.

### список змін

| Версия | Описание |
| --- | --- |
|  | Приймає та повертає [HashContext](class.hashcontext.html), а чи не ресурс. |

### Приклади

**Приклад #1 Приклад використання **hashcopy()****

```php
<?php
$context = hash_init("md5");
hash_update($context, "data");

/* копия контекста для дальнейшего использования */
$copy_context = hash_copy($context);

echo hash_final($context), "\n";

hash_update($copy_context, "data");
echo hash_final($copy_context), "\n";
?>
```

Результат виконання цього прикладу:

```
8d777f385d3dfec8815d20f7496026dc
511ae0b1c13f95e5f08f1a0dd3da3d93
```