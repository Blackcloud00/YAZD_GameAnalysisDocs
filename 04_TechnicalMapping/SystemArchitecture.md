# 🏗️ System Architecture — Sistem Mimarisi

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Technical Mapping → SystemArchitecture  
**Amaç:** Oyunun genel yazılım mimarisini ve sistemler arasındaki ilişkileri Unreal Engine 5 perspektifinden detaylandırmak.

---

## 🌌 Genel Mimarisi

- **Minimalist alan ve tek ışık kaynağı** nedeniyle oyun, basit ve performans odaklı bir mimariye sahip.  
- Sistemler modüler ve Blueprint tabanlı, Event Dispatchers ve Bindings ile birbirine bağlı.  
- Multiplayer veya co-op mod düşünülerek replication ve network yapılandırmaları dahil edilmiştir.

---

## 🔄 Temel Sistemler ve İlişkileri

1. **GameMode**
   - Oyun kurallarını yönetir: Dalga sayısı, skor, oyun sonu koşulları.  
   - İlgili sistemler: WaveController, PlayerController, GameState.

2. **GameState**
   - Global oyun durumu ve oyuncu verilerini tutar.  
   - Replication ile multiplayer için senkronizasyon sağlar.  
   - Örnek değişkenler: CurrentWave, AliveEnemies, Score.

3. **PlayerController**
   - Oyuncu girişlerini işler: Hareket, saldırı, pickup, menü navigasyonu.  
   - PlayerPawn ile bağlanır ve HUD/UI üzerinden bilgi günceller.

4. **PlayerPawn / Character**
   - Oyuncunun sahnedeki temsili.  
   - Components: Movement, Health, Inventory, Weapon System.  
   - Events → InputAction, OnOverlap, Event Dispatcher ile UI ve diğer sistemlere bağlanır.

5. **Enemy AI**
   - AIController + Behavior Tree + Blackboard ile hedef takip ve saldırı.  
   - WaveController ile spawn ve dalga yönetimi sağlanır.  

6. **WaveController**
   - Dalga ve spawn yönetimi.  
   - Enemy AI spawn → Enemy Death → Wave Clear Check → Next Wave.  

7. **Turret / Barriers**
   - Actor Blueprint → Attack Component + Health Component.  
   - Player Inventory ve HUD ile senkronize.  

8. **Pickup Items**
   - Actor Blueprint → Collision Component → Inventory Update + Feedback Event.  

9. **HUD / UI**
   - Player ve GameState değişkenleri ile bind edilmiş tüm görsel ve sesli feedback öğeleri.  
   - Health, Ammo, Score, Wave, Inventory ve Feedback sistemleri burada yönetilir.

---

## ⚙️ Sistem İlişkileri Görselleştirme (Örnek)


---

## 💡 Geliştirme Notları

- Blueprint tabanlı sistemler modüler ve bağımsız test edilebilir olmalı.  
- Event Dispatchers ile Player ↔ UI ↔ WaveController ↔ EnemyAI etkileşimi sağlanmalı.  
- Multiplayer veya co-op mod için replication kritik; GameState ve PlayerState her oyuncuya ayrı ve senkronize olmalı.  
- Minimalist alan ve tek ışık kaynağı sayesinde performans optimizasyonu daha kolay sağlanabilir.

---

## 📌 Özet

> SystemArchitecture.md, Yet Another Zombie Defense oyununun genel yazılım mimarisini ve sistemler arasındaki ilişkileri Unreal Engine 5 perspektifinden detaylandırır.  
> Modüler Blueprint yapısı ve Event Dispatcher ile oyun mekanikleri, UI ve multiplayer sistemleri birbirine entegre edilmiştir.
