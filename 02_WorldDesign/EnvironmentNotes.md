# 🌳 Environment Notes — Çevresel Tasarım

**Oyun:** Yet Another Zombie Defense  
**Kategori:** WorldDesign → Environment Notes  
**Amaç:** Minimalist oyun alanının çevresel öğelerini, stratejik objeleri ve oyuncu deneyimini detaylandırmak.

---

## 🌌 Oyun Alanı Konsepti

- **Boş Alan:** Oyun alanı neredeyse tamamen boş; oyuncunun hareketi ve stratejik yerleşimler ön planda.  
- **Sokak Lambası:** Alanın merkezinde tek bir ışık kaynağı; hem oyuncuya yön verir hem de düşman ve barikat yerleşimi için referans noktasıdır.  
- **Zemin:** Tek tip zemin mesh veya plane; basit materyal, oyuncu ve düşman kontrastını artırır.

---

## 🛠️ Stratejik Objeler

- **Barikatlar:**  
  - Oyuncu tarafından yerleştirilebilir  
  - Düşmanları yavaşlatmak veya yönlendirmek için kullanılır  
  - Alanın sınırlarına veya lambaya yakın stratejik konumlandırma önerilir  

- **Taretler:**  
  - Otomatik ateş eden savunma birimleri  
  - Lambaya veya barikatın arkasına yerleştirilebilir  
  - Spawn noktalarına göre oyuncuya avantaj sağlayacak şekilde konumlanır  

- **Pickup Itemler:**  
  - Sağlık kitleri veya ek kaynaklar  
  - Alanın çeşitli noktalarına rastgele veya sabit olarak yerleştirilebilir  

---

## 💡 Tasarım Notları

- Minimalist alan, oyuncunun strateji geliştirmesini ve hareket alanını ön plana çıkarır.  
- Sokak lambası, görsel odak ve güvenli alan referansı sağlar.  
- Barikat ve taretler, dalgaların ilerleyişine göre stratejik olarak yerleştirilmeli.  
- Zemin ve çevresel objeler, düşman ve oyuncu konumunu kolayca ayırt edilebilir kılmalı.  

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Sokak Lambası | `SpotLight` veya `PointLight` → Dinamik gölgeler, ışık renk ve yoğunluğu ayarlanabilir |
| Barikat | Blueprint Actor → Collision ve Health Component ile tahrip edilebilir objeler |
| Taret | Blueprint Actor → Fire Rate, Damage, Targeting Component |
| Pickup | Blueprint Actor → Sphere Collision + OnOverlap → Inventory veya Stat Update |
| Minimal Zemin | Static Mesh veya Plane + Basit Material → Navigation Mesh için uygun |

---

## 📌 Özet

> EnvironmentNotes.md, minimalist oyun alanının çevresel tasarımını ve stratejik objelerin yerleşimini detaylandırır.  
> Unreal Engine 5’te Blueprint tabanlı barikat, taret ve pickup sistemleri ile prototiplenebilir, ışıklandırma ve zemin materyalleri ile atmosfer optimize edilebilir.
