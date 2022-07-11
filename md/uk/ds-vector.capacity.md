- [« Ds\Vector::apply](ds-vector.apply.md)
- [Ds\Vector::clear »](ds-vector.clear.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Повертає поточну місткість

# Ds\Vector::capacity

(PECL ds \>= 1.0.0)

Ds\Vector::capacity — Повертає поточну місткість

### Опис

public **Ds\Vector::capacity**(): int

Повертає поточну місткість.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточна місткість.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::capacity()****

` <?php$vector = new \Ds\Vector();var_dump($vector->capacity());$vector->push(...range(1, 50));var_dump($vector->capacity ());$vector[] = "a";var_dump($vector->capacity());?> `

Результатом виконання цього прикладу буде щось подібне:

int(10)
int(50)
int(75)
