---
navigation:
  - phar.copy.md: '« Phar::copy'
  - phar.createdefaultstub.md: 'Phar::createDefaultStub »'
  - index.md: PHP Manual
  - class.phar.md: Phar
title: 'Phar::count'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Phar::count

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::count — Повертає кількість записів (файлів) у Phar-архіві

### Опис

```methodsynopsis
public Phar::count(int $mode = COUNT_NORMAL): int
```

### Список параметрів

`mode`

Параметр`mode` - ціле значення, що визначає режим підрахунку, що використовується. За замовчуванням встановлено значення **`COUNT_NORMAL`**, підраховуються лише елементи в архіві, які були видалені чи приховані. Якщо встановлено значення **`COUNT_RECURSIVE`**, підраховуються всі елементи в архіві, включаючи віддалені чи приховані.

### Значення, що повертаються

Кількість файлів, що містяться в цьому phar-архіві, або (число нуль), якщо архів порожній.

### Приклади

**Приклад #1 Приклад використання** Phar::count()\*\*\*\*

```php
<?php
// убедитесь, что архив не существует
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
} catch (Exception $e) {
    echo 'Не удалось создать phar:', $e;
}
echo 'Новый phar содержит ' . $p->count() . " записей\n";
$p['file.txt'] = 'привет';
echo 'Новый phar содержит ' . $p->count() . " записей\n";
?>
```

Результат виконання наведеного прикладу:

```
Новый phar содержит 0 записей
Новый phar содержит 1 записей
```
