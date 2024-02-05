---
navigation:
  - book.componere.md: « Componere
  - componere.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

Componere (латинська, англійська: compose) призначений для виробничих оточень і надає API для складання класів, мавпових патчів та приведення.

##### Структура:

[Componere\\Definition](class.componere-definition.md) використовується визначення (або перевизначення) класу під час виконання; Потім клас може бути зареєстрований і у разі перевизначення він замінює вихідний клас доти, доки існує [Componere\\Definition](class.componere-definition.md)

public[Componere\\Definition::\_\_construct](componere-definition.construct.md)(string`$name`) .

public[Componere\\Definition::\_\_construct](componere-definition.construct.md)(string`$name`, string`$parent`) .

public[Componere\\Definition::\_\_construct](componere-definition.construct.md)(string`$name`, array`$interfaces`) .

public[Componere\\Definition::\_\_construct](componere-definition.construct.md)(string`$name`, string`$parent`, array`$interfaces`) .

##### Патчінг:

[Componere\\Patch](class.componere-patch.md) використовується зміни класу конкретного екземпляра об'єкта під час виконання; Після застосування виправлення буде застосовуватися доти, доки існує [Componere\\Patch](class.componere-patch.md) і його можна скасувати.

public[Componere\\Patch::\_\_construct](componere-patch.construct.md)(object`$instance`) .

public[Componere\\Patch::\_\_construct](componere-patch.construct.md)(object`$instance`, array`$interfaces`) .

##### Приведення:

\**Componere\\\** функції приведення можуть наводити серед певних сумісних типів користувачів; У разі сумісності означає, що **Type** є підлеглим або супер типом `object`

```methodsynopsis
Componere\cast(Type $type,  $object): Type
```

```methodsynopsis
Componere\cast_by_ref(Type $type,  $object): Type
```
