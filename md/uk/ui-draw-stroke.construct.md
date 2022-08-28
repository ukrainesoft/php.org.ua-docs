Створити новий об'єкт Stroke

-   [« UI\\Draw\\Stroke](class.ui-draw-stroke.html)
    
-   [UI\\Draw\\Stroke::getCap »](ui-draw-stroke.getcap.html)
    
-   [PHP Manual](index.html)
    
-   [UI\\Draw\\Stroke](class.ui-draw-stroke.html)
    
-   Створити новий об'єкт Stroke
    

# ОЙDrawStroke::construct

(UI 0.9.9)

ОЙDrawStroke::construct — Створити новий об'єкт Stroke

### Опис

public **ОЙDrawStroke::construct**  
int `$cap` = UIDrawLineCap::Flat,  
int `$join` = UIDrawLineJoin::Miter,  
float `$thickness`  
float `$miterLimit`  

Створює новий об'єкт Stroke

### Список параметрів

`cap`

ОЙDrawLineCap::Flat, UIDrawLineCap::Round або UIDrawLineCap::Square

`join`

ОЙDrawLineJoin::Miter, UIDrawLineJoin::Round або UIDrawLineJoin::Bevel

`thickness`

Товщина обведення

`miterLimit`

Межа зрізу (за замовчуванням підходить для всіх підтримуваних платформ)