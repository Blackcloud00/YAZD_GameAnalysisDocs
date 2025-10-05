# 🔹 Blueprint Mapping — Blueprint Sistemi

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Technical Mapping → BlueprintMapping  
**Amaç:** Oyundaki temel sistemlerin Unreal Engine 5 Blueprint yapısını ve akışını detaylandırmak.

---

## 🌌 Blueprint Sistemi Konsepti

- Minimalist alan ve tek ışık kaynağı nedeniyle Blueprint’ler basit, modüler ve performans odaklı olmalı.  
- Her sistem kendi Blueprint veya Component’ine sahip olacak ve Event Dispatchers veya Bindings ile birbirine bağlanacak.  

---

## 🔄 Önemli Blueprintler ve Akış

1. **Player Character Blueprint**
   - **Components:** Movement, Health, Inventory, Weapon System  
   - **Events:**  
     - `InputAxis MoveForward/MoveRight` → Hareket  
     - `InputAction Fire` → Silah Ateşi  
     - `OnOverlap Pickup` → Pickup toplama  
   - **Bindings:** HUD, Inventory, Feedback  

2. **Enemy AI Blueprint**
   - **Components:** AIController, Blackboard, Behavior Tree  
   - **Logic:**  
     - `TargetPlayer` → Pursuit  
     - `AttackPlayer` → Damage Player  
     - `OnDeath` → Score Update + Feedback  

3. **WaveController Blueprint**
   - **Components:** Timer, Spawn Points Array, Wave Data Structure  
   - **Logic:**  
     - `StartWave` → Spawn Enemy → Increment Wave  
     - `CheckWaveClear` → Next Wave or End Game  
     - `OnEnemyDeath` → Wave Enemy Count Update  

4. **Turret / Barricade Blueprint**
   - **Components:** Attack Component, Health Component, Mesh  
   - **Logic:**  
     - `PlaceTurret` → Activate Attack Logic  
     - `OnDestroy` → Remove from Inventory + Feedback  
     - Bind HUD ammo / durability  

5. **Pickup Blueprint**
   - **Components:** Collision Component, Mesh, Pickup Type Variable  
   - **Events:**  
     - `OnOverlap` → Add to Player Inventory / Heal / Ammo  
     - Feedback Event → Floating Text + Sound  

6. **HUD & UI Blueprint**
   - **Components:** Health Bar, Ammo, Wave, Score, Inventory  
   - **Logic:** Bind to Player Character and GameState variables via Event Dispatcher  
   - Feedback animations: Damage pulse, pickup flash, kill points  

---

## ⚙️ Blueprint Etkileşimleri

- **Player ↔ HUD:** Event Dispatcher → Can, Ammo, Pickup  
- **Player ↔ Inventory:** Bind → Weapon / Turret selection  
- **WaveController ↔ Enemy AI:** Spawn Event → AI Init → Blackboard target  
- **Pickup ↔ Player:** OnOverlap → Inventory Update → HUD Feedback  
- **Turret ↔ Enemy:** Attack Event → Damage Player → Feedback  

---

## 💡 Geliştirme Notları

- Blueprint’ler modüler olmalı; her sistem bağımsız test edilebilmeli.  
- Event Dispatchers ile UI ve Gameplay sistemi arasında dinamik ve senkron iletişim sağlanmalı.  
- Multiplayer veya co-op modlarda replication ayarları kritik; AI ve Player state her oyuncu için senkronize edilmeli.  
- Placeholder assetler ile prototip testleri yapıldıktan sonra görsel ve sesler entegre edilmeli.  

---

## 📌 Özet

> BlueprintMapping.md, Yet Another Zombie Defense oyununda Player, Enemy, WaveController, Turret/Barikade ve Pickup sistemlerinin Blueprint yapısını ve etkileşim akışını detaylandırır.  
> Blueprint tabanlı modüler tasarım, prototipleme ve performans optimizasyonu için rehber niteliğindedir.
