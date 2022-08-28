Клас YafRegistry

-   [« Yaf\_Plugin\_Abstract::routerStartup](yaf-plugin-abstract.routerstartup.html)
    
-   [Yaf\_Registry::\_\_construct »](yaf-registry.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Yaf](book.yaf.html)
    
-   Клас YafRegistry
    

# Клас YafRegistry

(Yaf >=1.0.0)

## Вступ

Усі методи **YafRegistry** визначено як статичні, роблячи їх універсально доступними. Це надає можливості прочитати або записати будь-які дані з будь-якого місця у вашому додатку.

## Огляд класів

```classsynopsis


    
    
     
      class Yaf_Registry
     
     {
    
    /* Свойства */
    
     static
      $_instance;

    protected
      $_entries;



    /* Методы */
    
   private __construct()

    public static del(string $name): void
public static get(string $name): mixed
public static has(string $name): bool
public static set(string $name, string $value): bool

   }
```

## Властивості

instance

entries

## Зміст

-   [Yaf\_Registry::\_\_construct](yaf-registry.construct.html) - YafRegistry реалізує шаблон проектування "Одиночка"
-   [Yaf\_Registry::del](yaf-registry.del.html) — Видаляє елемент із реєстру
-   [Yaf\_Registry::get](yaf-registry.get.html) — Отримує елемент із реєстру
-   [Yaf\_Registry::has](yaf-registry.has.html) — Перевіряє, чи існує елемент
-   [Yaf\_Registry::set](yaf-registry.set.html) — Додає елемент до реєстру