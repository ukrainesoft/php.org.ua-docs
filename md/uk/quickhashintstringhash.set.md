Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує

-   [« QuickHashIntStringHash::saveToString](quickhashintstringhash.savetostring.html)
    
-   [QuickHashIntStringHash::update »](quickhashintstringhash.update.html)
    
-   [PHP Manual](index.html)
    
-   [QuickHashIntStringHash](class.quickhashintstringhash.html)
    
-   Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує
    

# QuickHashIntStringHash::set

(PECL quickhash >= Unknown)

QuickHashIntStringHash::set — Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує

### Опис

```methodsynopsis
public QuickHashIntStringHash::set(int $key, string $value): int
```

Метод намагається оновити запис новим значенням. Якщо запис ще не існує, замість цього додається новий запис. Повертається інформація про те, чи запис було додано або оновлено. Якщо є дублікати ключів, лише перший знайдений елемент набуде оновленого значення. Використовуйте константу **`QuickHashIntStringHash::CHECK_FOR_DUPES`** під час створення хешу, щоб запобігти попаданню дублюючих ключів у хеш.

### Список параметрів

`key`

Ключ запису, який потрібно додати або оновити.

`value`

Значення запису. Якщо передається нестрокове значення, воно буде автоматично перетворено на рядок, якщо це можливо.

### Значення, що повертаються

Метод повертає 2, якщо запис було знайдено та оновлено, 1, якщо запис було додано або 0 у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntStringHash::set()****

```php
<?php
$hash = new QuickHashIntStringHash( 1024 );

echo "Set->Add\n";
var_dump( $hash->get( 46692 ) );
var_dump( $hash->set( 46692, "шестнадцать тысяч девяносто один" ) );
var_dump( $hash->get( 46692 ) );

echo "Set->Update\n";
var_dump( $hash->set( 46692, "двадцать девять тысяч девятьсот шесть" ) );
var_dump( $hash->get( 46692 ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Set->Add
bool(false)
int(2)
string(27) "шестнадцать тысяч девяносто один"
Set->Update
int(1)
string(37) "двадцать девять тысяч девятьсот шесть"
```