Отримує зворотне трасування поточної точки виконання

-   [« ReflectionFiber::getFiber](reflectionfiber.getfiber.md)
    
-   [ReflectionIntersectionType »](class.reflectionintersectiontype.md)
    
-   [PHP Manual](index.md)
    
-   [ReflectionFiber](class.reflectionfiber.md)
    
-   Отримує зворотне трасування поточної точки виконання
    

# ReflectionFiber::getTrace

(PHP 8> = 8.1.0)

ReflectionFiber::getTrace — Отримує зворотне трасування поточної точки виконання

### Опис

```methodsynopsis
public ReflectionFiber::getTrace(int $options = DEBUG_BACKTRACE_PROVIDE_OBJECT): array
```

Отримує зворотне трасування поточної точки виконання відображеного класу [Fiber](class.fiber.md)

### Список параметрів

`options`

Значення `options` може бути будь-яким із наступних прапорів: the following flags.

**Доступні параметри**

| Параметр                             | Описание                                                          |
|--------------------------------------|-------------------------------------------------------------------|
| **`DEBUG_BACKTRACE_PROVIDE_OBJECT`** | За замовчуванням.                                                 |
| **`DEBUG_BACKTRACE_IGNORE_ARGS`**    | Не включати інформацію про аргумент для функцій трасування стека. |

### Значення, що повертаються

Відстежує поточну точку виконання файбера.