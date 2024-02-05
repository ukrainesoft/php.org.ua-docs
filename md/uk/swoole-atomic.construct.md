---
navigation:
  - swoole-atomic.cmpset.md: '« Swoole\\Atomic::cmpset'
  - swoole-atomic.get.md: 'Swoole\\Atomic::get »'
  - index.md: PHP Manual
  - class.swoole-atomic.md: Swoole\\Atomic
title: 'Swoole\\Atomic::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Atomic::\_\_construct

(PECL swoole >= 1.9.0)

Swoole\\Atomic::\_\_construct — Створює атомарний об'єкт swoole

### Опис

public **Swoole\\Atomic::\_\_construct**(int`$value`

Атомарний об'єкт Swoole - це ціла змінна, яка дозволяє будь-якому процесору атомарно тестувати і модифікувати. Він реалізований з урахуванням атомарних інструкцій процесора. Атомарні змінні Swoole мають бути визначені до swoole\_server->start.

Порівняння та заміна (CAS) - це атомарна інструкція, яка використовується в багатопоточності для досягнення синхронізації. Вона порівнює вміст області пам'яті із заданим значенням і, тільки якщо вони збігаються, змінює вміст цієї області пам'яті на нове значення.

### Список параметрів

`value`

Значення атомарного об'єкта.
