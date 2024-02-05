---
navigation:
  - hash.constants.md: « Зумовлені константи
  - hashcontext.construct.md: 'HashContext::\_\_construct »'
  - index.md: PHP Manual
  - book.hash.md: Hash
title: Клас HashContext
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас HashContext

(PHP 7 >= 7.2.0, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

    
     final
     class HashContext
     {

    /* Методы */
    
   private __construct()

    public __serialize(): array
public __unserialize(array $data): void

   }
```

## Зміст

-   [HashContext::\_\_construct](hashcontext.construct.md)— Закритий конструктор для заборони безпосереднього створення об'єкту
-   [HashContext::\_\_serialize](hashcontext.serialize.md)— Серіалізує об'єкт HashContext
-   [HashContext::\_\_unserialize](hashcontext.unserialize.md)— Десеріалізує параметр data в об'єкті HashContext
