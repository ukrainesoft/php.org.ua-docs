---
navigation:
  - yaconf.constants.md: « Зумовлені константи
  - yaconf.get.md: 'Yaconf::get »'
  - index.md: PHP Manual
  - book.yaconf.md: Yaconf
title: Клас Yaconf
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Yaconf

(PECL yaconf >= 1.0.0)

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

-   [Yaconf::get](yaconf.get.md)— Вийняти елемент
-   [Yaconf::has](yaconf.has.md)— Визначити, чи існує елемент
