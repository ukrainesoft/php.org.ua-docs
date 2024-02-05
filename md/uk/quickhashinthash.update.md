---
navigation:
  - quickhashinthash.set.md: '« QuickHashIntHash::set'
  - class.quickhashstringinthash.md: QuickHashStringIntHash »
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::update'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# QuickHashIntHash::update

(PECL quickhash >= Unknown)

QuickHashIntHash::update — Метод оновлює запис у хеші новим значенням

### Опис

```methodsynopsis
public QuickHashIntHash::update(int $key, int $value): bool
```

Метод оновлює запис новим значенням і повертає, чи запис оновлено. Якщо є дублікати ключів, лише перший знайдений елемент набуде оновленого значення. Використовуйте константу **`QuickHashIntHash::CHECK_FOR_DUPES`** під час створення хешу, щоб запобігти попаданню дублюючих ключів у хеш.

### Список параметрів

`key`

Ключ запису, що оновлюється.

`value`

Нове значення запису.

### Значення, що повертаються

Метод возвращает\*\*`true`\*\*, якщо запис було знайдено та оновлено та **`false`**, якщо запис був частиною хеша.

### Приклади

**Пример #1 Пример использования**QuickHashIntHash::update()\*\*\*\*

```php
<?php
$hash = new QuickHashIntHash( 1024 );

var_dump( $hash->add( 141421, 173205 ) );
var_dump( $hash->update( 141421, 223606 ) );
var_dump( $hash->get( 141421 ) );
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
int(223606)
```
