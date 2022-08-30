Створює ReflectionReference з елемента масиву

-   [« ReflectionReference::construct](reflectionreference.construct.html)
    
-   [ReflectionReference::getId »](reflectionreference.getid.html)
    
-   [PHP Manual](index.html)
    
-   [ReflectionReference](class.reflectionreference.html)
    
-   Створює ReflectionReference з елемента масиву
    

# ReflectionReference::fromArrayElement

(PHP 7> = 7.4.0, PHP 8)

ReflectionReference::fromArrayElement — Створює ReflectionReference з елемента масиву

### Опис

```methodsynopsis
public static ReflectionReference::fromArrayElement(array $array, int|string $key): ?ReflectionReference
```

Створює [ReflectionReference](class.reflectionreference.html) елемент масиву.

### Список параметрів

`array`

Масив, що містить потенційне посилання.

`key`

Ключ; ціле число(int) чи рядок(string).

### Значення, що повертаються

Повертає екземпляр **ReflectionReference** якщо `$array[$key]` є посиланням, або **`null`** в іншому випадку.

### Помилки

Якщо `array` не є масивом, або `key` не є цілим числом (int) або рядком (string), буде викинуто виняток [TypeError](class.typeerror.html). Якщо `$array[$key]` не заданий, то буде викинуто виняток [ReflectionException](class.reflectionexception.html)