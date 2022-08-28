Клас ReflectionFunctionAbstract

-   [« ReflectionFunction::\_\_toString](reflectionfunction.tostring.html)
    
-   [ReflectionFunctionAbstract::\_\_clone »](reflectionfunctionabstract.clone.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionFunctionAbstract
    

# Клас ReflectionFunctionAbstract

(PHP 5> = 5.2.0, PHP 7, PHP 8)

## Вступ

Є батьківським класом для [ReflectionFunction](class.reflectionfunction.html)Детальнішу інформацію дивіться в описі цього дочірнього класу.

## Огляд класів

```classsynopsis

     
    

    
     
      abstract
      class ReflectionFunctionAbstract
     

     implements 
       Reflector {

    /* Свойства */
    
     public
     string
      $name;


    /* Методы */
    
   private __clone(): void
public getAttributes(?string $name = null, int $flags = 0): array
public getClosureScopeClass(): ?ReflectionClass
public getClosureThis(): ?object
public getClosureUsedVariables(): array
public getDocComment(): string|false
public getEndLine(): int|false
public getExtension(): ?ReflectionExtension
public getExtensionName(): string|false
public getFileName(): string|false
public getName(): string
public getNamespaceName(): string
public getNumberOfParameters(): int
public getNumberOfRequiredParameters(): int
public getParameters(): array
public getReturnType(): ?ReflectionType
public getShortName(): string
public getStartLine(): int|false
public getStaticVariables(): array
public getTentativeReturnType(): ?ReflectionType
public hasReturnType(): bool
public hasTentativeReturnType(): bool
public inNamespace(): bool
public isClosure(): bool
public isDeprecated(): bool
public isGenerator(): bool
public isInternal(): bool
public isUserDefined(): bool
public isVariadic(): bool
public returnsReference(): bool
abstract public __toString(): void

   }
```

## Властивості

name

Ім'я функції. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.html) під час спроби запису.

## Зміст

-   [ReflectionFunctionAbstract::\_\_clone](reflectionfunctionabstract.clone.html) - Клонує функцію
-   [ReflectionFunctionAbstract::getAttributes](reflectionfunctionabstract.getattributes.html) — Отримує атрибути
-   [ReflectionFunctionAbstract::getClosureScopeClass](reflectionfunctionabstract.getclosurescopeclass.html) — Повертає клас, в рамках якого було оголошено замикання
-   [ReflectionFunctionAbstract::getClosureThis](reflectionfunctionabstract.getclosurethis.html) — Повертає покажчик, прив'язаний до замикання
-   [ReflectionFunctionAbstract::getClosureUsedVariables](reflectionfunctionabstract.getclosureusedvariables.html) — Повертає масив змінних, що використовуються в замиканні.
-   [ReflectionFunctionAbstract::getDocComment](reflectionfunctionabstract.getdoccomment.html) — Отримує doc-коментар
-   [ReflectionFunctionAbstract::getEndLine](reflectionfunctionabstract.getendline.html) — Отримує номер рядка завершення опису функції
-   [ReflectionFunctionAbstract::getExtension](reflectionfunctionabstract.getextension.html) — Отримує інформацію про модуль
-   [ReflectionFunctionAbstract::getExtensionName](reflectionfunctionabstract.getextensionname.html) — Отримання імені модуля
-   [ReflectionFunctionAbstract::getFileName](reflectionfunctionabstract.getfilename.html) — Отримує ім'я файлу
-   [ReflectionFunctionAbstract::getName](reflectionfunctionabstract.getname.html) — Отримує ім'я функції
-   [ReflectionFunctionAbstract::getNamespaceName](reflectionfunctionabstract.getnamespacename.html) — Отримання імені простору імен
-   [ReflectionFunctionAbstract::getNumberOfParameters](reflectionfunctionabstract.getnumberofparameters.html) — Отримує кількість параметрів
-   [ReflectionFunctionAbstract::getNumberOfRequiredParameters](reflectionfunctionabstract.getnumberofrequiredparameters.html) — Отримує кількість обов'язкових параметрів
-   [ReflectionFunctionAbstract::getParameters](reflectionfunctionabstract.getparameters.html) — Отримує параметри
-   [ReflectionFunctionAbstract::getReturnType](reflectionfunctionabstract.getreturntype.html) — Отримує оголошений тип значення, що повертається функцією значення
-   [ReflectionFunctionAbstract::getShortName](reflectionfunctionabstract.getshortname.html) — Отримує коротке ім'я функції
-   [ReflectionFunctionAbstract::getStartLine](reflectionfunctionabstract.getstartline.html) — Отримує початковий номер рядка
-   [ReflectionFunctionAbstract::getStaticVariables](reflectionfunctionabstract.getstaticvariables.html) — Отримує статичні змінні
-   [ReflectionFunctionAbstract::getTentativeReturnType](reflectionfunctionabstract.gettentativereturntype.html) — Повертає попередній тип значення, що повертається, пов'язаний з функцією
-   [ReflectionFunctionAbstract::hasReturnType](reflectionfunctionabstract.hasreturntype.html) — Перевіряє, чи має функція оголошений тип значення, що повертається
-   [ReflectionFunctionAbstract::hasTentativeReturnType](reflectionfunctionabstract.hastentativereturntype.html) — Визначає, чи має функція попередній тип значення, що повертається.
-   [ReflectionFunctionAbstract::inNamespace](reflectionfunctionabstract.innamespace.html) — Перевіряє, чи є функція у просторі імен
-   [ReflectionFunctionAbstract::isClosure](reflectionfunctionabstract.isclosure.html) - Перевіряє, чи є функція замиканням (Closure)
-   [ReflectionFunctionAbstract::isDeprecated](reflectionfunctionabstract.isdeprecated.html) — Перевіряє, чи є функція застарілої
-   [ReflectionFunctionAbstract::isGenerator](reflectionfunctionabstract.isgenerator.html) — Перевіряє, чи функція є генератором
-   [ReflectionFunctionAbstract::isInternal](reflectionfunctionabstract.isinternal.html) — Перевіряє, чи функція є внутрішньою
-   [ReflectionFunctionAbstract::isUserDefined](reflectionfunctionabstract.isuserdefined.html) — Перевіряє, чи функція є певною користувачем
-   [ReflectionFunctionAbstract::isVariadic](reflectionfunctionabstract.isvariadic.html) — Перевіряє, чи є функція зі змінною кількістю аргументів
-   [ReflectionFunctionAbstract::returnsReference](reflectionfunctionabstract.returnsreference.html) - Перевіряє, що функція повертає посилання
-   [ReflectionFunctionAbstract::\_\_toString](reflectionfunctionabstract.tostring.html) — Перетворення на рядок