---
navigation:
  - migration70.new-features.md: « Нова функціональність
  - migration70.changed-functions.md: Змінені функції »
  - index.md: PHP Manual
  - migration70.md: Міграція з PHP 5.6.x на PHP 7.0.x
title: 'Функціональність, оголошена застарілою PHP 7.0.x'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Функціональність, оголошена застарілою PHP 7.0.x

### Конструктори у стилі PHP 4

Конструктори в стилі PHP 4 (методи з тим самим ім'ям, що і сам клас) оголошені застарілими та будуть видалені у майбутньому. У PHP 7 видаватиметься попередження **`E_DEPRECATED`** у разі використання таких конструкторів. Класи, що реалізують метод **\_\_construct()**, торкнуті не будуть.

```php
<?php
class foo {
    function foo() {
        echo 'Я конструктор!';
    }
}
?>
```

Результат виконання наведеного прикладу:

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

Результат виконання наведеного прикладу:

```
Deprecated: Non-static method foo::bar() should not be called statically in - on line 8
Я не статический!
```

### Опция salt функции[password\_hash()](function.password-hash.md)

Опция salt функции[password\_hash()](function.password-hash.md) була оголошена застарілою для запобігання використанню розробниками своїх власних salt (часто небезпечних). Функція самостійно генерує криптографічно безпечний salt, якщо він не заданий розробником, отже більше немає потреби в генераторах користувача salt.

### Опция контекста SSL`capture_session_meta`

Опция контекста SSL`capture_session_meta` оголошено застарілою. Метадані SSL тепер доступні за допомогою функції [stream\_get\_meta\_data()](function.stream-get-meta-data.md)

### Застарілі функції [LDAP](book.ldap.md)

Наступні функції були оголошені застарілими:

-   [ldap\_sort()](function.ldap-sort.md)
