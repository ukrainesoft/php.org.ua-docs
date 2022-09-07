---
navigation:
  - quickhashstringinthash.savetostring.md: '« QuickHashStringIntHash::saveToString'
  - quickhashstringinthash.update.md: 'QuickHashStringIntHash::update »'
  - index.md: PHP Manual
  - class.quickhashstringinthash.md: QuickHashStringIntHash
title: 'QuickHashStringIntHash::set'
---
# QuickHashStringIntHash::set

(No version information available, might only be in Git)

QuickHashStringIntHash::set — Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує

### Опис

```methodsynopsis
public QuickHashStringIntHash::set(string $key, int $value): int
```

Метод намагається оновити запис новим значенням. Якщо запис ще не існує, замість цього додається новий запис. Повертається інформація про те, чи запис було додано або оновлено. Якщо є дублікати ключів, лише перший знайдений елемент набуде оновленого значення. Використовуйте константу **`QuickHashStringIntHash::CHECK_FOR_DUPES`** під час створення хешу, щоб запобігти попаданню дублюючих ключів у хеш.

### Список параметрів

`key`

Ключ запису, який потрібно додати або оновити.

`value`

Значення запису. Якщо передається нестрокове значення, воно буде автоматично перетворено на рядок, якщо це можливо.

### Значення, що повертаються

Метод повертає 2, якщо запис було знайдено та оновлено, 1, якщо запис було додано або 0 у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **QuickHashStringIntHash::set()****

```php
<?php
$hash = new QuickHashStringIntHash( 1024 );

echo "Set->Add\n";
var_dump( $hash->get( "сорок шесть тысяч шестьсот девяносто два" ) );
var_dump( $hash->set( "сорок шесть тысяч шестьсот девяносто два", 16091 ) );
var_dump( $hash->get( "сорок шесть тысяч шестьсот девяносто два" ) );

echo "Set->Update\n";
var_dump( $hash->set( "сорок шесть тысяч шестьсот девяносто два", 29906 ) );
var_dump( $hash->get( "сорок шесть тысяч шестьсот девяносто два" ) );
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Set->Add
bool(false)
int(2)
int(16091)
Set->Update
int(1)
int(29906)
```
