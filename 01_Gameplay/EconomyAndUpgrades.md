# 💰 Economy & Upgrades — Kaynak ve Geliştirme Sistemi

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Economy & Upgrades  
**Amaç:** Oyuncunun para kazanma, taret/silah geliştirme ve kaynak yönetimi mekaniklerini analiz etmek ve Unreal Engine 5’te nasıl uygulanabileceğini göstermek.

---

## 🕹️ Ekonomi Sisteminin Özeti

Oyuncu, zombi dalgalarını yendikçe **para ve kaynak kazanır**. Bu kaynaklar, savunma elemanlarını geliştirmek ve yeni yetenekler satın almak için kullanılır:

- **Para Kazanma:** Zombileri öldürmek ve görevleri tamamlamak  
- **Harcanabilir Kaynaklar:** Taretler, barikatlar, silahlar ve yetenekler  
- **Upgrade Mekanikleri:** Silah ve taret hasarı, ateş hızı, dayanıklılık gibi özelliklerin geliştirilmesi  
- **Limitler:** Kaynaklar sınırlı; oyuncu stratejik seçimler yapmak zorunda

---

## 🔄 Mekanik Detaylar

- **Taret ve Silah Upgrade:**  
  - Her taret veya silah, birkaç seviyeye kadar güçlendirilebilir  
  - Örnek: Damage +20%, Fire Rate +15%, Menzil +1 birim  

- **Kaynak Toplama ve Yönetimi:**  
  - Oyuncu kaynakları kazanır ve bunları harcayarak savunmasını güçlendirir  
  - Ekonomik kararlar hayatta kalma süresi üzerinde doğrudan etkilidir  

- **Güçlendirme Yetenekleri:**  
  - Bazı yetenekler yalnızca belirli bir miktar kaynak harcanarak açılır veya süresi artırılır  
  - Yetenekler, EconomyAndUpgrades ile bağlantılıdır (Abilities.md referansı)

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Para / Kaynak Yönetimi | `CurrencyManager` Blueprint sınıfı, oyuncuya ve taretlere kaynak atama |
| Upgrade Sistemi | Blueprint → `UpgradeComponent` veya `Struct` ile seviyeler ve değerler yönetimi |
| UI Gösterimi | Widget Blueprint → Para, taret/silah seviyeleri ve upgrade seçeneklerini görsel olarak sunma |
| Satın Alma ve Onay | Button → OnClick → Resource Check → Upgrade veya Spawn Action |
| Co-op / Multiplayer | `Replicated Variables` ile kaynakların tüm oyunculara senkronize edilmesi |

---

## 💡 Geliştirme Notları

- Upgrade maliyetleri ve etkileri **dengelemeye** dikkat edilmeli; oyuncunun çok hızlı güçlenmesi önlenmeli  
- Co-op modda kaynak paylaşımı veya takım stratejisi önemlidir  
- Gelecekte DLC veya yeni silah/taret eklemeleri kolay olmalı  
- Ekonomi sistemi, oyun döngüsünün zorluğunu ve tekrar oynanabilirliği desteklemeli  

---

## 📌 Özet

> EconomyAndUpgrades.md, oyunun kaynak yönetimi ve güçlendirme mekaniklerini detaylandırır.  
> Unreal Engine 5’te Blueprint tabanlı sistemler ve UI entegrasyonu ile prototiplenebilir, optimize edilebilir ve multiplayer modlarıyla uyumlu hale getirilebilir.
