---
navigation:
  - ds-map.xor.md: '« Ds\\Map::xor'
  - ds-pair.clear.md: 'Ds\\Pair::clear »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Pair
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Pair

(PECL ds >= 1.0.0)

## Вступ

Пара використовується класом [Ds\\Map](class.ds-map.md)для хранения пар ключ-значение.

## Огляд класів

```classsynopsis


    
    
     
      class Ds\Pair
     

     implements 
       JsonSerializable {
    

    /* Методы */
     
   public __construct(mixed $key = ?, mixed $value = ?)

     public clear(): void
public copy(): Ds\Pair
public isEmpty(): bool
public toArray(): array

    }
```

## Зміст

-   [Ds\\Pair::clear](ds-pair.clear.md) \- Видаляє всі значення
-   [Ds\\Pair::\_\_construct](ds-pair.construct.md) \- Створює екземпляр класу
-   [Ds\\Pair::copy](ds-pair.copy.md)— Повертає поверхневу копію пари
-   [Ds\\Pair::isEmpty](ds-pair.isempty.md)— Перевіряє, чи пара порожня.
-   [Ds\\Pair::jsonSerialize](ds-pair.jsonserialize.md)— Повертає пару у виставі JSON
-   [Ds\\Pair::toArray](ds-pair.toarray.md) \- Перетворює пару в масив (array)
