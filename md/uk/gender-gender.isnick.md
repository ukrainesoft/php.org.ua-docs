Перевіряє, чи є name0 псевдонімом для name1

-   [« Gender\\Gender::get](gender-gender.get.html)
    
-   [Gender\\Gender::similarNames »](gender-gender.similarnames.html)
    
-   [PHP Manual](index.html)
    
-   [Gender\\Gender](class.gender.html)
    
-   Перевіряє, чи є name0 псевдонімом для name1
    

# GenderGender::isNick

(PECL gender >= 0.9.0)

GenderGender::isNick — Перевіряє, чи є name0 псевдонімом для name1

### Опис

```methodsynopsis
public Gender\Gender::isNick(string $name0, string $name1, int $country = ?): array
```

Перевіряє, чи name0 є псевдонімом для name1.

### Список параметрів

`name0`

Ім'я для перевірки.

`name1`

Ім'я для перевірки.

`country`

Ідентифікатор країни, яка визначається константою класу Gender. Якщо опущений, то використовується ANYCOUNTRY.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.