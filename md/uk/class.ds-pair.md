---
navigation:
  - ds-map.xor.md: '« DsMap::xor'
  - ds-pair.clear.md: 'ДсPair::clear »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Pair
---
# Клас Pair

(No version information available, might only be in Git)

## Вступ

Пара використовується класом **ДсMap** для зберігання пар ключ-значення.

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

-   [ДсPair::clear](ds-pair.clear.md) - Видаляє всі значення
-   [ДсPair::construct](ds-pair.construct.md) - Створює екземпляр класу
-   [ДсPair::copy](ds-pair.copy.md) — Повертає поверхневу копію пари
-   [ДсPair::isEmpty](ds-pair.isempty.md) — Перевіряє, чи пара порожня.
-   [ДсPair::jsonSerialize](ds-pair.jsonserialize.md) — Повертає пару у виставі JSON
-   [ДсPair::toArray](ds-pair.toarray.md) - Перетворює пару в масив (array)
