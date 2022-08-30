Потоки для взаємодії з процесами

-   [« ogg://](wrappers.audio.html)
    
-   [Безпека »](security.html)
    
-   [PHP Manual](index.html)
    
-   [Підтримувані протоколи та обгортки](wrappers.html)
    
-   Потоки для взаємодії з процесами
    

# expect://

expect:// - Потоки для взаємодії з процесами

### Опис

Потоки, відкриті за допомогою обгортки expect://, надають доступ до процесів stdio, stdout та stderr через PTY.

> **Зауваження** **Ця обгортка вимкнена за умовчанням**  
> Для того щоб використовувати обгортку expect://, необхідно встановити модуль [» Expect](https://pecl.php.net/package/expect), доступний у [» PECL](https://pecl.php.net/)

expect:// (PECL)

### Використання

-   expect://command

### Опції

**Основна інформація**

| Атрибут                                                                         | Поддержка |
|---------------------------------------------------------------------------------|-----------|
| Обмеження по [allowurlfopen](filesystem.configuration.html#ini.allow-url-fopen) | Ні        |
| Читання                                                                         | Так       |
| Запис                                                                           | Так       |
| Додавання                                                                       | Так       |
| Одночасне читання та запис                                                      | Ні        |
| Підтримка [stat()](function.stat.html)                                          | Ні        |
| Підтримка [unlink()](function.unlink.html)                                      | Ні        |
| Підтримка [rename()](function.rename.html)                                      | Ні        |
| Підтримка [mkdir()](function.mkdir.html)                                        | Ні        |
| Підтримка [rmdir()](function.rmdir.html)                                        | Ні        |

### Приклади