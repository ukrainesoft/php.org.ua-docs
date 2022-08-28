Клас ReflectionParameter

-   [« ReflectionObject::export](reflectionobject.export.html)
    
-   [ReflectionParameter::allowsNull »](reflectionparameter.allowsnull.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionParameter
    

# Клас ReflectionParameter

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **ReflectionParameter** повідомляє інформацію про параметри методів та функцій.

Щоб мати можливість дослідити аргументи функції, спочатку створіть екземпляр класу [ReflectionFunction](class.reflectionfunction.html) або [ReflectionMethod](class.reflectionmethod.html), а потім використовуйте його метод [ReflectionFunctionAbstract::getParameters()](reflectionfunctionabstract.getparameters.html) для одержання масиву аргументів.

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

Ім'я аргументу. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.html) під час спроби запису.

## Зміст

-   [ReflectionParameter::allowsNull](reflectionparameter.allowsnull.html) — Перевіряє, чи допустиме значення null для параметра
-   [ReflectionParameter::canBePassedByValue](reflectionparameter.canbepassedbyvalue.html) — Перевіряє, чи можна передати цей аргумент за значенням
-   [ReflectionParameter::\_\_clone](reflectionparameter.clone.html) - Клонувати
-   [ReflectionParameter::\_\_construct](reflectionparameter.construct.html) - Конструктор
-   [ReflectionParameter::export](reflectionparameter.export.html) - Експорт
-   [ReflectionParameter::getAttributes](reflectionparameter.getattributes.html) — Отримує атрибути
-   [ReflectionParameter::getClass](reflectionparameter.getclass.html) — Отримує об'єкт ReflectionClass для параметра, що відображається, або null
-   [ReflectionParameter::getDeclaringClass](reflectionparameter.getdeclaringclass.html) — Отримання класу, що оголошує
-   [ReflectionParameter::getDeclaringFunction](reflectionparameter.getdeclaringfunction.html) — Отримання функції, що оголошує
-   [ReflectionParameter::getDefaultValue](reflectionparameter.getdefaultvalue.html) — Отримання стандартного значення для параметра
-   [ReflectionParameter::getDefaultValueConstantName](reflectionparameter.getdefaultvalueconstantname.html) — Повертає ім'я константи за промовчанням, якщо значення за промовчанням константа або null
-   [ReflectionParameter::getName](reflectionparameter.getname.html) — Отримання імені параметра
-   [ReflectionParameter::getPosition](reflectionparameter.getposition.html) — Отримання позиції параметра
-   [ReflectionParameter::getType](reflectionparameter.gettype.html) — Отримати тип параметра
-   [ReflectionParameter::hasType](reflectionparameter.hastype.html) — Перевірити, чи вказано тип параметра
-   [ReflectionParameter::isArray](reflectionparameter.isarray.html) — Перевіряє, чи очікує аргумент масив як значення
-   [ReflectionParameter::isCallable](reflectionparameter.iscallable.html) — Визначити, чи параметр має бути типу callable
-   [ReflectionParameter::isDefaultValueAvailable](reflectionparameter.isdefaultvalueavailable.html) — Перевіряє, чи є значення за замовчуванням
-   [ReflectionParameter::isDefaultValueConstant](reflectionparameter.isdefaultvalueconstant.html) — Визначити, чи значення параметра за промовчанням є константою
-   [ReflectionParameter::isOptional](reflectionparameter.isoptional.html) — Перевіряє, чи аргумент є необов'язковим
-   [ReflectionParameter::isPassedByReference](reflectionparameter.ispassedbyreference.html) — Перевіряє, чи передано параметр за посиланням
-   [ReflectionParameter::isVariadic](reflectionparameter.isvariadic.html) — Перевірити, чи параметр є параметром зі змінною кількістю аргументів
-   [ReflectionParameter::\_\_toString](reflectionparameter.tostring.html) — Перетворення на рядок