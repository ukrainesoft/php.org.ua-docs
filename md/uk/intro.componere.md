Вступ

-   [« Componere](book.componere.html)
    
-   [Установка и настройка »](componere.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Componere](book.componere.html)
    
-   Вступ
    

# Вступ

Componere (латинська, англійська: compose) призначений для виробничих оточень і надає API для складання класів, мавпових патчів та приведення.

##### Структура:

[Componere\\Definition](class.componere-definition.html) використовується визначення (або перевизначення) класу під час виконання; Потім клас може бути зареєстрований і у разі перевизначення він замінює вихідний клас доти, доки існує [Componere\\Definition](class.componere-definition.html)

public [Componere\\Definition::\_\_construct](componere-definition.construct.html)(string `$name`

public [Componere\\Definition::\_\_construct](componere-definition.construct.html)(string `$name`, string `$parent`

public [Componere\\Definition::\_\_construct](componere-definition.construct.html)(string `$name`, array `$interfaces`

public [Componere\\Definition::\_\_construct](componere-definition.construct.html)(string `$name`, string `$parent`, array `$interfaces`

##### Патчінг:

[Componere\\Patch](class.componere-patch.html) використовується зміни класу конкретного екземпляра об'єкта під час виконання; Після застосування виправлення буде застосовуватися доти, доки існує [Componere\\Patch](class.componere-patch.html) і його можна скасувати.

public [Componere\\Patch::\_\_construct](componere-patch.construct.html)(object `$instance`

public [Componere\\Patch::\_\_construct](componere-patch.construct.html)(object `$instance`, array `$interfaces`

##### Приведення:

*Componere* функції приведення можуть наводити серед певних сумісних типів користувачів; У разі сумісності означає, що **Type** є підлеглим або супер типом `object`

```methodsynopsis
Componere\cast(Type $type,  $object): Type
```

```methodsynopsis
Componere\cast_by_ref(Type $type,  $object): Type
```