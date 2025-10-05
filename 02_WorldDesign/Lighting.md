# 💡 Lighting — Işıklandırma ve Atmosfer

**Oyun:** Yet Another Zombie Defense  
**Kategori:** WorldDesign → Lighting  
**Amaç:** Minimalist oyun alanında, tek sokak lambasının ışıklandırmasını ve atmosfer tasarımını detaylandırmak.

---

## 🌌 Oyun Alanı Konsepti

- **Tek Işık Kaynağı:**  
  - Alanın merkezinde tek bir sokak lambası bulunur.  
  - Oyuncu ve düşmanlar bu ışığın etkisi altında hareket eder.  

- **Atmosfer:**  
  - Minimalist tasarım, gölge ve ışık kontrastını ön plana çıkarır.  
  - Gece ortamı ve hafif sis veya ambient light ile gerilim hissi artırılır.  

---

## 🔄 Mekanik Detaylar

- **Spot / Point Light:**  
  - Lambadan yayılan ışık, alanın merkezi ve oyuncunun stratejik hareket alanı için referans sağlar.  
  - Işık menzili ve yoğunluğu, alanın sınırlarıyla uyumlu olmalı.  

- **Shadowing:**  
  - Düşman ve objeler ışık altında gölgeler oluşturur.  
  - Dinamik gölgeler oyuncuya yön ve derinlik hissi verir.  

- **Ambient Light:**  
  - Hafif çevresel ışık (moonlight veya skyline glow) alanın tamamen kararmasını önler.  

- **Volumetric / Atmospheric Effects (Opsiyonel):**  
  - Hafif sis veya ışık hüzmesi (light shafts) ile atmosfer zenginleştirilebilir.  

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Sokak Lambası | `SpotLight` veya `PointLight` → Dinamik gölgeler + Light Intensity ve Color ayarı |
| Shadowing | Light → Cast Shadows açık, Soft Shadows ve Distance Field Shadows kullanılabilir |
| Ambient Light | `SkyLight` veya basit Directional Light → Alanın karanlık kısımlarını hafif aydınlatır |
| Volumetric Effects | `Exponential Height Fog` + Volumetric Fog Enabled → Hafif sis ve ışık hüzmesi |
| Performance | Tek ışık kaynağı ve minimal objeler performansı artırır; mobil veya düşük spec için optimize edilebilir |

---

## 💡 Geliştirme Notları

- Minimalist alan ve tek ışık kaynağı, oyuncuya odaklanma ve gerilim hissi sağlar.  
- Gölge ve ışık kontrastı, düşman yaklaşımını sezdirir ve stratejik kararları etkiler.  
- Dinamik ışık kullanımı, özellikle multiplayer veya yüksek düşman sayısında performans testleri ile optimize edilmeli.  
- Volumetric efektler opsiyoneldir; atmosferi zenginleştirir ama performansı düşürebilir.

---

## 📌 Özet

> Lighting.md, tek sokak lambasının ışıklandırmasını ve minimal alan atmosferini detaylandırır.  
> Unreal Engine 5’te Spot/Point Light, Shadowing ve optional volumetric fog kullanımıyla prototiplenebilir ve optimize edilebilir.
