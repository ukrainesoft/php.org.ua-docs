---
navigation:
  - reflectionobject.export.md: '« ReflectionObject::export'
  - reflectionparameter.allowsnull.md: 'ReflectionParameter::allowsNull »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionParameter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionParameter

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**ReflectionParameter** повідомляє інформацію про параметри методів та функцій.

Щоб мати можливість дослідити аргументи функції, спочатку створіть екземпляр класу [ReflectionFunction](class.reflectionfunction.md)либо[ReflectionMethod](class.reflectionmethod.md), а затем используйте его метод[ReflectionFunctionAbstract::getParameters()](reflectionfunctionabstract.getparameters.md)для получения массива аргументов.

## Огляд класів

```classsynopsis

    
     class ReflectionParameter
    

    
     implements
      Reflector {

    /* Свойства */
    
     public
     string
      $name;


    /* Методы */
    
   public __construct(string|array|object $function, int|string $param)

    public allowsNull(): bool
public canBePassedByValue(): bool
private __clone(): void
public static export(string $function, string $parameter, bool $return = ?): string
public getAttributes(?string $name = null, int $flags = 0): array
public getClass(): ?ReflectionClass
public getDeclaringClass(): ?ReflectionClass
public getDeclaringFunction(): ReflectionFunctionAbstract
public getDefaultValue(): mixed
public getDefaultValueConstantName(): ?string
public getName(): string
public getPosition(): int
public getType(): ?ReflectionType
public hasType(): bool
public isArray(): bool
public isCallable(): bool
public isDefaultValueAvailable(): bool
public isDefaultValueConstant(): bool
public isOptional(): bool
public isPassedByReference(): bool
public isVariadic(): bool
public __toString(): string

   }
```

## Властивості

name

Ім'я аргументу. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.md) під час спроби запису.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionParameter::export()](reflectionparameter.export.md)був видалений. |

## Зміст

-   [ReflectionParameter::allowsNull](reflectionparameter.allowsnull.md)— Перевіряє, чи допустиме значення null для параметра
-   [ReflectionParameter::canBePassedByValue](reflectionparameter.canbepassedbyvalue.md)— Перевіряє, чи можна передати цей аргумент за значенням
-   [ReflectionParameter::\_\_clone](reflectionparameter.clone.md) \- Клонувати
-   [ReflectionParameter::\_\_construct](reflectionparameter.construct.md) \- Конструктор
-   [ReflectionParameter::export](reflectionparameter.export.md) \- Експорт
-   [ReflectionParameter::getAttributes](reflectionparameter.getattributes.md)— Отримує атрибути
-   [ReflectionParameter::getClass](reflectionparameter.getclass.md)— Отримує об'єкт ReflectionClass для параметра, що відображається, або null
-   [ReflectionParameter::getDeclaringClass](reflectionparameter.getdeclaringclass.md)— Отримання класу, що оголошує
-   [ReflectionParameter::getDeclaringFunction](reflectionparameter.getdeclaringfunction.md)— Отримання функції, що оголошує
-   [ReflectionParameter::getDefaultValue](reflectionparameter.getdefaultvalue.md)— Отримання стандартного значення для параметра
-   [ReflectionParameter::getDefaultValueConstantName](reflectionparameter.getdefaultvalueconstantname.md)— Повертає ім'я константи за промовчанням, якщо значення за промовчанням константа або null
-   [ReflectionParameter::getName](reflectionparameter.getname.md)— Отримання імені параметра
-   [ReflectionParameter::getPosition](reflectionparameter.getposition.md)— Отримання позиції параметра
-   [ReflectionParameter::getType](reflectionparameter.gettype.md)— Отримати тип параметра
-   [ReflectionParameter::hasType](reflectionparameter.hastype.md)— Перевірити, чи вказано тип параметра
-   [ReflectionParameter::isArray](reflectionparameter.isarray.md)— Перевіряє, чи очікує аргумент масив як значення
-   [ReflectionParameter::isCallable](reflectionparameter.iscallable.md)— Визначити, чи має бути параметр типу callable
-   [ReflectionParameter::isDefaultValueAvailable](reflectionparameter.isdefaultvalueavailable.md)— Перевіряє, чи є значення за замовчуванням
-   [ReflectionParameter::isDefaultValueConstant](reflectionparameter.isdefaultvalueconstant.md)— Визначити, чи значення параметра за промовчанням є константою
-   [ReflectionParameter::isOptional](reflectionparameter.isoptional.md)— Перевіряє, чи аргумент є необов'язковим
-   [ReflectionParameter::isPassedByReference](reflectionparameter.ispassedbyreference.md)— Перевіряє, чи передано параметр за посиланням
-   [ReflectionParameter::isVariadic](reflectionparameter.isvariadic.md)— Перевірити, чи параметр є параметром зі змінною кількістю аргументів
-   [ReflectionParameter::\_\_function toString() { \[native code\] }](reflectionparameter.tostring.md)— Перетворення на рядок
