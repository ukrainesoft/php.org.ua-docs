Клас ReflectionAttribute

-   [« ReflectionReference::getId](reflectionreference.getid.html)
    
-   [ReflectionAttribute::construct »](reflectionattribute.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionAttribute
    

# Клас ReflectionAttribute

(PHP 8)

## Вступ

Клас **ReflectionAttribute** надає інформацію про [Атрибутах](language.attributes.html)

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

-   [ReflectionAttribute::construct](reflectionattribute.construct.html) — Закритий конструктор, який забороняє створення об'єкта безпосередньо
-   [ReflectionAttribute::getArguments](reflectionattribute.getarguments.html) — Повертає аргументи, передані атрибуту
-   [ReflectionAttribute::getName](reflectionattribute.getname.html) - Повертає ім'я атрибута
-   [ReflectionAttribute::getTarget](reflectionattribute.gettarget.html) — Повертає мету атрибуту у вигляді бітової маски
-   [ReflectionAttribute::isRepeated](reflectionattribute.isrepeated.html) — Перевіряє, чи атрибут може вказуватися багаторазово в елементі коду
-   [ReflectionAttribute::newInstance](reflectionattribute.newinstance.html) — Створює екземпляр класу атрибута, представленого цим класом ReflectionAttribute та аргументами