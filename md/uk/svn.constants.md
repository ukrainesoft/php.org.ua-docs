---
navigation:
  - svn.resources.md: « Типи ресурсів
  - ref.svn.md: Функції SVN »
  - index.md: PHP Manual
  - book.svn.md: SVN
title: Обумовлені константи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Обумовлені константи

Наведені нижче константи визначені цим модулем і доступні або в збірках PHP з підтримкою цього модуля, або коли модуль динамічно завантажений під час виконання коду.

**`SVN_REVISION_HEAD`**(int)

Магічне число (-1), що вказує на останню ревізію

**Константи, що використовуються з [svn\_auth\_set\_parameter()](function.svn-auth-set-parameter.md)**

**`SVN_AUTH_PARAM_DEFAULT_USERNAME`**(string)

Властивість, що визначає ім'я користувача за умовчанням, яке використовуватиметься при виконанні базової автентифікації

**`SVN_AUTH_PARAM_DEFAULT_PASSWORD`**(string)

Властивість, що визначає пароль користувача за промовчанням, яке буде використовуватися при виконанні базової автентифікації

**`SVN_AUTH_PARAM_NON_INTERACTIVE`**(string)

**`SVN_AUTH_PARAM_DONT_STORE_PASSWORDS`**(string)

**`SVN_AUTH_PARAM_NO_AUTH_CACHE`**(string)

**`SVN_AUTH_PARAM_SSL_SERVER_FAILURES`**(string)

**`SVN_AUTH_PARAM_SSL_SERVER_CERT_INFO`**(string)

**`SVN_AUTH_PARAM_CONFIG`**(string)

**`SVN_AUTH_PARAM_SERVER_GROUP`**(string)

**`SVN_AUTH_PARAM_CONFIG_DIR`**(string)

**`PHP_SVN_AUTH_PARAM_IGNORE_SSL_VERIFY_ERRORS`**(string)

Поле, що передбачає ігнорування помилок верифікації SSL-сертифіката

**Константи файлової системи**

**`SVN_FS_CONFIG_FS_TYPE`**(string)

Ключ конфігурації, що визначає тип файлової системи

**`SVN_FS_TYPE_BDB`**(string)

Файлова система, реалізована Berkeley-DB

**`SVN_FS_TYPE_FSFS`**(string)

Файлова система, що реалізується стандартним чином

**Константи зарезервованих властивостей**

**`SVN_PROP_REVISION_DATE`**(string)

svn:date

**`SVN_PROP_REVISION_ORIG_DATE`**(string)

svn:original-date

**`SVN_PROP_REVISION_AUTHOR`**(string)

svn:author

**`SVN_PROP_REVISION_LOG`**(string)

svn:log

**Константи статусу робочої копії**

**`SVN_WC_STATUS_NONE`**(int)

Статус відсутній

**`SVN_WC_STATUS_UNVERSIONED`**(int)

Елемент не має версії у робочій копії

**`SVN_WC_STATUS_NORMAL`**(int)

Елемент існує, дій над ним не відбувається

**`SVN_WC_STATUS_ADDED`**(int)

Елемент запланований до додавання до репозиторію

**`SVN_WC_STATUS_MISSING`**(int)

Елемент має версію, але відсутня у робочій копії

**`SVN_WC_STATUS_DELETED`**(int)

Елемент запланований для видалення

**`SVN_WC_STATUS_REPLACED`**(int)

Елемент було видалено, а потім знову додано

**`SVN_WC_STATUS_MODIFIED`**(int)

Елемент (текст чи властивості) було змінено

**`SVN_WC_STATUS_MERGED`**(int)

Локальні зміни елемента були об'єднані із змінами в репозиторії

**`SVN_WC_STATUS_CONFLICTED`**(int)

Локальні зміни елемента конфліктують із змінами у репозиторії

**`SVN_WC_STATUS_IGNORED`**(int)

Елемент не має версії та ігнорується системою контролю версій

**`SVN_WC_STATUS_OBSTRUCTED`**(int)

Елемент, який не має версії, пов'язаний із ресурсом, що має версію.

**`SVN_WC_STATUS_EXTERNAL`**(int)

Неверсіонований шлях, що заповнюється з використанням svn:externals

**`SVN_WC_STATUS_INCOMPLETE`**(int)

Директорія не містить повного списку записів

**Константи типу Node**

**`SVN_NODE_NONE`**(int)

Відсутнє

**`SVN_NODE_FILE`**(int)

Файл

**`SVN_NODE_DIR`**(int)

Директорія

**`SVN_NODE_UNKNOWN`**(int)

Щось, що не ідентифікується Subversion
