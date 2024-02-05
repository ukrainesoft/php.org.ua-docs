---
navigation:
  - rnp.examples-clearsign.md: « Підписання тексту
  - function.rnp-backend-string.md: rnp\_backend\_string »
  - index.md: PHP Manual
  - book.rnp.md: Rnp
title: Функції Rnp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Функції Rnp

## Зміст

-   [rnp\_backend\_string](function.rnp-backend-string.md)— Повертає ім'я бібліотеки криптографічного бекенду
-   [rnp\_backend\_version](function.rnp-backend-version.md)— Повертає версію криптографічної бібліотеки бекенду
-   [rnp\_decrypt](function.rnp-decrypt.md)— Розшифровує PGP-повідомлення
-   [rnp\_dump\_packets\_to\_json](function.rnp-dump-packets-to-json.md)— Вивантаження інформації про потік пакетів OpenPGP у рядок JSON
-   [rnp\_dump\_packets](function.rnp-dump-packets.md)— Вивантажує інформацію про потік пакетів OpenPGP у людино-читаному форматі
-   [rnp\_ffi\_create](function.rnp-ffi-create.md)— Створює об'єкт верхнього рівня, який використовується для взаємодії з бібліотекою
-   [rnp\_ffi\_destroy](function.rnp-ffi-destroy.md)— Знищує об'єкт верхнього рівня, який використовується для взаємодії з бібліотекою
-   [rnp\_ffi\_set\_pass\_provider](function.rnp-ffi-set-pass-provider.md) \- Встановлює callback-функцію постачальника паролів
-   [rnp\_import\_keys](function.rnp-import-keys.md)— Імпортує ключі з рядка PHP у зв'язок ключів і отримує JSON з описом нових/оновлених ключів
-   [rnp\_import\_signatures](function.rnp-import-signatures.md)— Імпортує автономні підписи у зв'язку ключів та отримує JSON з описом оновлених ключів
-   [rnp\_key\_export\_autocrypt](function.rnp-key-export-autocrypt.md) \- Експортує мінімальний ключ для функції автоматичного шифрування (всього 5 пакетів: ключ, uid, підпис, дочірній ключ шифрування, підпис)
-   [rnp\_key\_export\_revocation](function.rnp-key-export-revocation.md)— Генерує та експортує підпис відкликання первинного ключа
-   [rnp\_key\_export](function.rnp-key-export.md) \- Експортує ключ
-   [rnp\_key\_get\_info](function.rnp-key-get-info.md)— Отримує інформацію про ключ
-   [rnp\_key\_remove](function.rnp-key-remove.md)— Видаляє ключ зі зв'язування
-   [rnp\_key\_revoke](function.rnp-key-revoke.md)— Відкликає ключ або дочірній ключ шляхом створення та додавання підпису відгуку
-   [rnp\_list\_keys](function.rnp-list-keys.md)— Перераховує всі ключі, які є у зв'язці ключів, за вказаним типом ідентифікатора
-   [rnp\_load\_keys\_from\_path](function.rnp-load-keys-from-path.md)— Завантажує ключі із зазначеного шляху
-   [rnp\_load\_keys](function.rnp-load-keys.md)— Завантажує ключі з рядка PHP
-   [rnp\_locate\_key](function.rnp-locate-key.md) \- Пошук ключа
-   [rnp\_op\_encrypt](function.rnp-op-encrypt.md) \- Шифрує повідомлення
-   [rnp\_op\_generate\_key](function.rnp-op-generate-key.md) \- Генерує ключ
-   [rnp\_op\_sign\_cleartext](function.rnp-op-sign-cleartext.md)— Виконує операцію підписання текстових даних, повертаючи підписаний відкритий текст повідомлення
-   [rnp\_op\_sign\_detached](function.rnp-op-sign-detached.md) \- Виконує операцію підписання, повертає від'єднаний підпис (підписи)
-   [rnp\_op\_sign](function.rnp-op-sign.md) \- Виконує операцію підписання бінарних даних, повертає приєднаний підпис (підписи)
-   [rnp\_op\_verify\_detached](function.rnp-op-verify-detached.md)— Перевіряє від'єднані підписи
-   [rnp\_op\_verify](function.rnp-op-verify.md)— Перевіряє приєднаний підпис або підпис відкритого тексту
-   [rnp\_save\_keys\_to\_path](function.rnp-save-keys-to-path.md)— Зберігає ключі зазначеним шляхом
-   [rnp\_save\_keys](function.rnp-save-keys.md)— Зберігає ключі у рядку PHP
-   [rnp\_supported\_features](function.rnp-supported-features.md)— Отримує функції, що підтримуються у форматі JSON
-   [rnp\_version\_string\_full](function.rnp-version-string-full.md)— Повертає рядок повної версії бібліотеки RNP
-   [rnp\_version\_string](function.rnp-version-string.md)— Повертає рядок версії бібліотеки RNP
