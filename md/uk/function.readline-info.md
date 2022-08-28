Встановлює/читає різні внутрішні змінні readline

-   [« readline\_completion\_function](function.readline-completion-function.html)
    
-   [readline\_list\_history »](function.readline-list-history.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Readline](ref.readline.html)
    
-   Встановлює/читає різні внутрішні змінні readline
    

# readlineinfo

(PHP 4, PHP 5, PHP 7, PHP 8)

readlineinfo — Встановлює/читає різні внутрішні змінні readline

### Опис

```methodsynopsis
readline_info(?string $var_name = null, int|string|bool|null $value = null): mixed
```

Встановлює/читає різні внутрішні змінні readline.

### Список параметрів

`var_name`

Ім'я змінної.

`value`

Якщо встановлено, то змінної буде присвоєно це значення.

### Значення, що повертаються

Якщо викликати функцію без параметрів, буде повернуто масив значень всіх внутрішніх змінних readline. Елементи масиву матимуть наступні індекси: done, end, eraseemptyline, libraryversion, linebuffer, mark, pendinginput, point, prompt, readlinename та terminalname.

Якщо викликати з одним або двома параметрами, то повернеться старе/поточне значення змінної.

### список змін

| Версия | Описание                                             |
|--------|------------------------------------------------------|
|        | `var_name` і `value` тепер допускають значення null. |