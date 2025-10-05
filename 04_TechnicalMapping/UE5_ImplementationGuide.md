# 🖥️ UE5 Implementation Guide — Unreal Engine 5 Implementasyon Rehberi

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Technical Mapping → UE5 Implementation Guide  
**Amaç:** Oyunun temel mekaniklerini Unreal Engine 5 ortamında nasıl implement edeceğimizi detaylandırmak.

---

## 🌌 Genel Konsept

- Oyun tek alan ve tek ışık kaynağı üzerine kuruludur.  
- Minimalist tasarım, hızlı prototipleme ve performans odaklı UE5 implementasyonu gerektirir.  
- Blueprint ve Component tabanlı yaklaşım önerilir.

---

## 🔄 Temel Sistemler ve Önerilen Blueprint Yapısı

1. **Player Controller & Pawn**  
   - Hareket, saldırı, pickup ve taret yerleştirme mekanikleri.  
   - `Character` veya `Pawn` Blueprint → Movement Component, Health Component, Inventory Component.

2. **Enemy AI**  
   - Düşmanlar basit hedef takip ve saldırı davranışına sahip.  
   - `AIController` + `Behavior Tree` + `Blackboard`.  
   - Target acquisition, pathfinding ve attack logic.

3. **Wave / Spawner System**  
   - Zombilerin dalga bazlı spawn edilmesi.  
   - `Actor` veya `Actor Component` → WaveController Blueprint.  
   - Dalga süresi, spawn interval, enemy count parametreleri.  

4. **Turret / Barricade System**  
   - Oyuncunun yerleştirdiği taret ve barikat mekanikleri.  
   - `Actor` Blueprint → Attack Component, Health Component.  
   - UI ile inventory ve placement binding.  

5. **Pickup System**  
   - Health kit, ammo, resource itemleri toplama.  
   - `Actor` Blueprint → Pickup Component, OnOverlap Event.  

6. **UI Binding**  
   - HUD, Inventory, Feedback ve Menu ile tüm game variables binding.  
   - Event Dispatcher veya Bindings ile dynamic updates.

---

## ⚙️ Blueprint & Component Önerileri

| Sistem | Blueprint / Component |
|--------|--------------------|
| Player | Character Blueprint + Movement Component + Health + Inventory |
| Enemy AI | AIController + Behavior Tree + Blackboard |
| Wave System | Actor + Timer + Spawn Logic Component |
| Turrets / Barriers | Actor + Attack Component + Health Component |
| Pickup Items | Actor + Collision Component + Pickup Event |
| HUD / UI | UMG Widget Blueprint + Bind Variables + Event Dispatcher |

---

## 💡 Geliştirme Notları

- Minimal alan ve tek ışık kaynağı performans optimizasyonunu kolaylaştırır.  
- Blueprint tabanlı sistemler modüler ve tekrar kullanılabilir olmalı.  
- Multiplayer veya co-op mod için replication ve network ayarları ayrı planlanmalı.  
- Prototip aşamasında placeholder assetler ile test edilip, gameplay mekanikleri doğrulandıktan sonra görseller entegre edilmeli.

---

## 📌 Özet

> UE5_ImplementationGuide.md, Yet Another Zombie Defense oyununun temel mekaniklerinin Unreal Engine 5’te nasıl implement edileceğini detaylandırır.  
> Blueprint ve Component tabanlı yaklaşım, prototipleme ve modüler tasarım için rehber niteliğindedir.
