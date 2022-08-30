Створює атомарний об'єкт swoole

-   [« SwooleAtomic::cmpset](swoole-atomic.cmpset.html)
    
-   [SwooleAtomic::get »](swoole-atomic.get.html)
    
-   [PHP Manual](index.md)
    
-   [SwooleAtomic](class.swoole-atomic.html)
    
-   Створює атомарний об'єкт swoole
    

# SwooleAtomic::construct

(PECL swoole >= 1.9.0)

SwooleAtomic::construct — Створює атомарний об'єкт swoole

### Опис

public **SwooleAtomic::construct**(int `$value`

Атомарний об'єкт Swoole - це ціла змінна, яка дозволяє будь-якому процесору атомарно тестувати і модифікувати. Він реалізований з урахуванням атомарних інструкцій процесора. Атомарні змінні Swoole мають бути визначені до swooleserver->start.

Порівняння та заміна (CAS) - це атомарна інструкція, яка використовується в багатопоточності для досягнення синхронізації. Вона порівнює вміст області пам'яті із заданим значенням і, тільки якщо вони збігаються, змінює вміст цієї області пам'яті на нове значення.

### Список параметрів

`value`

Значення атомарного об'єкта.