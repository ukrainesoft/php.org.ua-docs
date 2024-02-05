---
navigation:
  - class.ui-draw-stroke.md: « UI\\Draw\\Stroke
  - ui-draw-stroke.getcap.md: 'UI\\Draw\\Stroke::getCap »'
  - index.md: PHP Manual
  - class.ui-draw-stroke.md: UI\\Draw\\Stroke
title: 'UI\\Draw\\Stroke::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# UI\\Draw\\Stroke::\_\_construct

(UI 0.9.9)

UI\\Draw\\Stroke::\_\_construct — Створити новий об'єкт Stroke

### Опис

public**UI\\Draw\\Stroke::\_\_construct**  
int`$cap`\= UI\\Draw\\Line\\Cap::Flat,  
int`$join`\= UI\\Draw\\Line\\Join::Miter,  
float`$thickness`  
float`$miterLimit`  
) .

Створює новий об'єкт Stroke

### Список параметрів

`cap`

UI\\Draw\\Line\\Cap::Flat, UI\\Draw\\Line\\Cap::Round або UI\\Draw\\Line\\Cap::Square

`join`

UI\\Draw\\Line\\Join::Miter, UI\\Draw\\Line\\Join::Round або UI\\Draw\\Line\\Join::Bevel

`thickness`

Товщина обведення

`miterLimit`

Межа зрізу (за замовчуванням підходить для всіх підтримуваних платформ)
