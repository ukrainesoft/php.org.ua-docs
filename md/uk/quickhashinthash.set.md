---
navigation:
  - quickhashinthash.savetostring.md: '« QuickHashIntHash::saveToString'
  - quickhashinthash.update.md: 'QuickHashIntHash::update »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::set

(PECL quickhash >= Unknown)

QuickHashIntHash::set — Метод оновлює запис у хеші новим значенням або додає новий, якщо запис не існує

### Опис

```methodsynopsis
public QuickHashIntHash::set(int $key, int $value): bool
```

Метод намагається оновити запис новим значенням. Якщо запис ще не існує, замість цього додається новий запис. Повертається інформація про те, чи запис було додано або оновлено. Якщо є дублікати ключів, лише перший знайдений елемент набуде оновленого значення. Використовуйте константу **`QuickHashIntHash::CHECK_FOR_DUPES`** під час створення хешу, щоб запобігти попаданню дублюючих ключів у хеш.

### Список параметрів

`key`

Ключ запису, який потрібно додати або оновити.

`value`

Нове значення запису.

### Значення, що повертаються

Метод повертає 2, якщо запис було знайдено та оновлено, 1, якщо запис було додано або 0 у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання** QuickHashIntHash::set()\*\*\*\*

```php
<?php
$hash = new QuickHashIntHash( 1024 );

echo "Set->Add\n";
var_dump( $hash->get( 46692 ) );
var_dump( $hash->set( 46692, 16091 ) );
var_dump( $hash->get( 46692 ) );

echo "Set->Update\n";
var_dump( $hash->set( 46692, 29906 ) );
var_dump( $hash->get( 46692 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(false)
int(2)
int(16091)
Set->Update
int(1)
int(29906)
```
