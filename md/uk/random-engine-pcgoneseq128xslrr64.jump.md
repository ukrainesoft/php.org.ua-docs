---
navigation:
  - random-engine-pcgoneseq128xslrr64.generate.md: '« Random\\Engine\\PcgOneseq128XslRr64::generate'
  - random-engine-pcgoneseq128xslrr64.serialize.md: 'Random\\Engine\\PcgOneseq128XslRr64::\_\_serialize »'
  - index.md: PHP Manual
  - class.random-engine-pcgoneseq128xslrr64.md: Random\\Engine\\PcgOneseq128XslRr64
title: 'Random\\Engine\\PcgOneseq128XslRr64::jump'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Random\\Engine\\PcgOneseq128XslRr64::jump

(PHP 8 >= 8.2.0)

Random\\Engine\\PcgOneseq128XslRr64::jump — Ефективне переміщення двигуна вперед на кілька кроків

### Опис

```methodsynopsis
public Random\Engine\PcgOneseq128XslRr64::jump(int $advance): void
```

Переміщує стан алгоритму вперед на кількість кроків, задану параметром `advance`ніби функція [Random\\Engine\\PcgOneseq128XslRr64::generate()](random-engine-pcgoneseq128xslrr64.generate.md) була викликана стільки разів.

### Список параметрів

`advance`

Кількість кроків просування вперед; повинно бути или больше.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

-   Якщо параметр `advance`меньше , буде викинуто виняток [ValueError](class.valueerror.md)

### Приклади

**Приклад #1 Приклад використання** Random\\Engine\\PcgOneseq128XslRr64::jump()\*\*\*\*

```php
<?php
$a = new \Random\Engine\PcgOneseq128XslRr64(0);
$b = clone $a;

for ($i = 0; $i < 1_000; $i++) {
    $a->generate();
}
$b->jump(1_000);

echo "A: ", bin2hex($a->generate()), "\n";
echo "B: ", bin2hex($b->generate()), "\n";
?>
```

Результат виконання наведеного прикладу:

```
A: e6d0d5813913a424
B: e6d0d5813913a424
```

**Приклад #2 Методи Randomizer можуть викликати двигун більше одного разу**

```php
<?php
$a = new \Random\Randomizer(new \Random\Engine\PcgOneseq128XslRr64(42659));
$b = new \Random\Randomizer(clone $a->engine);

$a->getInt(1, 1572864); // Выполняет два вызова generate().
$a->getInt(1, 1572864);

$b->engine->jump(2);

// Потому что первый вызов ->getInt() вызвал ->generate() дважды
// движки не совпадают после выполнения ->jump(2).
echo "A: ", bin2hex($a->engine->generate()), "\n";
echo "B: ", bin2hex($b->engine->generate()), "\n";

// Теперь движок B соответствует движку A.
echo "B: ", bin2hex($b->engine->generate()), "\n";
?>
```

Результат виконання наведеного прикладу:

```
A: 1e9f3107d56653d0
B: a156c0086dd79d44
B: 1e9f3107d56653d0
```
