- [« spl_autoload](function.spl-autoload.md)
- [spl_object_hash »](function.spl-object-hash.md)

- [PHP Manual](index.md)
- [Функції SPL](ref.spl.md)
- Повертає доступні класи SPL

# spl_classes

(PHP 5, PHP 7, PHP 8)

spl_classes — Повертає доступні класи SPL

### Опис

**spl_classes**(): array

Ця функція повертає масив з доступними в даний час класами
SPL.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array) з доступними нині класами SPL.

### Приклади

**Приклад #1 Приклад використання **spl_classes()****

` <?phpprint_r(spl_classes());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[ArrayObject] => ArrayObject
[ArrayIterator] => ArrayIterator
[CachingIterator] => CachingIterator
[RecursiveCachingIterator] => RecursiveCachingIterator
[DirectoryIterator] => DirectoryIterator
[FilterIterator] => FilterIterator
[LimitIterator] => LimitIterator
[ParentIterator] => ParentIterator
[RecursiveDirectoryIterator] => RecursiveDirectoryIterator
[RecursiveIterator] => RecursiveIterator
[RecursiveIteratorIterator] => RecursiveIteratorIterator
[SeekableIterator] => SeekableIterator
[SimpleXMLIterator] => SimpleXMLIterator
)
