---
navigation:
  - quickhashinthash.delete.md: '« QuickHashIntHash::delete'
  - quickhashinthash.get.md: 'QuickHashIntHash::get »'
  - index.md: PHP Manual
  - class.quickhashinthash.md: QuickHashIntHash
title: 'QuickHashIntHash::exists'
---
# QuickHashIntHash::exists

(PECL quickhash >= Unknown)

QuickHashIntHash::exists — Метод перевіряє, чи є ключ частиною хеша

### Опис

```methodsynopsis
public QuickHashIntHash::exists(int $key): bool
```

Метод перевіряє, чи існує у хеші запис із зазначеним ключем.

### Список параметрів

`key`

Ключ запису для перевірки її існування у хеші.

### Значення, що повертаються

Метод повертає **`true`**, якщо запис було знайдено або **`false`**, якщо запис не було знайдено.

### Приклади

**Приклад #1 Приклад використання **QuickHashIntHash::exists()****

```php
<?php
// Генерация 200000 элементов
$array = range( 0, 199999 );
$existingEntries = array_rand( array_flip( $array ), 180000 );
$testForEntries = array_rand( array_flip( $array ), 1000 );
$foundCount = 0;

echo "Создание хеша: ", microtime( true ), "\n";
$hash = new QuickHashIntHash( 100000 );
echo "Добавление элементов: ", microtime( true ), "\n";
foreach( $existingEntries as $key )
{
     $hash->add( $key, 56 );
}

echo "Запуск 1000 тестов: ", microtime( true ), "\n";
foreach( $testForEntries as $key )
{
     $foundCount += $hash->exists( $key );
}
echo "Готово, $foundCount найдено: ", microtime( true ), "\n";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Создание хеша: 1263588703.0748
Добавление элементов: 1263588703.0757
Запуск 1000 тестов: 1263588703.7851
Готово, 898 найдено: 1263588703.7897
```
