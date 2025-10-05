# 🎒 Inventory — Oyuncu Envanteri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** UI/UX → Inventory  
**Amaç:** Oyuncunun sahip olduğu silahlar, taretler, barikatlar ve pickup itemlerini görüntüleyip yönetebileceği envanter sistemini detaylandırmak.

---

## 🌌 Inventory Konsepti

- **Minimalist ve hızlı erişilebilir:** Oyuncu tek alan ve tek ışık kaynağı ile oynadığından, inventory ekranı oyun akışını kesmeden hızlı erişim sunmalı.  
- **Odak Noktası:** Silah, taret ve barikat seçimleri; pickup itemleri ve kaynak durumu.  

---

## 🔄 Inventory Öğeleri

1. **Weapons**  
   - Oyuncunun sahip olduğu silahlar listelenir.  
   - Seçim yapılabilir ve kısa tooltip ile damage, fire rate gibi bilgiler gösterilir.  

2. **Turrets / Barriers**  
   - Yerleştirilebilir taretler ve barikatlar.  
   - Stok durumu ve yerleştirme tuşları ile birlikte gösterilir.  

3. **Pickup Items**  
   - Sağlık kitleri, ammo veya ekstra kaynaklar.  
   - Ekranın bir köşesinde küçük ikonlar veya slotlar halinde gösterilir.  

4. **Quick Access / Hotkeys**  
   - Hızlı kullanım için tuş atamaları (1-4 veya mouse wheel)  
   - Ekranda ikon ile aktif item gösterilir.  

---

## ⚙️ UE5 Tasarım Önerileri

| Inventory Öğesi | Unreal Engine 5 Uygulaması |
|-----------------|---------------------------|
| Weapons / Turrets | UMG Widget → Grid Panel veya Horizontal Box → Bind Player Inventory Array |
| Pickup Items | UMG Image / Icon → Bind Item Quantity / Status |
| Tooltip | `TextBlock` veya `Border + Text` → Mouse Hover veya Controller Focus Event |
| Quick Access | UMG Widget + Hotkey Bindings → Switch Item / Turret Blueprint |
| Update System | Inventory değişiklikleri için Event Dispatcher veya Bind Widget → PlayerState veya Inventory Component |

---

## 💡 Geliştirme Notları

- Minimalist tasarım, oyuncunun hızlı seçim yapmasını sağlamalı.  
- Inventory öğeleri, hızlı görsel algı ve kontrol için ikon ve kısa bilgi göstermeli.  
- Hotkey ve hızlı erişim sistemi, oyuncu eylemlerini kesintisiz desteklemeli.  
- Multiplayer modda inventory durumu her oyuncuya ayrı ve senkronize gösterilmeli.  

---

## 📌 Özet

> Inventory.md, oyuncunun sahip olduğu silahlar, taretler, barikatlar ve pickup itemlerini görüntüleyip yönetebileceği minimalist ve hızlı erişilebilir envanter sistemini detaylandırır.  
> Unreal Engine 5’te UMG Widget Blueprint, Bindings ve Event Dispatcher kullanımıyla prototiplenebilir ve dinamik hale getirilebilir.
