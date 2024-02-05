---
navigation:
  - yar-client-exception.gettype.md: '« Yar\_Client\_Exception::getType'
  - intro.xmlrpc.md: Вступ "
  - index.md: PHP Manual
  - refs.webservice.md: Веб-сервіси
title: XML-RPC
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XML-RPC

-   [Вступ](intro.xmlrpc.md)
-   [Встановлення та налаштування](xmlrpc.setup.md)
    -   [Вимоги](xmlrpc.requirements.md)
    -   [Установка](xmlrpc.installation.md)
    -   [Налаштування під час виконання](xmlrpc.configuration.md)
    -   [Типи ресурсів](xmlrpc.resources.md)
-   [Обумовлені константи](xmlrpc.constants.md)
-   [Функції XML-RPC](ref.xmlrpc.md)
    -   [xmlrpc\_decode\_request](function.xmlrpc-decode-request.md) \- Декодує XML у нативні типи PHP
    -   [xmlrpc\_decode](function.xmlrpc-decode.md) \- Декодує XML у нативні типи PHP
    -   [xmlrpc\_encode\_request](function.xmlrpc-encode-request.md) \- Генерує XML для методу запиту
    -   [xmlrpc\_encode](function.xmlrpc-encode.md) \- Генерує XML для PHP значення
    -   [xmlrpc\_get\_type](function.xmlrpc-get-type.md)— Отримує тип XML-RPC для значення PHP
    -   [xmlrpc\_is\_fault](function.xmlrpc-is-fault.md)— Визначає, чи є масив значень уявленням помилки XMLRPC
    -   [xmlrpc\_parse\_method\_descriptions](function.xmlrpc-parse-method-descriptions.md)— Декодує XML до списку описів методів
    -   [xmlrpc\_server\_add\_introspection\_data](function.xmlrpc-server-add-introspection-data.md) \- Додає документацію самоаналізу
    -   [xmlrpc\_server\_call\_method](function.xmlrpc-server-call-method.md)— Розбирає XML-запити та методи, що викликають.
    -   [xmlrpc\_server\_create](function.xmlrpc-server-create.md)— Створює сервер XML-RPC
    -   [xmlrpc\_server\_destroy](function.xmlrpc-server-destroy.md)— Знищує серверні ресурси
    -   [xmlrpc\_server\_register\_introspection\_callback](function.xmlrpc-server-register-introspection-callback.md)— Реєструє функцію PHP для створення документації
    -   [xmlrpc\_server\_register\_method](function.xmlrpc-server-register-method.md)— Реєструє функцію PHP до методу ресурсу, що відповідає методу\_name
    -   [xmlrpc\_set\_type](function.xmlrpc-set-type.md)— Встановлює тип XML-RPC, base64 або datetime для значення рядка PHP
