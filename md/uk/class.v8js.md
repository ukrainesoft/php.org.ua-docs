Клас V8Js

-   [« Приклади](v8js.examples.html)
    
-   [V8Js::construct »](v8js.construct.html)
    
-   [PHP Manual](index.html)
    
-   [V8js](book.v8js.html)
    
-   Клас V8Js
    

# Клас [V8Js](class.v8js.html)

(PECL v8js >= 0.1.0)

## Вступ

Це основний клас модуля V8Js. Кожен екземпляр цього класу має власний контекст у якому буде скомпільовано та запущено JavaScript.

Також дивіться [V8Js::construct()](v8js.construct.html)

## Огляд класів

```classsynopsis


    
    
     
      class V8Js
     
     {
    
    /* Константы */
    
     const
     string
      V8_VERSION;

    const
     int
      FLAG_NONE = 1;

    const
     int
      FLAG_FORCE_ARRAY = 2;


    /* Методы */
    
   public __construct(    string $object_name = "PHP",    array $variables = array(),    array $extensions = array(),    bool $report_uncaught_exceptions = true)

    public executeString(string $script, string $identifier = "V8Js::executeString()", int $flags = V8Js::FLAG_NONE): mixed
public static getExtensions(): array
public getPendingException(): V8JsException
public static registerExtension(    string $extension_name,    string $script,    array $dependencies = array(),    bool $auto_enable = false): bool

   }
```

## Обумовлені константи

**`V8Js::V8_VERSION`**

Версія двигуна V8 Javascript.

**`V8Js::FLAG_NONE`**

Без прапорів.

**`V8Js::FLAG_FORCE_ARRAY`**

Примушує об'єкти JS бути асоціативними масивами PHP.

## Зміст

-   [V8Js::construct](v8js.construct.html) - Створює новий об'єкт V8Js
-   [V8Js::executeString](v8js.executestring.html) — Виконати рядок як код Javascript
-   [V8Js::getExtensions](v8js.getextensions.html) — Повертає масив зареєстрованих модулів
-   [V8Js::getPendingException](v8js.getpendingexception.html) — Повертає очікуваний непойманий виняток Javascript
-   [V8Js::registerExtension](v8js.registerextension.html) - Реєстрація модуля Javascript для V8Js