Контексти потоків

-   [« Потоковые фильтры](stream.filters.html)
    
-   [Ошибки потока »](stream.errors.html)
    
-   [PHP Manual](index.html)
    
-   [Потоки](book.stream.html)
    
-   Контексти потоків
    

# Контексти потоків

`Контекст` - це набір `параметров` та залежних від контексту `опций`, який змінює або розширює поведінку потоку . `Контексты` створюються за допомогою функції [stream\_context\_create()](function.stream-context-create.html) і можуть бути передані більшості функцій файлової системи, пов'язаних із створенням потоків (наприклад, [fopen()](function.fopen.html) [file()](function.file.html) [file\_get\_contents()](function.file-get-contents.html), і т.д...).

`Опции` можуть бути визначені під час виклику функції [stream\_context\_create()](function.stream-context-create.html), чи пізніше, використовуючи функцію [stream\_context\_set\_option()](function.stream-context-set-option.html). Список можливих `опций` у цьому контексті може бути знайдений у розділі [Контекстные опции и параметры](context.html)

`Параметры` можуть бути визначені для `контекстов`, використовуючи функцію [stream\_context\_set\_params()](function.stream-context-set-params.html)