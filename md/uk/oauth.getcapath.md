Отримати інформацію CA

-   [« OAuth::getAccessToken](oauth.getaccesstoken.html)
    
-   [OAuth::getLastResponse »](oauth.getlastresponse.html)
    
-   [PHP Manual](index.html)
    
-   [OAuth](class.oauth.html)
    
-   Отримати інформацію CA
    

# OAuth::getCAPath

(PECL OAuth >= 0.99.8)

OAuth::getCAPath — Отримати інформацію CA

### Опис

```methodsynopsis
public OAuth::getCAPath(): array
```

Повертає інформацію про центр сертифікації, що включає capath та cainfo, встановлені [OAuth::setCaPath()](oauth.setcapath.html)

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Асоціативний масив з інформацією про центр сертифікації з ключами `ca_path` і `ca_info`

### Дивіться також

-   [OAuth::setCAPath()](oauth.setcapath.html) - Встановити CA для шляху та інформації
-   [OAuth::getLastResponseInfo()](oauth.getlastresponseinfo.html) - Отримати HTTP-інформацію про останню відповідь