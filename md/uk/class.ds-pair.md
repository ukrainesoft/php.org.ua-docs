Клас Pair

-   [« Ds\\Map::xor](ds-map.xor.html)
    
-   [Ds\\Pair::clear »](ds-pair.clear.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Клас Pair
    

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

-   [Ds\\Pair::clear](ds-pair.clear.html) - Видаляє всі значення
-   [Ds\\Pair::\_\_construct](ds-pair.construct.html) - Створює екземпляр класу
-   [Ds\\Pair::copy](ds-pair.copy.html) — Повертає поверхневу копію пари
-   [Ds\\Pair::isEmpty](ds-pair.isempty.html) — Перевіряє, чи пара порожня.
-   [Ds\\Pair::jsonSerialize](ds-pair.jsonserialize.html) — Повертає пару у виставі JSON
-   [Ds\\Pair::toArray](ds-pair.toarray.html) - Перетворює пару в масив (array)