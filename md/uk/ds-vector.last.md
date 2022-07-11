- [« Ds\Vector::jsonSerialize](ds-vector.jsonserialize.md)
- [Ds\Vector::map »](ds-vector.map.md)

- [PHP Manual](index.md)
- [Вектор](class.ds-vector.md)
- Повертає останнє значення вектора

# Ds\Vector::last

(PECL ds \>= 1.0.0)

Ds\Vector::last — Повертає останнє значення вектора

### Опис

public **Ds\Vector::last**():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Повертає останнє значення вектора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Останній елемент вектор.

### Помилки

Викидає виняток
[UnderflowException](class.underflowexception.md), якщо вектор порожній.

### Приклади

**Приклад #1 Приклад використання **Ds\Vector::last()****

` <?php$vector = new \Ds\Vector([1, 2, 3]);var_dump($vector->last());?> `

Результатом виконання цього прикладу буде щось подібне:

int(3)
