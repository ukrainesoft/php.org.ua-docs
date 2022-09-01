---
navigation:
  - book.componere.md: « Componere
  - componere.setup.md: Встановлення та налаштування »
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Вступ
---
# Вступ

Componere (латинська, англійська: compose) призначений для виробничих оточень і надає API для складання класів, мавпових патчів та приведення.

##### Структура:

[ComponereDefinition](class.componere-definition.html) використовується визначення (або перевизначення) класу під час виконання; Потім клас може бути зареєстрований і у разі перевизначення він замінює вихідний клас доти, доки існує [ComponereDefinition](class.componere-definition.html)

public [ComponereDefinition::construct](componere-definition.construct.html)(string `$name`

public [ComponereDefinition::construct](componere-definition.construct.html)(string `$name`, string `$parent`

public [ComponereDefinition::construct](componere-definition.construct.html)(string `$name`, array `$interfaces`

public [ComponereDefinition::construct](componere-definition.construct.html)(string `$name`, string `$parent`, array `$interfaces`

##### Патчінг:

[ComponerePatch](class.componere-patch.html) використовується зміни класу конкретного екземпляра об'єкта під час виконання; Після застосування виправлення буде застосовуватися доти, доки існує [ComponerePatch](class.componere-patch.html) і його можна скасувати.

public [ComponerePatch::construct](componere-patch.construct.html)(object `$instance`

public [ComponerePatch::construct](componere-patch.construct.html)(object `$instance`, array `$interfaces`

##### Приведення:

*Componere* функції приведення можуть наводити серед певних сумісних типів користувачів; У разі сумісності означає, що **Type** є підлеглим або супер типом `object`

```methodsynopsis
Componere\cast(Type $type,  $object): Type
```

```methodsynopsis
Componere\cast_by_ref(Type $type,  $object): Type
```
