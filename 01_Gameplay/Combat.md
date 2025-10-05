# ⚔️ Combat — Dövüş Mekanikleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Combat  
**Amaç:** Oyuncunun kullandığı silahlar, taretler ve düşman etkileşimlerini analiz etmek ve Unreal Engine 5’te yeniden tasarlarken rehber olarak kullanmak.

---

## 🕹️ Dövüş Mekaniklerinin Özeti

Oyuncu, **zombi dalgalarına karşı çeşitli silahlar ve otomatik taretler** kullanarak hayatta kalmaya çalışır.  

- **El Silahları:** Tabanca, shotgun, SMG  
- **Taretler:** Otomatik ateş eden savunma birimleri  
- **Melee / Yakın Dövüş:** Motorlu Testere, Kılıç  
- **Düşman Tipleri:** Yavaş, hızlı, tank gibi farklı zombi türleri  
- **PvP Modu:** Diğer oyunculara karşı hasar sistemi

---

## 🔄 Mekanik Detaylar

- **Hasar Sistemi:** Silahlar ve taretler düşmanlara sabit veya değişken hasar verir.  
- **Menzil & Hedefleme:** Taretler otomatik hedef alır; oyuncu manuel hedefleme yapabilir.  
- **Ateş Hızı ve Mühimmat:** Silah ve taretlerin rate of fire, reload süreleri ve ammo kapasitesi vardır.  
- **Özel Efektler:** Ateş, patlama veya elemental hasar efektleri (Fire, Electric vb.)  
- **Geri Tepme / Knockback:** Bazı silahlar düşmanları geri iter, alan kontrolü sağlar.

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Silah Ateşi | Blueprint → `Fire` fonksiyonu + `SpawnActor` projectile veya hitscan line trace |
| Taretler | Blueprint Actor → `SphereOverlapActors` veya `LineTrace` hedefleme, `FireRate` yönetimi |
| Hasar Sistemi | `ApplyDamage` veya `Custom Damage Event` kullanımı |
| Farklı Düşman Tipleri | AI Controller + Behavior Tree ile farklı hız ve saldırı desenleri |
| Mermi / Patlama Efektleri | `Niagara Particle System` + `Sound Cue` |
| PvP Hasar | `Replicated Actors` ile multiplayer damage sync |
| Geri Tepme | `LaunchCharacter` veya impulse ile knockback uygulama |

---

## 💡 Geliştirme Notları

- Taret ve silahların **upgrade versiyonları** EconomyAndUpgrades.md ile ilişkilendirilebilir.  
- Co-op modunda oyuncuların **alan paylaşımı ve friendly fire** dikkate alınmalı.  
- AI davranışları, **dalga yönetimi ve spawn noktalarıyla senkronize** olmalı.  
- Hasar görsel ve ses efektleri, oyuncuya geri bildirim sağlamak için mutlaka kullanılmalı.

---

## 📌 Özet

> Combat.md, oyuncunun ve düşmanların etkileşimlerini, silah ve taret mekaniklerini detaylandırır.  
> UE5’te Blueprint ve sistem bileşenleriyle prototiplenebilir, geliştirilebilir ve multiplayer modlarıyla uyumlu hale getirilebilir.

