- [«Collator::getStrength](collator.getstrength.md)
- [Collator::setStrength »](collator.setstrength.md)

- [PHP Manual](index.md)
- [Collator](class.collator.md)
- Встановлює атрибут зіставлення

# Collator::setAttribute

#collator_set_attribute

(PHP 5 = 5.3.0, PHP 7, PHP 8, PECL intl = 1.0.0)

Collator::setAttribute -- collator_set_attribute -- Встановлює атрибут
зіставлення

### Опис

Об'єктно-орієнтований стиль

public **Collator::setAttribute**(int `$attribute`, int `$value`): bool

Процедурний стиль

**collator_set_attribute**([Collator](class.collator.md) `$object`,
int `$attribute`, int `$value`): bool

### Список параметрів

`object`
Об'єкт [Collator](class.collator.md).

`attribute`
Атрибут.

`value`
Значення атрибуту.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у
у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **collator_set_attribute()****

` <?php$coll = collator_create( 'en_CA' );$val = collator_get_attribute( $coll, Collator::NUMERIC_COLLATION );if ($val ====false) { про=    = Collator::ON) {    // Робимо щось корисне.}?> `

### Дивіться також

- [Константи [Collator](class.collator.md)](class.collator.md#intl.collator-constants)
- [collator_get_attribute()](collator.getattribute.md) - Отримує
значення атрибуту зіставлення
- [collator_set_strength()](collator.setstrength.md) - Встановлює
силу зіставлення
