# 🏃 Movement — Oyuncu Hareket Mekanikleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Movement  
**Amaç:** Oyuncu karakterinin hareket mekaniklerini analiz etmek ve Unreal Engine 5’te yeniden tasarlarken rehber olarak kullanmak.

---

## 🕹️ Hareket Mekaniklerinin Özeti

Oyuncu, hayatta kalabilmek için çevresinde serbestçe hareket eder:

- **Top-Down Perspektif:**  
  - Üstten görünüm (top-down) ile tüm çevre gözlemlenebilir  
- **Temel Hareket:**  
  - Yürümek / Koşmak, 8 yönlü veya analog stick hareketi  
- **Sprint / Speed Boost:**  
  - Geçici hız artışı (Abilities.md ile ilişkili)  
- **Engel / Çarpışma Kontrolü:**  
  - Barikatlar, taretler veya çevre objeleri ile çarpışma kontrolü  
- **Animation / Feedback:**  
  - Yön ve hız ile uyumlu animasyon ve particle/efektler

---

## 🔄 Mekanik Detaylar

- **Hareket Hızı (Movement Speed):**  
  - Karakterin temel hızı, seviye ve upgrade ile artabilir  
- **Dönüş / Yön Kontrolü:**  
  - Fare veya analog stick ile yön belirleme  
  - Yön, animasyon ve taret hedeflemesi ile uyumlu olmalı  
- **Zıplama / Engel Atlama (Opsiyonel):**  
  - Eğer oyun mekaniği varsa küçük engeller üzerinden geçiş  
- **Geri Tepme / Knockback Etkileri:**  
  - Düşman saldırıları veya patlayıcılar hareketi etkileyebilir

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Hareket & Input | `CharacterMovementComponent` + `Input Mapping` (WASD veya analog stick) |
| Sprint / Speed Boost | `MaxWalkSpeed` geçici modifikasyonu → Timer veya Ability trigger |
| Çarpışma | `CapsuleComponent` + `Collision Channels` ile çarpışma kontrolü |
| Animasyon | `AnimBlueprint` → Yön ve hız ile blend space animasyonları |
| Knockback / Geri Tepme | `LaunchCharacter` veya impulse ile hareket etkisi uygulama |
| Top-Down Kamera | `SpringArm` + `Camera` → sabit veya karakteri takip eden üstten görünüm |

---

## 💡 Geliştirme Notları

- Top-down hareket, oyuncuya çevreyi tam gözlemleme imkanı verir; navigasyon kolay olmalı  
- Movement speed ve sprint mekanikleri karakter upgrades ile uyumlu olmalı  
- Knockback veya patlama etkileri, oyuncuya net görsel/işitsel geri bildirim sağlamalı  
- Multiplayer’da movement replication ile senkronizasyon sağlanmalı

---

## 📌 Özet

> Movement.md, oyuncu karakterinin hareket mekaniklerini ve kamera sistemini detaylandırır.  
> Unreal Engine 5’te `CharacterMovementComponent`, AnimBlueprint ve Blueprint tabanlı input sistemi ile prototiplenebilir ve optimize edilebilir.
