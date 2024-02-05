---
navigation:
  - refs.crypto.md: « Криптографічні модулі
  - intro.hash.md: Вступ "
  - index.md: PHP Manual
  - refs.crypto.md: Криптографічні модулі
title: Фреймворк хеш-кодів HASH
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Фреймворк хеш-кодів HASH

-   [Вступ](intro.hash.md)
-   [Встановлення та налаштування](hash.setup.md)
    -   [Вимоги](hash.requirements.md)
    -   [Установка](hash.installation.md)
    -   [Налаштування під час виконання](hash.configuration.md)
    -   [Типи ресурсів](hash.resources.md)
-   [Обумовлені константи](hash.constants.md)
-   [HashContext](class.hashcontext.md) \- Клас HashContext
    -   [HashContext::\_\_construct](hashcontext.construct.md)— Закритий конструктор для заборони безпосереднього створення об'єкту
    -   [HashContext::\_\_serialize](hashcontext.serialize.md)— Серіалізує об'єкт HashContext
    -   [HashContext::\_\_unserialize](hashcontext.unserialize.md)— Десеріалізує параметр data в об'єкті HashContext
-   [Функції Hash](ref.hash.md)
    -   [hash\_algos](function.hash-algos.md)— Повертає список зареєстрованих алгоритмів хешування
    -   [hash\_copy](function.hash-copy.md)— Копіює контекст хешування
    -   [hash\_equals](function.hash-equals.md)— Порівнює рядки без ризику атаки за часом
    -   [hash\_file](function.hash-file.md) \- Генерація хеш-значення, використовуючи вміст заданого файлу
    -   [hash\_final](function.hash-final.md)— Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
    -   [hash\_hkdf](function.hash-hkdf.md)— Формування ключа HKDF для заданих вхідних даних
    -   [hash\_hmac\_algos](function.hash-hmac-algos.md)— Повертає список зареєстрованих алгоритмів хешування, які застосовуються для hash\_hmac
    -   [hash\_hmac\_file](function.hash-hmac-file.md)— Генерація хеш-коду на основі ключа, використовуючи метод HMAC та вміст отриманого файлу
    -   [hash\_hmac](function.hash-hmac.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC
    -   [hash\_init](function.hash-init.md) \- Ініціалізація інкрементального контексту хешування
    -   [hash\_pbkdf2](function.hash-pbkdf2.md) \- Формування ключа PBKDF2 для заданих вхідних даних
    -   [hash\_update\_file](function.hash-update-file.md)— Додає дані з файлу до активного контексту хешування
    -   [hash\_update\_stream](function.hash-update-stream.md)— Додає дані з відкритого потоку до активного контексту хешування
    -   [hash\_update](function.hash-update.md)— Додає дані до активного контексту хешування
    -   [hash](function.hash.md) \- Генерує хеш-код (підпис повідомлення)
