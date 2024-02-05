---
navigation:
  - reflectionfunction.tostring.md: '« ReflectionFunction::\_\_function toString() { [native code] }'
  - reflectionfunctionabstract.clone.md: 'ReflectionFunctionAbstract::\_\_clone »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionFunctionAbstract
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionFunctionAbstract

(PHP 5 >= 5.2.0, PHP 7, PHP 8)

## Вступ

Є батьківським класом для [ReflectionFunction](class.reflectionfunction.md)Детальнішу інформацію дивіться в описі цього дочірнього класу.

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
public isStatic(): bool
public isUserDefined(): bool
public isVariadic(): bool
public returnsReference(): bool
abstract public __toString(): void

   }
```

## Властивості

name

Ім'я функції. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.md) під час спроби запису.

## Зміст

-   [ReflectionFunctionAbstract::\_\_clone](reflectionfunctionabstract.clone.md) \- Клонує функцію
-   [ReflectionFunctionAbstract::getAttributes](reflectionfunctionabstract.getattributes.md)— Отримує атрибути
-   [ReflectionFunctionAbstract::getClosureScopeClass](reflectionfunctionabstract.getclosurescopeclass.md)— Повертає клас, в рамках якого було оголошено замикання
-   [ReflectionFunctionAbstract::getClosureThis](reflectionfunctionabstract.getclosurethis.md)— Повертає покажчик, прив'язаний до замикання
-   [ReflectionFunctionAbstract::getClosureUsedVariables](reflectionfunctionabstract.getclosureusedvariables.md)— Повертає масив змінних, що використовуються в замиканні.
-   [ReflectionFunctionAbstract::getDocComment](reflectionfunctionabstract.getdoccomment.md)— Отримує doc-коментар
-   [ReflectionFunctionAbstract::getEndLine](reflectionfunctionabstract.getendline.md)— Отримує номер рядка завершення опису функції
-   [ReflectionFunctionAbstract::getExtension](reflectionfunctionabstract.getextension.md)— Отримує інформацію про модуль
-   [ReflectionFunctionAbstract::getExtensionName](reflectionfunctionabstract.getextensionname.md)— Отримання імені модуля
-   [ReflectionFunctionAbstract::getFileName](reflectionfunctionabstract.getfilename.md)— Отримує ім'я файлу
-   [ReflectionFunctionAbstract::getName](reflectionfunctionabstract.getname.md)— Отримує ім'я функції
-   [ReflectionFunctionAbstract::getNamespaceName](reflectionfunctionabstract.getnamespacename.md)— Отримання імені простору імен
-   [ReflectionFunctionAbstract::getNumberOfParameters](reflectionfunctionabstract.getnumberofparameters.md)— Отримує кількість параметрів
-   [ReflectionFunctionAbstract::getNumberOfRequiredParameters](reflectionfunctionabstract.getnumberofrequiredparameters.md)— Отримує кількість обов'язкових параметрів
-   [ReflectionFunctionAbstract::getParameters](reflectionfunctionabstract.getparameters.md)— Отримує параметри
-   [ReflectionFunctionAbstract::getReturnType](reflectionfunctionabstract.getreturntype.md)— Отримує оголошений тип значення, що повертається функцією значення
-   [ReflectionFunctionAbstract::getShortName](reflectionfunctionabstract.getshortname.md)— Отримує коротке ім'я функції
-   [ReflectionFunctionAbstract::getStartLine](reflectionfunctionabstract.getstartline.md)— Отримує початковий номер рядка
-   [ReflectionFunctionAbstract::getStaticVariables](reflectionfunctionabstract.getstaticvariables.md)— Отримує статичні змінні
-   [ReflectionFunctionAbstract::getTentativeReturnType](reflectionfunctionabstract.gettentativereturntype.md)— Повертає попередній тип значення, що повертається, пов'язаний з функцією
-   [ReflectionFunctionAbstract::hasReturnType](reflectionfunctionabstract.hasreturntype.md)— Перевіряє, чи має функція оголошений тип значення, що повертається
-   [ReflectionFunctionAbstract::hasTentativeReturnType](reflectionfunctionabstract.hastentativereturntype.md)— Визначає, чи має функція попередній тип значення, що повертається.
-   [ReflectionFunctionAbstract::inNamespace](reflectionfunctionabstract.innamespace.md)— Перевіряє, чи є функція у просторі імен
-   [ReflectionFunctionAbstract::isClosure](reflectionfunctionabstract.isclosure.md) \- Перевіряє, чи є функція замиканням (Closure)
-   [ReflectionFunctionAbstract::isDeprecated](reflectionfunctionabstract.isdeprecated.md)— Перевіряє, чи є функція застарілої
-   [ReflectionFunctionAbstract::isGenerator](reflectionfunctionabstract.isgenerator.md)— Перевіряє, чи функція є генератором
-   [ReflectionFunctionAbstract::isInternal](reflectionfunctionabstract.isinternal.md)— Перевіряє, чи функція є внутрішньою
-   [ReflectionFunctionAbstract::isStatic](reflectiofunctionabstract.isstatic.md)— Перевіряє, чи є статична функція
-   [ReflectionFunctionAbstract::isUserDefined](reflectionfunctionabstract.isuserdefined.md)— Перевіряє, чи функція є певною користувачем
-   [ReflectionFunctionAbstract::isVariadic](reflectionfunctionabstract.isvariadic.md)— Перевіряє, чи є функція зі змінною кількістю аргументів
-   [ReflectionFunctionAbstract::returnsReference](reflectionfunctionabstract.returnsreference.md) \- Перевіряє, що функція повертає посилання
-   [ReflectionFunctionAbstract::\_\_function toString() { \[native code\] }](reflectionfunctionabstract.tostring.md)— Повертає рядкову виставу об'єкта ReflectionFunctionAbstract
