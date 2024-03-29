---
navigation:
  - function.yaz-hits.md: « yaz\_hits
  - function.yaz-present.md: yaz\_present »
  - index.md: PHP Manual
  - ref.yaz.md: Функції YAZ
title: yaz\_itemorder
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# yaz\_itemorder

(PHP 4 >= 4.0.5, PECL yaz >= 0.9.0)

yaz\_itemorder — Підготовка запиту до Z39.50 Item Order з пакетом ILL-Request

### Опис

```methodsynopsis
yaz_itemorder(resource $id, array $args): void
```

Функция подготавливает запрос Extended Services с использованием профиля для использования Item Order Extended Service для Transport ILL (Profile/1). Смотрите[» це](http://www.collectionscanada.ca/iso/ill/stanprf.htm) і [» специфікацію](http://www.collectionscanada.ca/iso/ill/document/standard/z-ill-1a.pdf)

### Список параметрів

`id`

Ресурс підключення, що повертається [yaz\_connect()](function.yaz-connect.md)

`args`

Повинен бути асоціативним масивом з інформацією про запит Item Order. Ключ хеша – це ім'я відповідного шляху тегу ASN.1. Наприклад, у ISBN під Item-ID буде ключ item-id, ISBN.

Параметри ILL-запиту:

protocol-version-num transaction-id,initial-requester-id,person-or-institution-symbol,person transaction-id,initial-requester-id,person-or-institution-symbol,institution transaction-id,initial-requester-id,name-of-person-or-institution,name-of-person transaction-id,initial-requester-id,name-of-person-or-institution,name-of-institution transaction-id,transaction-group-qualifier transaction-id,transaction-qualifier transaction-id,sub-transaction-qualifier service-date-time,this,date service-date-time,this,time service-date-time,original,date service-date-time,original,time requester-id,person-or-institution-symbol,person requester-id,person-or-institution-symbol,institution requester-id,name-of-person-or-institution,name-of-person requester-id,name-of-person-or-institution,name-of-institution responder-id,person-or-institution-symbol,person responder-id,person-or-institution-symbol,institution responder-id,name-of-person-or-institution,name-of-person responder-id,name-of-person-or-institution,name-of-institution transaction-type delivery-address,postal-address,name-of-person-or-institution,name-of-person delivery-address,postal-address,name-of-person-or-institution,name-of-institution delivery-address,postal-address,extended-postal-delivery-address delivery-address,postal-address,street-and-number delivery-address,postal-address,post-office-box delivery-address,postal-address,city delivery-address,postal-address,region delivery-address,postal-address,country delivery-address,postal-address,postal-code delivery-address,electronic-address,telecom-service-identifier delivery-address,electronic-address,telecom-service-addreess billing-address,postal-address,name-of-person-or-institution,name-of-person billing-address,postal-address,name-of-person-or-institution,name-of-institution billing-address,postal-address,extended-postal-delivery-address billing-address,postal-address,street-and-number billing-address,postal-address,post-office-box billing-address,postal-address,city billing-address,postal-address,region billing-address,postal-address,country billing-address,postal-address,postal-code billing-address,electronic-address,telecom-service-identifier billing-address,electronic-address,telecom-service-addreess ill-service-type requester-optional-messages,can-send-RECEIVED requester-optional-messages,can-send-RETURNED requester-optional-messages,requester-SHIPPED requester-optional-messages,requester-CHECKED-IN search-type,level-of-service search-type,need-before-date search-type,expiry-date search-type,expiry-flag place-on-hold client-id,client-name client-id,client-status client-id,client-identifier item-id,item-type item-id,call-number item-id,author item-id,title item-id,sub-title item-id,sponsoring-body item-id,place-of-publication item-id,publisher item-id,series-title-number item-id,volume-issue item-id,edition item-id,publication-date item-id,publication-date-of-component item-id,author-of-article item-id,title-of-article item-id,pagination item-id,ISBN item-id,ISSN item-id,additional-no-letters item-id,verification-reference-source copyright-complicance retry-flag forward-flag requester-note forward-note

Є також кілька параметрів, які є частиною пакетів запиту Extended Services та ItemOrder:

package-name user-id contact-name contact-phone contact-email itemorder-item

### Значення, що повертаються

Функція не повертає значення після виконання.
