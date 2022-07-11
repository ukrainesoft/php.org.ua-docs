- [« SplObjectStorage::removeAll](splobjectstorage.removeall.md)
- [SplObjectStorage::rewind »](splobjectstorage.rewind.md)

- [PHP Manual](index.md)
- [SplObjectStorage](class.splobjectstorage.md)
- Видаляє з поточного контейнера всі об'єкти, яких немає в іншому
контейнері

# SplObjectStorage::removeAllExcept

(PHP 5 \>= 5.3.6, PHP 7, PHP 8)

SplObjectStorage::removeAllExcept — Видаляє з поточного контейнера все
об'єкти, яких немає в іншому контейнері

### Опис

public
**SplObjectStorage::removeAllExcept**([SplObjectStorage](class.splobjectstorage.md)
`$storage`): int

Видаляє з поточного контейнера всі об'єкти, яких немає в іншому
контейнер.

### Список параметрів

`storage`
Контейнер, який містить елементи, які повинні залишитися в поточному
контейнер.

### Значення, що повертаються

Повертає кількість об'єктів, що залишилися.

### Приклади

**Приклад #1 Приклад використання
**SplObjectStorage::removeAllExcept()****

` <?php$a = (object) 'a';$b = (object) 'b';$c = (object) 'c';$foo = new SplObjectStorage;$foo->attach($a); $foo->attach($b);$bar = new SplObjectStorage;$bar->attach($b);$bar->attach($c);$foo->removeAllExcept($bar);var_dump($foo ->contains($a));var_dump($foo->contains($b));?> `

Результатом виконання цього прикладу буде щось подібне:

bool(false)
bool(true)
