- [« DirectoryIterator::getMTime](directoryiterator.getmtime.md)
- [DirectoryIterator::getPath »](directoryiterator.getpath.md)

- [PHP Manual](index.md)
- [DirectoryIterator](class.directoryiterator.md)
- Повертає ідентифікатор власника поточного елемента
DirectoryIterator

# DirectoryIterator::getOwner

(PHP 5, PHP 7, PHP 8)

DirectoryIterator::getOwner — Повертає ідентифікатор власника
поточний елемент DirectoryIterator

### Опис

public **DirectoryIterator::getOwner**(): int

Повертає ідентифікатор власника поточного елемента
[DirectoryIterator](class.directoryiterator.md) у числовому форматі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Власник файлу, у числовому форматі.

### Приклади

**Приклад #1 Приклад використання **DirectoryIterator::getOwner()****

Приклад показує власника директорії, що містить скрипт, що виконується.

` <?php$iterator = new DirectoryIterator(dirname(__FILE__));print_r(posix_getpwuid($iterator->getOwner()));?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[name] => tom
[passwd] => x
[uid] => 501
[gid] => 42
[gecos] => Tom Cat
[dir] => /home/tom
[shell] => /bin/bash
)

### Дивіться також

- [DirectoryIterator::getGroup()](directoryiterator.getgroup.md) -
Повертає ідентифікатор групи поточного елемента DirectoryIterator
- [DirectoryIterator::getiNode()](directoryiterator.getinode.md) -
Повертає inode поточного елемента DirectoryIterator
- [DirectoryIterator::getPerms()](directoryiterator.getperms.md) -
Повертає набір прав для поточного елемента DirectoryIterator item
- [posix_getpwuid()](function.posix-getpwuid.md) - Повертає
інформацію про користувача, використовуючи його ID
