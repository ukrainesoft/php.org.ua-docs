Метод перевіряє, чи є ключ частиною набору

-   [« QuickHashIntSet::delete](quickhashintset.delete.html)
    
-   [QuickHashIntSet::getSize »](quickhashintset.getsize.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashIntSet](class.quickhashintset.html)
    
-   Метод перевіряє, чи є ключ частиною набору
    

# QuickHashIntSet::exists

(PECL quickhash >= Unknown)

QuickHashIntSet::exists — Метод перевіряє, чи є ключем частиною набору

### Опис

```methodsynopsis
public QuickHashIntSet::exists(int $key): bool
```

Метод перевіряє, чи існує в наборі запис із зазначеним ключем.

### Список параметрів

`key`

Ключ запису для перевірки її існування у наборі.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було знайдено або **`false`**, якщо запис не знайдено.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntSet::exists()****

```php
<?php
// создание 200000 элементов
$array = range( 0, 199999 );
$existingEntries = array_rand( array_flip( $array ), 180000 );
$testForEntries = array_rand( array_flip( $array ), 1000 );
$foundCount = 0;

echo "Создание набора: ", microtime( true ), "\n";
$set = new QuickHashIntSet( 100000 );
echo "Добавление элементов: ", microtime( true ), "\n";
foreach( $existingEntries as $key )
{
     $set->add( $key );
}

echo "Выполнение 1000 тестов: ", microtime( true ), "\n";
foreach( $testForEntries as $key )
{
     $foundCount += $set->exists( $key );
}
echo "Готово, $foundCount найдено: ", microtime( true ), "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Создание набора: 1263588703.0748
Добавление элементов: 1263588703.0757
Выполнение 1000 тестов: 1263588703.7851
Готово, $foundCount найдено: 1263588703.7897
```