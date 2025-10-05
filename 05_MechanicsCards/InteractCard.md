# 🛠️ Interact Card — Etkileşim Mekanikleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Mechanics Cards → Interact  
**Amaç:** Oyuncunun pickup, taret ve barikat yerleştirme sistemlerini hızlıca referans alabileceğimiz şekilde özetlemek.

---

## 🌌 Etkileşim Mekanikleri

- **Pickup Items:** Sağlık, ammo veya kaynak itemleri.  
- **Turret / Barricade Placement:** Oyuncu envanterindeki taret ve barikatları sahaya yerleştirebilir.  
- **Contextual Interaction:** Özel objelerle (kapılar, itemler) etkileşim.  

---

## 🔄 Parametreler

| Özellik | Değer / Açıklama |
|---------|----------------|
| Pickup Range | 200 units |
| Pickup Cooldown | 0.5 s |
| Turret Placement Range | 300 units from player |
| Barricade Placement Range | 300 units from player |
| Max Active Turrets | 3 |
| Max Active Barricades | 3 |

---

## ⚙️ UE5 Blueprint Uygulaması

- **Pickup Actor** → Collision Component + OnOverlap Event → Add to Inventory / Heal / Ammo.  
- **Turret / Barricade Actor** → Placement Component + Health / Attack Component.  
- **Input Bindings** → PlaceTurret, PlaceBarricade, Interact.  
- **HUD / Inventory Binding** → Seçilen taret/barikat türünü göstermek için.  
- **Feedback** → Pickup veya yerleştirme sırasında UI animasyonları ve ses efektleri.  
- **Replication** → Multiplayer için pickup ve placement state senkronize edilmelidir.

---

## 💡 Notlar

- Pickup ve yerleştirme mekanikleri, gameplay stratejisini doğrudan etkiler.  
- Turret ve barikat yerleştirme arayüzü, hızlı ve sezgisel olmalıdır.  
- Multiplayer modda tüm oyuncular için eşzamanlı state yönetimi kritik.  

---

## 📌 Özet

> InteractCard.md, oyuncunun pickup itemleri, taret ve barikat yerleştirme mekaniklerini, parametrelerini ve Unreal Engine 5’teki implementasyon detaylarını hızlı bir referans kartı olarak sunar.
