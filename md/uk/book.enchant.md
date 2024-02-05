---
navigation:
  - refs.international.md: « Підтримка мов та кодувань
  - intro.enchant.md: Вступ "
  - index.md: PHP Manual
  - refs.international.md: Підтримка мов та кодувань
title: Бібліотека перевірки правопису Enchant
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Бібліотека перевірки правопису Enchant

-   [Вступ](intro.enchant.md)
-   [Встановлення та налаштування](enchant.setup.md)
    -   [Вимоги](enchant.requirements.md)
    -   [Установка](enchant.installation.md)
    -   [Налаштування під час виконання](enchant.configuration.md)
    -   [Типи ресурсів](enchant.resources.md)
-   [Обумовлені константи](enchant.constants.md)
-   [Приклади](enchant.examples.md)
-   [Функції Enchant](ref.enchant.md)
    -   [enchant\_broker\_describe](function.enchant-broker-describe.md) \- Перераховує провайдерів Enchant
    -   [enchant\_broker\_dict\_exists](function.enchant-broker-dict-exists.md)— Перевіряє, чи є словник чи ні. Використовується не пустий тег
    -   [enchant\_broker\_free\_dict](function.enchant-broker-free-dict.md) \- Звільняє ресурс словника
    -   [enchant\_broker\_free](function.enchant-broker-free.md)— Звільняє ресурс брокера та його словники
    -   [enchant\_broker\_get\_dict\_path](function.enchant-broker-get-dict-path.md)— Повертає шлях словника для заданого бекенду
    -   [enchant\_broker\_get\_error](function.enchant-broker-get-error.md) \- Повертає останню помилку брокера
    -   [enchant\_broker\_init](function.enchant-broker-init.md) \- Створити новий об'єкт брокера
    -   [enchant\_broker\_list\_dicts](function.enchant-broker-list-dicts.md)— Повертає список доступних словників
    -   [enchant\_broker\_request\_dict](function.enchant-broker-request-dict.md)— Створити новий словник, використовуючи тег
    -   [enchant\_broker\_request\_pwl\_dict](function.enchant-broker-request-pwl-dict.md)— Створити словник, використовуючи файл PWL
    -   [enchant\_broker\_set\_dict\_path](function.enchant-broker-set-dict-path.md)— Встановити шлях для заданого бекенду
    -   [enchant\_broker\_set\_ordering](function.enchant-broker-set-ordering.md)— Надати перевагу вибору словників для мови
    -   [enchant\_dict\_add\_to\_personal](function.enchant-dict-add-to-personal.md)— Додати слово до списку персональних слів
    -   [enchant\_dict\_add\_to\_session](function.enchant-dict-add-to-session.md)— Додати слово до поточної сесії перевірки
    -   [enchant\_dict\_add](function.enchant-dict-add.md)— Додає слово до особистого словника
    -   [enchant\_dict\_check](function.enchant-dict-check.md)— Перевіряє, чи правильно задано слово
    -   [enchant\_dict\_describe](function.enchant-dict-describe.md)— Повертає інформацію про словник
    -   [enchant\_dict\_get\_error](function.enchant-dict-get-error.md)— Повертає останню помилку поточної сесії перевірки
    -   [enchant\_dict\_is\_added](function.enchant-dict-is-added.md)— Визначає, чи існує слово у цій орфографічній сесії
    -   [enchant\_dict\_is\_in\_session](function.enchant-dict-is-in-session.md) — Чи є слово 'word' у сесії перевірки
    -   [enchant\_dict\_quick\_check](function.enchant-dict-quick-check.md)— Перевірити, чи правильно написано слово та запропонувати варіанти заміни
    -   [enchant\_dict\_store\_replacement](function.enchant-dict-store-replacement.md)— Додати виправлення до слова
    -   [enchant\_dict\_suggest](function.enchant-dict-suggest.md)— Поверне список можливих варіантів для слова з помилкою
-   [EnchantBroker](class.enchantbroker.md) \- Клас EnchantBroker
-   [EnchantDictionary](class.enchantdictionary.md) \- Клас EnchantDictionary
