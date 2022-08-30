Метод оновлює запис у хеші новим значенням

-   [« QuickHashStringIntHash::set](quickhashstringinthash.set.md)
    
-   [QuickHashIntStringHash »](class.quickhashintstringhash.md)
    
-   [PHP Manual](index.md)
    
-   [QuickHashStringIntHash](class.quickhashstringinthash.md)
    
-   Метод оновлює запис у хеші новим значенням
    

# QuickHashStringIntHash::update

(No version information available, might only be in Git)

QuickHashStringIntHash::update — Метод оновлює запис у хеші новим значенням

### Опис

```methodsynopsis
public QuickHashStringIntHash::update(string $key, int $value): bool
```

Метод оновлює запис новим значенням і повертає, чи запис оновлено. Якщо є дублікати ключів, лише перший знайдений елемент набуде оновленого значення. Використовуйте константу **`QuickHashStringIntHash::CHECK_FOR_DUPES`** під час створення хешу, щоб запобігти попаданню дублюючих ключів у хеш.

### Список параметрів

`key`

Ключ запису, що оновлюється.

`value`

Нове значення запису. Якщо передається нестрокове значення, воно буде автоматично перетворено на рядок, якщо це можливо.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було знайдено та оновлено та **`false`**, якщо запис був частиною хеша.

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::update()****

```php
<?php
$hash = new QuickHashStringIntHash( 1024 );

$hash->add( 'шесть', 314159265 );
$hash->add( "множество", 314159265 );

echo $hash->get( 'шесть' ), "\n";
echo $hash->get( 'множество' ), "\n";

var_dump( $hash->update( 'множество', 314159266 ) );
var_dump( $hash->update( "множество плюс один", 314159999 ) );

echo $hash->get( 'шесть' ), "\n";
echo $hash->get( 'множество' ), "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
314159265
314159265
bool(true)
bool(false)
314159265
314159266
```