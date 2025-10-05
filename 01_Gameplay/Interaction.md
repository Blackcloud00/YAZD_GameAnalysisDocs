# 🤝 Interaction — Oyuncu Etkileşimleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Interaction  
**Amaç:** Oyuncunun oyun dünyasıyla nasıl etkileşime girdiğini analiz etmek ve Unreal Engine 5’te yeniden tasarlarken rehber olarak kullanmak.

---

## 🕹️ Etkileşim Mekaniklerinin Özeti

Oyuncu, hayatta kalabilmek için çevresindeki ortamla çeşitli şekillerde etkileşime geçer:

- **Barikat Yerleştirme:**  
  - Önceden belirlenmiş noktalara veya serbest alanlara savunma engelleri kurulur  
- **Taret Kurma:**  
  - Otomatik ateş eden taretler stratejik noktalara yerleştirilir  
- **Eşya / Loot Toplama:**  
  - Oyuncu, silah, sağlık kitleri veya kaynakları toplar  
- **UI Tabanlı Etkileşimler:**  
  - Inventory, skill menu, upgrade screen gibi menülerle etkileşim  
- **Diğer Oyuncularla Etkileşim (Co-op):**  
  - Eşyaları paylaşma veya takım stratejisi belirleme

---

## 🔄 Mekanik Detaylar

- **Placement Mechanics:**  
  - Barikat ve taretler belirli grid veya free placement sistemiyle yerleştirilir  
  - Çarpışma kontrolü yapılır; çakışma varsa yerleştirme engellenir  

- **Pickup Mechanics:**  
  - Oyuncu menzil içindeki eşyaları toplar (`Pickup Range` karakter özelliğine bağlı)  
  - Toplanan itemler envantere veya anlık statlara eklenir  

- **UI Feedback:**  
  - Etkileşim sırasında görsel ve sesli geri bildirim verilir  
  - Örnek: Barikat yerleştirildiğinde “place sound” ve highlight efekti  

- **Co-op Etkileşimi:**  
  - Eşya ve taret yerleştirme, diğer oyuncularla senkronize edilmelidir  
  - Multiplayer için `Replicated Actors` kullanımı gerekir

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Barikat / Taret Placement | Blueprint Actor → `Collision Check` + `SetActorLocation` |
| Pickup Item | Blueprint Actor → `SphereOverlapActors` + `AddToInventory` veya stat update |
| UI Etkileşimleri | Widget Blueprint → Inventory, Upgrade, Menu sistemleri |
| Etkileşim Geri Bildirimi | `Niagara` particles + `AudioComponent` + Highlight Material |
| Multiplayer | `Replicated Variables` ve `Replicate Movement` ile etkileşimlerin tüm oyunculara yansıtılması |

---

## 💡 Geliştirme Notları

- Etkileşimlerin hızlı ve sezgisel olması oyuncu deneyimi için kritik  
- Yerleştirme ve pickup sistemleri, karakter upgrades (pickup range, movement speed) ile uyumlu olmalı  
- Co-op modda çakışma ve senkronizasyon dikkatlice test edilmeli  
- UI üzerinden yapılan etkileşimler, görsel olarak anlaşılır ve geri bildirimi güçlü olmalı

---

## 📌 Özet

> Interaction.md, oyuncunun çevre ve oyun dünyasıyla kurduğu temel etkileşimleri detaylandırır.  
> Unreal Engine 5’te Blueprint tabanlı Actor’lar, UI widget’ları ve multiplayer replication ile prototiplenebilir ve optimize edilebilir.
