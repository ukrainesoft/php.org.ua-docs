Callback-функції

-   [« О постоянных(persistent) событиях](event.persistence.html)
    
-   [Создание событий для сигналов »](event.constructing.signal.events.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Callback-функції
    

# Callback-функції

Якщо для події зареєстрована callback-функція, вона буде викликана, коли подія перейде в активний статус. Для прив'язування функції до події необхідно передати її як параметр [callable](language.types.callable.html) в [Event::\_\_construct()](event.construct.html) або [Event::set()](event.set.html) або в один із фабричних методів, таких як [Event::timer()](event.timer.html)

Функція повинна відповідати наступному прототипу:

```methodsynopsis
callback(
   mixed
     $fd
     = null
  , 
   int
     $what
   = ?, 
   mixed
     $arg
     = null
  ): void
```

`fd`

Дескриптор файлу, потокового ресурсу чи сокету, пов'язані з подією. Для подій сигналів `fd` збігається із номером сигналу.

`what`

Побітова маска *всіх* оброблюваних подій.

`arg`

Дані користувача.

Для [Event::timer()](event.timer.html) callback-функція повинна відповідати наступному прототипу:

```methodsynopsis
callback(
   mixed
     $arg
     = null
  ): void
```

`arg`

Дані користувача.

Для [Event::signal()](event.signal.html) callback-функція повинна відповідати наступному прототипу:

```methodsynopsis
callback(
   int
     $signum
   = ?, 
   mixed
     $arg
     = null
  ): void
```

`signum`

Номер сигналу (наприклад, **`SIGTERM`**

`arg`

Дані користувача.