---
navigation:
  - ev.suspend.md: '« Ev::suspend'
  - ev.verify.md: 'Ev::verify »'
  - index.md: PHP Manual
  - class.ev.md: Ev
title: 'Ev::time'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Ev::time

(PECL ev >= 0.2.0)

Ev::time — Повертає поточний час у секундах (дрібне число) минуле з початку епохи Unix

### Опис

```methodsynopsis
final
   public
   static
   Ev::time(): float
```

Повертає поточний час у секундах (дрібне число) минуле з початку епохи Unix. Але краще, все ж таки, використовуйте [Ev::now()](ev.now.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний час у секундах (дрібне число) минуле з початку епохи Unix.

### Дивіться також

-   [Ev::now()](ev.now.md) \- Отримати час запуску останньої ітерації циклу за замовчуванням
