- [« $\_SERVER](reserved.variables.server.md)
- [$\_POST »](reserved.variables.post.md)

- [PHP Manual](index.md)
- [Предвизначені змінні](reserved.variables.md)
- Змінні HTTP GET

# $\_GET

(PHP 4 \>= 4.1.0, PHP 5, PHP 7, PHP 8)

$\_GET — Змінні HTTP GET

### Опис

Асоціативний масив змінних, переданих скрипту через параметри URL
(відомі також як рядок запиту). Зверніть увагу, що масив не
тільки заповнюється для GET-запитів, а скоріше для всіх запитів
рядком запиту.

### Приклади

**Приклад #1 Приклад використання `$_GET`**

`<?phpecho 'Привіт, ' . htmlspecialchars($_GET["name"]) . '!';?> `

Очевидно, що користувач ввів у браузері адресу
http://example.com/?name=Іван

Результатом виконання цього прикладу буде щось подібне:

Привіт, Іване!

### Примітки

> **Примітка**:
>
> Це 'суперглобальна' або автоматична глобальна змінна. Це
> просто означає, що вона є у всіх контекстах скрипта. Ні
> необхідності виконувати **global $variable;** для доступу до неї всередині
> методу чи функції.

> **Примітка**:
>
> Параметри GET обробляються [urldecode()](function.urldecode.md).

### Дивіться також

- [Змінні ззовні PHP](language.variables.external.md)
- [Фільтрування даних](book.filter.md)
