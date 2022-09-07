---
navigation:
  - migration70.new-features.md: « Новая функциональность
  - migration70.changed-functions.md: Змінені функції »
  - index.md: PHP Manual
  - migration70.md: Миграция с PHP 5.6.x на PHP 7.0.x
title: 'Функціональність, оголошена застарілою PHP 7.0.x'
---
## Функціональність, оголошена застарілою PHP 7.0.x

### Конструктори у стилі PHP 4

Конструктори в стилі PHP 4 (методи з тим самим ім'ям, що і сам клас) оголошені застарілими та будуть видалені у майбутньому. У PHP 7 видаватиметься попередження **`E_DEPRECATED`** у разі використання таких конструкторів. Класи, що реалізують метод **construct()**, торкнуті не будуть.

```php
<?php
class foo {
    function foo() {
        echo 'Я конструктор!';
    }
}
?>
```

Результат виконання цього прикладу:

```
Deprecated: Methods with the same name as their class will not be constructors in a future version of PHP; foo has a deprecated constructor in example.php on line 3
```

### Статичні виклики нестатичних методів

[Статичні](language.oop5.static.md) виклики методів, не визначених як **static**, оголошені застарілими та можуть бути в майбутньому заборонені.

```php
<?php
class foo {
    function bar() {
        echo 'Я не статический!';
    }
}

foo::bar();
?>
```

Результат виконання цього прикладу:

```
Deprecated: Non-static method foo::bar() should not be called statically in - on line 8
Я не статический!
```

### Опція salt функції [passwordhash()](function.password-hash.md)

Опція salt функції [passwordhash()](function.password-hash.md) була оголошена застарілою для запобігання використанню розробниками своїх власних salt (часто небезпечних). Функція самостійно генерує криптографічно безпечний salt, якщо він не заданий розробником, отже більше немає потреби в генераторах користувача salt.

### Опція контексту SSL `capture_session_meta`

Опція контексту SSL `capture_session_meta` оголошено застарілою. Метадані SSL тепер доступні за допомогою функції [streamgetmetadata()](function.stream-get-meta-data.md)

### Застарілі функції [LDAP](book.ldap.md)

Наступні функції були оголошені застарілими:

-   [ldapsort()](function.ldap-sort.md)
