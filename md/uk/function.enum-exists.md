Перевіряє, чи визначено перерахування

-   [« class\_exists](function.class-exists.html)
    
-   [get\_called\_class »](function.get-called-class.html)
    
-   [PHP Manual](index.html)
    
-   [Функции работы с классами и объектами](ref.classobj.html)
    
-   Перевіряє, чи визначено перерахування
    

# enumexists

(PHP 8> = 8.1.0)

enumexists — Перевіряє, чи визначено перерахування

### Опис

```methodsynopsis
enum_exists(string $enum, bool $autoload = true): bool
```

Функція перевіряє, чи визначено цей перелік.

### Список параметрів

`enum`

Ім'я переліку. Ім'я зіставляється без урахування регістру.

`autoload`

Чи слід викликати [\_\_autoload](language.oop5.autoload.html) за замовчуванням.

### Значення, що повертаються

Повертає **`true`**, якщо перерахування `enum` визначено або **`false`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **enumexists()****

```php
<?php
// Убедитесь, что перечисление существует, прежде чем пытаться его использовать
if (enum_exists(Suit::class)) {
    $myclass = Suit::Hearts;
}
?>
```

### Дивіться також

-   [function\_exists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
-   [class\_exists()](function.class-exists.html) - Перевіряє, чи був оголошений клас
-   [interface\_exists()](function.interface-exists.html) - Перевіряє, чи визначено інтерфейс
-   [get\_declared\_classes()](function.get-declared-classes.html) - Повертає масив із іменами оголошених класів