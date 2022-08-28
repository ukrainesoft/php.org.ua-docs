Клас Volatile

-   [« Pool::submitTo](pool.submitTo.html)
    
-   [Семафоры »](book.sem.html)
    
-   [PHP Manual](index.html)
    
-   [pthreads](book.pthreads.html)
    
-   Клас Volatile
    

# Клас Volatile

(PECL pthreads >= 3.0.0)

## Вступ

Клас **Volatile** з'явився в pthreads v3. Його запровадження є наслідком нової семантики незмінності [Threaded](class.threaded.html)властивостей класів [Threaded](class.threaded.html). Клас **Volatile** включає іммутабельність їх [Threaded](class.threaded.html)властивостей і також використовується для зберігання масивів PHP в контексті [Threaded](class.threaded.html)

## Огляд класів

```classsynopsis


    
    
     
      class Volatile
     

     
      extends
       Threaded
     

     implements 
       Collectable,  Traversable {

    /* Наследуемые методы */
    
   public Threaded::chunk(int $size, bool $preserve): array
public Threaded::count(): int
public Threaded::extend(string $class): bool
public Threaded::isRunning(): bool
public Threaded::isTerminated(): bool
public Threaded::merge(mixed $from, bool $overwrite = ?): bool
public Threaded::notify(): bool
public Threaded::notifyOne(): bool
public Threaded::pop(): bool
public Threaded::run(): void
public Threaded::shift(): mixed
public Threaded::synchronized(Closure $block, mixed ...$args): mixed
public Threaded::wait(int $timeout = ?): bool

   }
```

## Приклади

**Приклад #1 Нова семантика іммутабельності Threaded**

```php
<?php

class Task extends Threaded
{
    public function __construct()
    {
        $this->data = new Threaded();

        // попытка переопределить Threaded-свойство Threaded-класса (ошибка)
        $this->data = new StdClass();
    }
}

var_dump((new Task())->data);
```

Результатом виконання цього прикладу буде щось подібне:

```
RuntimeException: Threaded members previously set to Threaded objects are immutable, cannot overwrite data in %s:%d
```

**Приклад #2 Приклад використання Volatile**

```php
<?php

class Task extends Volatile
{
    public function __construct()
    {
        $this->data = new Threaded();

        // попытка переопределить Threaded-свойство Volatile-класса (корректно)
        $this->data = new StdClass();
    }
}

var_dump((new Task())->data);
```

Результатом виконання цього прикладу буде щось подібне:

```
object(stdClass)#3 (0) {
}
```