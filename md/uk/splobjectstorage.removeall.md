- [« SplObjectStorage::offsetUnset](splobjectstorage.offsetunset.md)
- [SplObjectStorage::removeAllExcept »](splobjectstorage.removeallexcept.md)

- [PHP Manual](index.md)
- [SplObjectStorage](class.splobjectstorage.md)
- Видаляє з поточного контейнера об'єкти, які є в іншому
контейнері

# SplObjectStorage::removeAll

(PHP 5 \>= 5.3.0, PHP 7, PHP 8)

SplObjectStorage::removeAll — Видаляє з поточного контейнера об'єкти,
які є в іншому контейнері

### Опис

public
**SplObjectStorage::removeAll**([SplObjectStorage](class.splobjectstorage.md)
`$storage`): int

Видаляє з поточного контейнера об'єкти, які є в іншому
контейнер.

### Список параметрів

`storage`
Контейнер містить елементи, які потрібно видалити.

### Значення, що повертаються

Повертає кількість об'єктів, що залишилися.

### Приклади

**Приклад #1 Приклад використання **SplObjectStorage::removeAll()****

` <?php$o1 = new StdClass;$o2 = new StdClass;$a = new SplObjectStorage();$a[$o1] = "foo";$b = new SplObjectStorage();$b$ "bar";$b[$o2] = "gee";var_dump(count($b));$b->removeAll($a);var_dump(count($b));?> `

Результатом виконання цього прикладу буде щось подібне:

int(2)
int(1)

### Дивіться також

- [SplObjectStorage::addAll()](splobjectstorage.addall.md) -
Додає всі об'єкти з іншого контейнера
