---
navigation:
  - class.ds-stack.md: « Ds\\Stack
  - ds-stack.capacity.md: 'Ds\\Stack::capacity »'
  - index.md: PHP Manual
  - class.ds-stack.md: Ds\\Stack
title: 'Ds\\Stack::allocate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ds\\Stack::allocate

(PECL ds >= 1.0.0)

Ds\\Stack::allocate — Виділяє пам'ять під зазначену місткість

### Опис

```methodsynopsis
public Ds\Stack::allocate(int $capacity): void
```

Гарантує, що виділено достатньо пам'яті під задану місткість (кількість значень). Дозволяє уникнути динамічного перерозподілу пам'яті під час додавання значень.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження** :
> 
> Якщо нове значення місткості менше поточного, воно не зміниться.

### Значення, що повертаються

Функція не повертає значення після виконання.
