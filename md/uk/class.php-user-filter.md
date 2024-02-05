---
navigation:
  - stream.streamwrapper.example-1.md: '« Приклад класу, зареєстрованого як обгортка потоку'
  - php-user-filter.filter.md: 'php\_user\_filter::filter »'
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Клас php\_user\_filter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас php\_user\_filter

(PHP 5, PHP 7, PHP 8)

## Вступ

Нащадки цього класу передаються у функцію [stream\_filter\_register()](function.stream-filter-register.md)Обратите внимание, что метод[\_\_construct](language.oop5.decon.md#object.construct) не викликається; натомість для ініціалізації слід використовувати [php\_user\_filter::onCreate()](php-user-filter.oncreate.md)

## Огляд класів

```classsynopsis

    
     class php_user_filter
     {

    /* Свойства */
    
     public
     string
      $filtername = "";

    public
     mixed
      $params = "";

    public
     ?resource
      $stream = null;


    /* Методы */
    
   public filter(    resource $in,    resource $out,    int &$consumed,    bool $closing): int
public onClose(): void
public onCreate(): bool

   }
```

## Властивості

filtername

Ім'я фільтра, зареєстрованого функцією [stream\_filter\_append()](function.stream-filter-append.md)

params

stream

## Зміст

-   [php\_user\_filter::filter](php-user-filter.filter.md)— Викликається, щойно застосовується фільтр
-   [php\_user\_filter::onClose](php-user-filter.onclose.md)— Викликається під час закриття фільтра
-   [php\_user\_filter::onCreate](php-user-filter.oncreate.md)— Викликається під час створення об'єкта фільтра
