# 💰 Economy & Upgrades — Kaynak ve Geliştirme Sistemi

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Economy & Upgrades  
**Amaç:** Oyuncunun para kazanma, taret/silah geliştirme ve karakter özelliklerini yükseltme mekaniklerini analiz etmek ve Unreal Engine 5’te nasıl uygulanabileceğini göstermek.

---

## 🕹️ Ekonomi Sisteminin Özeti

Oyuncu, zombi dalgalarını yendikçe **para ve kaynak kazanır**. Bu kaynaklar, savunma elemanlarını geliştirmek ve **oyuncu karakterinin yeteneklerini ve temel istatistiklerini yükseltmek** için kullanılır:

- **Para Kazanma:** Zombileri öldürmek ve görevleri tamamlamak  
- **Harcanabilir Kaynaklar:** Taretler, barikatlar, silahlar ve karakter upgrades  
- **Upgrade Mekanikleri:** 
  - Oyuncu karakter özellikleri:  
    - Movement Speed (Hareket Hızı)  
    - Reloading Speed (Silah Yenileme Hızı)  
    - Health Points (HP)  
    - Health Regeneration (HP Regen)  
    - Pickup Range (Eşyaları toplama menzili)  
- **Limitler:** Kaynaklar sınırlı; oyuncu stratejik seçimler yapmak zorunda

---

## 🔄 Mekanik Detaylar
- **Karakter Özellikleri Upgrade:**  
  - Level arttıkça yukarıdaki özellikler kademeli olarak yükselir  
  - Bu sayede oyuncu dalga ilerledikçe daha güçlü ve hayatta kalabilir hale gelir  

- **Kaynak Toplama ve Yönetimi:**  
  - Oyuncu kaynakları kazanır ve bunları harcayarak savunmasını ve karakterini güçlendirir  
  - Ekonomik kararlar hayatta kalma süresi üzerinde doğrudan etkilidir  

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Para / Kaynak Yönetimi | `CurrencyManager` Blueprint sınıfı, oyuncuya ve taretlere kaynak atama |
| Upgrade Sistemi | Blueprint → `UpgradeComponent` veya `Struct` ile seviyeler ve değerler yönetimi |
| Karakter Özellikleri | `Character Stats Component` ile movement speed, health, regen, reload speed, pickup range modifikasyonu |
| UI Gösterimi | Widget Blueprint → Para, taret/silah seviyeleri ve karakter upgrades’i görsel olarak sunma |
| Satın Alma ve Onay | Button → OnClick → Resource Check → Upgrade veya Spawn Action |
| Co-op / Multiplayer | `Replicated Variables` ile kaynak ve upgrade durumlarının tüm oyunculara senkronize edilmesi |

---

## 💡 Geliştirme Notları

- Karakter upgrades ve taret/silah upgrades **dengelemeye** dikkat edilmeli; oyuncunun çok hızlı güçlenmesi önlenmeli  
- Co-op modda kaynak paylaşımı veya takım stratejisi önemlidir  
- Upgrade sistemi, oyun döngüsünün zorluğunu ve tekrar oynanabilirliği desteklemeli  
- Karakter özelliklerinin kademeli yükselmesi, oyuncuya ilerleme hissi verir  

---

## 📌 Özet

> EconomyAndUpgrades.md, oyunun kaynak yönetimi, silah/taret ve karakter upgrades mekaniklerini detaylandırır.  
> Unreal Engine 5’te Blueprint tabanlı sistemler, karakter component’leri ve UI entegrasyonu ile prototiplenebilir ve multiplayer modlarıyla uyumlu hale getirilebilir.
