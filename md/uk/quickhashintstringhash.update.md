---
navigation:
  - quickhashintstringhash.set.md: '« QuickHashIntStringHash::set'
  - book.reflection.md: Reflection »
  - index.md: PHP Manual
  - class.quickhashintstringhash.md: QuickHashIntStringHash
title: 'QuickHashIntStringHash::update'
---
# QuickHashIntStringHash::update

(PECL quickhash >= Unknown)

QuickHashIntStringHash::update — Метод оновлює запис у хеші новим значенням

### Опис

```methodsynopsis
public QuickHashIntStringHash::update(int $key, string $value): bool
```

Метод оновлює запис новим значенням і повертає, чи запис оновлено. Якщо є дублікати ключів, лише перший знайдений елемент набуде оновленого значення. Використовуйте константу **`QuickHashIntStringHash::CHECK_FOR_DUPES`** під час створення хешу, щоб запобігти попаданню дублюючих ключів у хеш.

### Список параметрів

`key`

Ключ запису, що оновлюється.

`value`

Нове значення запису. Якщо передається нестрокове значення, воно буде автоматично перетворено на рядок, якщо це можливо.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було знайдено та оновлено та **`false`**, якщо запис був частиною хеша.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntStringHash::update()****

```php
<?php
$hash->add( 161803398, "--" );
$hash->add( 314159265, "множество" );

echo $hash->get( 161803398 ), "\n";
echo $hash->get( 314159265 ), "\n";

var_dump( $hash->update( 314159265, "множество плюс один" ) );
var_dump( $hash->update( 314159999, "множество плюс один" ) );

echo $hash->get( 161803398 ), "\n";
echo $hash->get( 314159265 ), "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
--
множество
bool(true)
bool(false)
--
множество плюс один
```
