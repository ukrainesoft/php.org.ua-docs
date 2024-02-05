---
navigation:
  - function.hash-algos.md: « hash\_algos
  - function.hash-equals.md: hash\_equals »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_copy

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

hash\_copy — Копіює контекст хешування

### Опис

```methodsynopsis
hash_copy(HashContext $context): HashContext
```

### Список параметрів

`context`

Контекст хешування, повернутий [hash\_init()](function.hash-init.md)

### Значення, що повертаються

Повертає копію контексту хешування.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Приймає та повертає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Приклади

**Пример #1 Пример использования**hash\_copy()\*\*\*\*

```php
<?php
$context = hash_init("sha256");
hash_update($context, "Наглый коричневый лисёнок");

/* копия контекста для дальнейшего использования */
$copy_context = hash_copy($context);

echo hash_final($context), "\n";

hash_update($copy_context, "прыгает вокруг ленивой собаки.");
echo hash_final($copy_context), "\n";
?>
```

Результат виконання наведеного прикладу:

```
49fd7dddcdc0e0e6b2252f966b750d78536e8cd2677bf84db0c605652f7f1699
8b0ec9465a2a0befe6b45bc081e32e4629a7f3e39dcf1fda31af101b8d85145b
```
