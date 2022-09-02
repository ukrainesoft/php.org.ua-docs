---
navigation:
  - stream.streamwrapper.example-1.md: '« Приклад класу, зареєстрованого як обгортка потоку'
  - php-user-filter.filter.md: 'phpuserfilter::filter »'
  - index.md: PHP Manual
  - book.stream.md: Потоки
title: Клас phpuserfilter
---
# Клас phpuserfilter

(PHP 5, PHP 7, PHP 8)

## Вступ

Нащадки цього класу передаються у функцію [streamfilterregister()](function.stream-filter-register.md). Зверніть увагу, що метод [construct](language.oop5.decon.md#object.construct) не викликається; натомість для ініціалізації слід використовувати [phpuserfilter::onCreate()](php-user-filter.oncreate.md)

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

Ім'я фільтра, зареєстрованого функцією [streamfilterappend()](function.stream-filter-append.md)

params

stream

## Зміст

-   [phpuserfilter::filter](php-user-filter.filter.md) — Викликається, щойно застосовується фільтр
-   [phpuserfilter::onClose](php-user-filter.onclose.md) — Викликається під час закриття фільтра
-   [phpuserfilter::onCreate](php-user-filter.oncreate.md) — Викликається під час створення об'єкта фільтра
