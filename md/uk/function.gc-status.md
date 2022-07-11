- [«gc_mem_caches](function.gc-mem-caches.md)
- [get_cfg_var »](function.get-cfg-var.md)

- [PHP Manual](index.md)
- [Опції PHP/інформаційні функції](ref.info.md)
- Повертає інформацію про поточний статус збирача сміття

# gc_status

(PHP 7 \>= 7.3.0, PHP 8)

gc_status — Повертає інформацію про поточний статус збирача сміття

### Опис

**gc_status**(): array

Повертає інформацію про поточний статус збирача сміття.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає асоціативний масив із такими елементами:

- ``runs'`
- ``collected'`
- ``threshold'`
- ``roots'`

### Приклади

**Приклад #1 Використання **gc_status()****

`<?php// створимо дерево об'єктів, для потрібно збирати сміття$a = new stdClass();$a->b = [];for ($i = 0; $i  = new stdClass(); $b->a = $a; $a->b[] = $b;}unset($a);unset($b);gc_collect_cycles();var_dump(gc_status()); `

Результатом виконання цього прикладу буде щось подібне:

array(4) {
["runs"]=>
int(5)
["collected"]=>
int(100002)
["threshold"]=>
int(50001)
["roots"]=>
int(0)
}

### Дивіться також

- [Збір сміття](features.gc.md)
