Перевіряє, чи існує трейт

-   [« property\_exists](function.property-exists.html)
    
-   [Ctype »](book.ctype.html)
    
-   [PHP Manual](index.html)
    
-   [Функции работы с классами и объектами](ref.classobj.html)
    
-   Перевіряє, чи існує трейт
    

# traitexists

(PHP 5> = 5.4.0, PHP 7, PHP 8)

traitexists — Перевіряє, чи існує трейт

### Опис

```methodsynopsis
trait_exists(string $trait, bool $autoload = true): bool
```

### Список параметрів

`trait`

Ім'я трейту для перевірки

`autoload`

Чи намагатиметься його завантажити автоматично

### Значення, що повертаються

Повертає **`true`**якщо трейт існує, в іншому випадку повертає **`false`**