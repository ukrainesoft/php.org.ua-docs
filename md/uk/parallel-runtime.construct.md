Конструктор класу Runtime

-   [« parallel\\Runtime](class.parallel-runtime.html)
    
-   [parallel\\Runtime::run »](parallel-runtime.run.html)
    
-   [PHP Manual](index.html)
    
-   [parallel\\Runtime](class.parallel-runtime.html)
    
-   Конструктор класу Runtime
    

# parallelRuntime::construct

parallelRuntime::construct - Конструктор класу Runtime

### Опис

public **parallelRuntime::construct**

Створює нове виконання без початкового завантаження.

public **parallelRuntime::construct**(string `$bootstrap`

Створює нове середовище виконання з початковим завантаженням.

### Список параметрів

`bootstrap`

Розташування файлу початкового завантаження зазвичай це автозавантажувач.

### Помилки

**Увага**

Викидає parallelRuntimeError, якщо потік не може бути створений.

**Увага**

Викидає parallelRuntimeBootstrap, якщо початкове завантаження завершилося з помилкою.