---
navigation:
  - class.ds-stack.html: « Стек
  - ds-stack.capacity.html: 'ДсStack::capacity »'
  - index.md: PHP Manual
  - class.ds-stack.html: Стек
title: 'ДсStack::allocate'
---
# ДсStack::allocate

(PECL ds >= 1.0.0)

ДсStack::allocate — Виділяє пам'ять під зазначену місткість

### Опис

```methodsynopsis
public Ds\Stack::allocate(int $capacity): void
```

Гарантує, що виділено достатньо пам'яті під задану місткість (кількість значень). Дозволяє уникнути динамічного перерозподілу пам'яті під час додавання значень.

### Список параметрів

`capacity`

Місткість. Очікувана кількість значень.

> **Зауваження**
> 
> Якщо нове значення місткості менше поточного, воно не зміниться.

### Значення, що повертаються

Функція не повертає значення після виконання.
