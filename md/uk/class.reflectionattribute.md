Клас ReflectionAttribute

-   [« ReflectionReference::getId](reflectionreference.getid.md)
    
-   [ReflectionAttribute::construct »](reflectionattribute.construct.md)
    
-   [PHP Manual](index.md)
    
-   [Reflection](book.reflection.md)
    
-   Клас ReflectionAttribute
    

# Клас ReflectionAttribute

(PHP 8)

## Вступ

Клас **ReflectionAttribute** надає інформацію про [Атрибутах](language.attributes.md)

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionAttribute
     

     implements 
       Reflector {

    /* Константы */
    
     const
     int
      IS_INSTANCEOF = 2;


    /* Методы */
    
   private __construct()

    public getArguments(): array
public getName(): string
public getTarget(): int
public isRepeated(): bool
public newInstance(): object

   }
```

## Обумовлені константи

## Прапори ReflectionAttribute

**`ReflectionAttribute::IS_INSTANCEOF`**

Отримання атрибутів за допомогою перевірки параметра `instanceof`

> **Зауваження**
> 
> Значення цих констант можуть змінюватись в залежності від версії PHP. Рекомендується завжди використовувати константи і не покладатися на значення прямо.

## Зміст

-   [ReflectionAttribute::construct](reflectionattribute.construct.md) — Закритий конструктор, який забороняє створення об'єкта безпосередньо
-   [ReflectionAttribute::getArguments](reflectionattribute.getarguments.md) — Повертає аргументи, передані атрибуту
-   [ReflectionAttribute::getName](reflectionattribute.getname.md) - Повертає ім'я атрибута
-   [ReflectionAttribute::getTarget](reflectionattribute.gettarget.md) — Повертає мету атрибуту у вигляді бітової маски
-   [ReflectionAttribute::isRepeated](reflectionattribute.isrepeated.md) — Перевіряє, чи атрибут може вказуватися багаторазово в елементі коду
-   [ReflectionAttribute::newInstance](reflectionattribute.newinstance.md) — Створює екземпляр класу атрибута, представленого цим класом ReflectionAttribute та аргументами