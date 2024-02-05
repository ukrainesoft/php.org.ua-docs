---
navigation:
  - class.ds-deque.md: « Ds\\Deque
  - ds-deque.apply.md: 'Ds\\Deque::apply »'
  - index.md: PHP Manual
  - class.ds-deque.md: Ds\\Deque
title: 'Ds\\Deque::allocate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Deque::allocate

(PECL ds >= 1.0.0)

Ds\\Deque::allocate — Виділяє пам'ять під зазначену місткість

### Опис

```methodsynopsis
public Ds\Deque::allocate(int $capacity): void
```

Гарантує, що виділено достатньо пам'яті під задану місткість (кількість значень). Дозволяє уникнути динамічного перерозподілу пам'яті під час додавання значень.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження** :
> 
> Якщо нове значення місткості менше поточного, вона не зміниться.

> **Зауваження** :
> 
> Значення місткості округляється до найближчого ступеня двійки (тобто 8, 16, 32, 64, 128 і т.д.)

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Пример #1 Пример использования**Ds\\Deque::allocate()\*\*\*\*

```php
<?php
$deque = new \Ds\Deque();
var_dump($deque->capacity());

$deque->allocate(100);
var_dump($deque->capacity());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(8)
int(128)
```
