# 🤖 Enemy AI Card — Düşman Yapay Zekâ Mekanikleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Mechanics Cards → EnemyAI  
**Amaç:** Düşman AI davranışlarını ve saldırı mantığını hızlıca referans alabileceğimiz şekilde özetlemek.

---

## 🌌 AI Mekanikleri

- **Targeting:** Oyuncuyu tespit edip takip eder.  
- **Movement:** Basit pathfinding ve collision avoidance ile oyuncuya yaklaşır.  
- **Attack:** Yakın veya menzilli saldırı, damage uygular.  
- **Death / Feedback:** Ölünce skor ve feedback tetiklenir.  

---

## 🔄 Parametreler

| Özellik | Değer / Açıklama |
|---------|----------------|
| Health | 50 – 200 |
| Damage | 5 – 25 |
| Speed | 300 – 500 units/s |
| Detection Range | 1000 units |
| Attack Rate | 1.0 – 2.0 s / attack |
| Spawn Wave | Dalga numarasına göre artar |

---

## ⚙️ UE5 Blueprint Uygulaması

- **AIController + Behavior Tree + Blackboard** → Hedef takibi, saldırı ve pathfinding.  
- **Events:** OnSeePlayer, OnHearNoise, OnTakeDamage, OnDeath.  
- **Blackboard Keys:** TargetActor, IsAttacking, CurrentWaypoint.  
- **Event Dispatcher:** HUD veya WaveController ile ölüm ve skor feedback’i için.  
- **Replication:** Multiplayer veya co-op modda AI durumu tüm oyuncular için senkronize edilir.

---

## 💡 Notlar

- Dalga sistemi ile spawn ve güç dengesi kontrol edilmeli.  
- AI basit ama stratejik olarak oyuncuyu zorlamalı.  
- Multiplayer modda replication ve network optimizasyonu kritik.  

---

## 📌 Özet

> EnemyAICard.md, düşmanların temel AI davranışlarını, saldırı mantığını ve Unreal Engine 5 implementasyon detaylarını hızlı bir referans kartı olarak sunar.
