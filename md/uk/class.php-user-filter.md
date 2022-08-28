Клас phpuserfilter

-   [« Пример класса, зарегистрированного в качестве обёртки потока](stream.streamwrapper.example-1.html)
    
-   [php\_user\_filter::filter »](php-user-filter.filter.html)
    
-   [PHP Manual](index.html)
    
-   [Потоки](book.stream.html)
    
-   Клас phpuserfilter
    

# Клас phpuserfilter

(PHP 5, PHP 7, PHP 8)

## Вступ

Нащадки цього класу передаються у функцію [stream\_filter\_register()](function.stream-filter-register.html). Зверніть увагу, що метод [\_\_construct](language.oop5.decon.html#object.construct) не викликається; натомість для ініціалізації слід використовувати [php\_user\_filter::onCreate()](php-user-filter.oncreate.html)

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

Ім'я фільтра, зареєстрованого функцією [stream\_filter\_append()](function.stream-filter-append.html)

params

stream

## Зміст

-   [php\_user\_filter::filter](php-user-filter.filter.html) — Викликається, щойно застосовується фільтр
-   [php\_user\_filter::onClose](php-user-filter.onclose.html) — Викликається під час закриття фільтра
-   [php\_user\_filter::onCreate](php-user-filter.oncreate.html) — Викликається під час створення об'єкта фільтра