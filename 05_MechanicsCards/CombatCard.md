# 🔫 Combat Card — Oyuncu Savaş Mekanikleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Mechanics Cards → Combat  
**Amaç:** Oyuncunun saldırı sistemini ve silah mekaniklerini hızlıca referans alabileceğimiz şekilde özetlemek.

---

## 🌌 Silah ve Saldırı Mekanikleri

- **Primary Weapon:** Fire tuşu ile ateş edilir.  
- **Secondary Weapon / Turret:** Yerleştirilebilir otomatik saldırı birimleri.  
- **Melee Attack:** Opsiyonel; yakın dövüş veya backup silah.  
- **Reload:** Her silah için reload süresi ve animasyonu bulunur.  

---

## 🔄 Parametreler

| Özellik | Değer / Açıklama |
|---------|----------------|
| Damage | 10 – 50 (Silah tipine göre değişir) |
| Fire Rate | 0.2 – 1.0 s / shot |
| Reload Time | 1 – 3 s |
| Magazine Size | 6 – 30 rounds |
| Range | 500 – 2000 units |
| Spread / Accuracy | %5 – %15 |

---

## ⚙️ UE5 Blueprint Uygulaması

- **Weapon Actor / Component** → Damage, FireRate, Reload, Ammo yönetimi.  
- **Input Bindings** → Fire, Reload.  
- **Animation Blueprint** → Fire, Reload, Idle blend.  
- **Projectile / HitScan** → Damage uygulama ve enemy hit detection.  
- **Event Dispatcher** → HUD / Feedback binding (Ammo display, hit markers).  
- **Replication** → Multiplayer için projectile ve damage replication aktif.

---

## 💡 Notlar

- Taret ve barikat sistemi combat mekaniklerine entegre olmalı.  
- Silahlar oyuncu stratejisine göre farklı damage ve fire rate değerlerine sahip olmalı.  
- Multiplayer modda damage ve ammo durumu tüm oyuncular için senkronize edilmeli.

---

## 📌 Özet

> CombatCard.md, oyuncunun silah, saldırı ve damage mekaniklerini, parametrelerini ve Unreal Engine 5’teki implementasyon detaylarını hızlı bir referans kartı olarak sunar.
