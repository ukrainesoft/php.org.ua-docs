---
navigation:
  - reflectionreference.getid.md: '« ReflectionReference::getId'
  - reflectionattribute.construct.md: 'ReflectionAttribute::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionAttribute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionAttribute

(PHP 8)

## Вступ

Класс**ReflectionAttribute**предоставляет информацию об[Атрибути](language.attributes.md)

## Огляд класів

```classsynopsis

    
     class ReflectionAttribute
    

    
     implements
      Reflector {

    /* Константы */
    
     public
     const
     int
      IS_INSTANCEOF;


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

Получение атрибутов с помощью проверки параметра`instanceof`

> **Зауваження** :
> 
> Значення цих констант можуть змінюватись в залежності від версії PHP. Рекомендується завжди використовувати константи і не покладатися на значення прямо.

## Зміст

-   [ReflectionAttribute::\_\_construct](reflectionattribute.construct.md)— Закритий конструктор, який забороняє створення об'єкта безпосередньо
-   [ReflectionAttribute::getArguments](reflectionattribute.getarguments.md)— Повертає аргументи, передані атрибуту
-   [ReflectionAttribute::getName](reflectionattribute.getname.md) \- Повертає ім'я атрибута
-   [ReflectionAttribute::getTarget](reflectionattribute.gettarget.md)— Повертає мету атрибуту у вигляді бітової маски
-   [ReflectionAttribute::isRepeated](reflectionattribute.isrepeated.md)— Визначає, чи атрибут з таким ім'ям був вказаний багаторазово в елементі коду
-   [ReflectionAttribute::newInstance](reflectionattribute.newinstance.md)— Створює екземпляр класу атрибута, використовуючи ім'я класу та аргументи, що містяться в об'єкті ReflectionAttribute.
