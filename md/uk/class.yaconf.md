Клас Yaconf

-   [« Обумовлені константи](yaconf.constants.html)
    
-   [Yaconf::get »](yaconf.get.html)
    
-   [PHP Manual](index.html)
    
-   [Yaconf](book.yaconf.html)
    
-   Клас Yaconf
    

# Клас Yaconf

(PECL yaconf> = 1.0.0)

## Вступ

Yaconf - контейнер конфігурацій, він розбирає конфігураційні файли, зберігає результат у PHP під час запуску PHP, результат зберігається протягом усього життєвого циклу PHP.

## Огляд класів

```classsynopsis



    
     
      class Yaconf
     
     {


    /* Методы */
    
   public static get(string $name, mixed $default_value = NULL): mixed
public static has(string $name): bool

   }
```

## Зміст

-   [Yaconf::get](yaconf.get.html) — Вийняти елемент
-   [Yaconf::has](yaconf.has.html) — Визначити, чи існує елемент