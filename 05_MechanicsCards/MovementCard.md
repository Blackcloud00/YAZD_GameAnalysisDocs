# 🏃 Movement Card — Oyuncu Hareket Mekanikleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Mechanics Cards → Movement  
**Amaç:** Oyuncunun hareket sistemini hızlıca referans alabileceğimiz şekilde özetlemek.

---

## 🌌 Hareket Mekanikleri

- **Yönlü Hareket:** W/A/S/D veya analog stick ile kontrol edilir.  
- **Sprint:** Shift tuşu ile kısa süreli hız artışı.  
- **Rotation / Facing:** Mouse veya right stick ile yön değişimi.  
- **Jump / Vault:** Opsiyonel; basit engeller üzerinden geçiş için.  

---

## 🔄 Parametreler

| Özellik | Değer / Açıklama |
|---------|----------------|
| Base Speed | 600 units/s |
| Sprint Speed | 900 units/s |
| Acceleration | 2048 units/s² |
| Deceleration | 2048 units/s² |
| Rotation Rate | 720 degrees/s |
| Jump Height | 300 units |
| Gravity | 980 units/s² |

---

## ⚙️ UE5 Blueprint Uygulaması

- **Character Movement Component** → Speed, Acceleration, Jump settings.  
- **Input Bindings** → MoveForward, MoveRight, Sprint, Jump.  
- **Animation Blueprint** → Walk, Run, Idle blend.  
- **Network Replication** → Multiplayer için Movement Component replication aktif.  

---

## 💡 Notlar

- Tek alanlı oyun ve minimal ışık ile hareket oyuncunun odak noktasını korumalı.  
- Sprint mekanizması strateji için sınırlı kaynak veya cooldown ile bağlanabilir.  
- Multiplayer modda tüm hareketler senkronize olmalı; latency ve prediction optimizasyonu önemli.

---

## 📌 Özet

> MovementCard.md, oyuncunun temel hareket mekaniklerini, parametrelerini ve Unreal Engine 5’teki implementasyon detaylarını hızlı bir referans kartı olarak sunar.
