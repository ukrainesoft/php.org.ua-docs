---
navigation:
  - com.construct.md: '« com::construct'
  - dotnet.construct.md: 'dotnet::construct »'
  - index.md: PHP Manual
  - book.com.md: COM
title: Клас dotnet
---
# Клас dotnet

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

## Вступ

Клас dotnet дозволяє створювати об'єкти зі збірок .Net, викликати їх методи та використовувати їх властивості, якщо клас, методи та властивості [» видимі для COM](https://docs.microsoft.com/dotnet/api/system.runtime.interopservices.comvisibleattribute)

Ні створення екземплярів статичних класів, ні виклик статичних методів не підтримуються. Створення екземплярів універсальних класів, таких як `System.Collections.Generic.List`, також не підтримується.

Деякі класи в .Net не реалізують IDispatch, тому хоча їх об'єкти можна створювати, виклик методів або доступ до властивостей цих класів не підтримується.

> **Зауваження**
> 
> Вам потрібно встановити бібліотеки часу виконання .Net на ваш веб-сервер, щоб скористатися цією функцією.

> **Зауваження**
> 
> До PHP 8.0.0 .Net framework 4.0 і пізніші версії не підтримуються класом **dotnet**. Однак якщо збірки були зареєстровані за допомогою **regasm.exe**, класи можуть бути створені як об'єкти [com](class.com.md). Починаючи з PHP 8.0.0, .Net framework 4.0 та пізніші версії підтримуються за допомогою директиви php.ini [com.dotnetversion](com.configuration.md#ini.com.dotnet-version)

## Огляд класів

```synopsis

     
    

    
     
      class dotnet
     

    
     extends
      variant
    

     {

    /* Методы */
    
   public __construct(string $assembly_name, string $datatype_name, int $codepage = CP_ACP)

   }
```

## Перевантажені методи

Об'єкт, що повертається, є перевантаженим, тобто PHP не бачить будь-яких фіксованих методів, як це відбувається зі звичайними класами; натомість властивості та доступ до методів передається через COM, а звідти в DOTNET. Іншими словами, об'єкт .Net відображається через рівень взаємодії COM, який надається бібліотекою часу виконання .Net.

Як тільки ви створили об'єкт dotnet, PHP обробляє його ідентично до будь-якого іншого об'єкта COM; застосовуються ті самі правила.

## Приклади dotnet

**Приклад #1 Приклад використання dotnet**

```php
<?php
$stack = new dotnet("mscorlib", "System.Collections.Stack");
$stack->Push(".Net");
$stack->Push("Привет ");
echo $stack->Pop() . $stack->Pop();
?>
```

## Зміст

-   [dotnet::construct](dotnet.construct.md) - Конструктор класу dotnet
