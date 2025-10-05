# 🌐 Multiplayer — Çok Oyunculu Mekanikler

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Multiplayer  
**Amaç:** Oyunun co-op ve PvP modlarını analiz etmek, oyuncu senkronizasyonunu ve UE5’te uygulanacak multiplayer sistemlerini planlamak.

---

## 🕹️ Multiplayer Mekaniklerinin Özeti

Oyuncular, çevrimiçi modda birlikte veya birbirlerine karşı mücadele eder:

- **Co-op Mode:**  
  - 2–4 oyuncu birlikte zombi dalgalarına karşı savunma yapar  
  - Taret yerleştirme, barikat kurma ve kaynak paylaşımı takım olarak yapılır  

- **PvP Deathmatch Mode:**  
  - Oyuncular birbirlerine karşı savaşır  
  - Skor tabloları ve harita kontrollü ölüm sayıları ile oynanır  

- **Eşya ve Kaynak Yönetimi:**  
  - Co-op modda kaynaklar ve yükseltmeler oyuncular arasında senkronize edilir  
  - PvP’de pickup’lar ve silahlar oyuncular arasında adil dağıtılır  

- **Spawn ve Respawn:**  
  - Oyuncuların spawn noktaları, co-op ve PvP moduna göre farklılık gösterir  
  - Ölüm sonrası belirli süre sonra respawn

---

## 🔄 Mekanik Detaylar

- **Senkranizasyon:**  
  - Tüm oyuncu hareketleri, yerleştirdiği taretler ve barikatlar, hasar ve ölümler network üzerinden güncellenir  
- **Replication:**  
  - Oyuncu pozisyonu, silah ateşi, health ve upgrade değerleri replicated actor veya replicated variable ile güncellenir  
- **Lag Compensation:**  
  - Hit detection ve zombi spawnları, gecikme (lag) durumuna göre dengelenmeli  
- **Team Coordination:**  
  - Co-op modda yetenekler, taretler ve kaynaklar takım oyuncuları arasında uyumlu olmalı

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Co-op / PvP | `Online Subsystem` (Steam, EOS vb.) ile oyuncu eşleştirme ve oturum yönetimi |
| Actor Replication | Tüm karakterler, taretler, barikatlar ve önemli itemler `Replicated` |
| Player Stats | Health, Ammo, Upgrade Levels → `Replicated Variables` |
| Spawn / Respawn | Blueprint → Spawn Point Array + Respawn Timer |
| Hit / Damage | `Server-Side Hit Validation` ile güvenli damage uygulaması |
| UI / HUD | Widget Blueprint → Scoreboard, Team Status, Player List, Chat |

---

## 💡 Geliştirme Notları

- Co-op modda oyuncuların kaynak paylaşımı ve upgrade senkronizasyonu kritik  
- PvP’de lag compensation ve server-side validation ile adil oyun sağlanmalı  
- Multiplayer testleri her zaman düşük ve yüksek ping simülasyonlarıyla yapılmalı  
- UI, oyuncuların takım durumunu ve kritik bilgileri net göstermeli

---

## 📌 Özet

> Multiplayer.md, oyunun co-op ve PvP modlarını, oyuncu senkronizasyonunu ve network sistemlerini detaylandırır.  
> Unreal Engine 5’te Online Subsystem, Replication ve Blueprint tabanlı sistemler ile prototiplenebilir, optimize edilebilir ve test edilebilir.

