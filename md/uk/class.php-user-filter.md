Клас phpuserfilter

-   [« Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.html)
    
-   [phpuserfilter::filter »](php-user-filter.filter.html)
    
-   [PHP Manual](index.html)
    
-   [Потоки](book.stream.html)
    
-   Клас phpuserfilter
    

# Клас phpuserfilter

(PHP 5, PHP 7, PHP 8)

## Вступ

Нащадки цього класу передаються у функцію [streamfilterregister()](function.stream-filter-register.html). Зверніть увагу, що метод [construct](language.oop5.decon.html#object.construct) не викликається; натомість для ініціалізації слід використовувати [phpuserfilter::onCreate()](php-user-filter.oncreate.html)

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

Ім'я фільтра, зареєстрованого функцією [streamfilterappend()](function.stream-filter-append.html)

params

stream

## Зміст

-   [phpuserfilter::filter](php-user-filter.filter.html) — Викликається, щойно застосовується фільтр
-   [phpuserfilter::onClose](php-user-filter.onclose.html) — Викликається під час закриття фільтра
-   [phpuserfilter::onCreate](php-user-filter.oncreate.html) — Викликається під час створення об'єкта фільтра