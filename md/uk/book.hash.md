---
navigation:
  - function.random-int.md: « randomint
  - intro.hash.md: Введение »
  - index.md: PHP Manual
  - refs.crypto.md: Криптографічні модулі
title: Фреймворк хеш-кодів HASH
---
# Фреймворк хеш-кодів HASH

-   [Введение](intro.hash.md)
-   [Встановлення та налаштування](hash.setup.md)
    -   [Вимоги](hash.requirements.md)
    -   [Установка](hash.installation.md)
    -   [Налаштування під час виконання](hash.configuration.md)
    -   [Типи ресурсів](hash.resources.md)
-   [Обумовлені константи](hash.constants.md)
-   [HashContext](class.hashcontext.md) - Клас HashContext
    -   [HashContext::construct](hashcontext.construct.md) — Закритий конструктор для заборони безпосереднього створення об'єкту
    -   [HashContext::serialize](hashcontext.serialize.md) — Серіалізує об'єкт HashContext
    -   [HashContext::unserialize](hashcontext.unserialize.md) — Десеріалізує параметр data в об'єкті HashContext
-   [Функции Hash](ref.hash.md)
    -   [hashalgos](function.hash-algos.md) — Повертає список зареєстрованих алгоритмів хешування
    -   [hashcopy](function.hash-copy.md) — Копіює контекст хешування
    -   [hashequals](function.hash-equals.md) — Порівняння рядків, нечутливе до атак за часом
    -   [hashfile](function.hash-file.md) - Генерація хеш-значення, використовуючи вміст заданого файлу
    -   [hashfinal](function.hash-final.md) — Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
    -   [hashhkdf](function.hash-hkdf.md) — Формування ключа HKDF для заданих вхідних даних
    -   [hashhmacalgos](function.hash-hmac-algos.md) — Повертає список зареєстрованих алгоритмів хешування, які застосовуються для hashhmac
    -   [hashhmacfile](function.hash-hmac-file.md) — Генерація хеш-коду на основі ключа, використовуючи метод HMAC та вміст отриманого файлу
    -   [hashhmac](function.hash-hmac.md) - Генерація хеш-коду на основі ключа, використовуючи метод HMAC
    -   [hashinit](function.hash-init.md) - Ініціалізація інкрементального контексту хешування
    -   [hashpbkdf2](function.hash-pbkdf2.md) - Формування ключа PBKDF2 для заданих вхідних даних
    -   [hashupdatefile](function.hash-update-file.md) — Додає дані з файлу до активного контексту хешування
    -   [hashupdatestream](function.hash-update-stream.md) — Додає дані з відкритого потоку до активного контексту хешування
    -   [hashupdate](function.hash-update.md) — Додає дані до активного контексту хешування
    -   [hash](function.hash.md) - Генерує хеш-код (підпис повідомлення)
