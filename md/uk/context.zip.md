- [« Параметри контексту](context.params.md)
- [Підтримувані протоколи та обгортки »](wrappers.md)

- [PHP Manual](index.md)
- [Контекстні опції та параметри](context.md)
- Список опцій контексту Zip

# Опції контексту Zip

Опції контексту Zip - Список опцій контексту Zip

### Опис

Опції контексту Zip доступні для обгорток `zip`.

### Опції

`password`
Використовується для вказівки пароля, який використовується для зашифрованих
архівів.

### Список змін

| Версія                     | Опис                       |
|----------------------------|----------------------------|
| PHP 7.2.0, PECL zip 1.14.0 | Доданий параметр password. |

### Приклади

**Приклад #1 Простий приклад використання `password`**

` <?php// Читаємо зашифрований архів$opts = array(   'zip' => array(        'password' => 'secret', stre_context)); // ...і використовується його для отримання данихecho file_get_contents('zip://test.zip#test.txt', false, $context);?> `
