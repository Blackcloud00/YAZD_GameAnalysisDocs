# 🛠️ Abilities — Oyuncu Yetenekleri

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Player Abilities  
**Amaç:** Oyuncunun kullanabileceği özel yetenekler ve güçlendirmeleri analiz etmek, Unreal Engine 5’te yeniden tasarlarken rehber olarak kullanmak.

---

## 🕹️ Yeteneklerin Özeti

Oyuncu, hayatta kalma süresini artırmak ve stratejilerini çeşitlendirmek için **geçici yetenekler** ve **güçlendirmeler** kullanabilir:

- **Hız Artışı (Speed Boost):**  
  Kısa süreliğine hareket hızı artar.  
- **Patlayıcı (Bomb / Grenade):**  
  Belirli bir alan içindeki zombilere hasar verir.  
- **Taret Güçlendirme (Turret Boost):**  
  Yerleştirilen taretlerin ateş gücü veya ateş hızı geçici olarak artar.  
- **Kalkan / Damage Reduction:**  
  Oyuncuya gelen hasarı belirli bir süre azaltır.  
- **Special Ammo / Elemental Rounds:**  
  Taret veya silahlara geçici ekstra efekt (örneğin ateş veya elektrik hasarı).

---

## 🔄 Mekanik Detaylar

- **Kullanım Limiti:** Yetenekler cooldown veya kaynak tüketimi ile sınırlıdır.  
- **Etki Süresi:** Her yetenek belirli bir süre boyunca aktiftir (örn. 5–10 saniye).  
- **Görsel ve Ses Efektleri:** Yetenek kullanımı sırasında hem görsel (particles) hem de ses (cue) ile oyuncuya geri bildirim verilir.  
- **Stratejik Kullanım:** Zombilerin yoğunlaştığı bölgelerde veya kritik anlarda kullanılır.

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Cooldown / Timer | `FTimerHandle` veya `Delay` node ile süre yönetimi |
| Hız Artışı | `CharacterMovementComponent → MaxWalkSpeed` geçici modifikasyonu |
| Patlayıcı / Area Damage | Blueprint Actor + `SphereOverlapActors` → `ApplyDamage` |
| Taret Güçlendirme | Taret Blueprint’e geçici `FireRateMultiplier` veya `DamageMultiplier` ekleme |
| Kalkan / Damage Reduction | `GameplayTag` veya `Custom Damage Calculation` ile hasar azaltma |
| Görsel/Ses Efektleri | `Niagara` particle effect + `AudioComponent` play on use |

---

## 💡 Geliştirme Notları

- Yetenekler **stackable** olabilir veya sadece tek seferlik kullanılabilir.  
- Co-op modunda **paylaşımlı yetenekler** veya takım buffları düşünülebilir.  
- UI’da cooldown ve aktif durum göstergesi için **Widget Blueprint** kullanılmalı.  
- Yeteneklerin **upgrade versiyonları** da EconomyAndUpgrades.md dosyasında ele alınabilir.

---

## 📌 Özet

> Abilities.md dosyası, oyuncuya çeşitli geçici avantajlar sağlayan yetenekleri ve bunların oyun mekaniklerine etkilerini özetler.  
> Unreal Engine 5’te tasarım, Blueprint ve sistem bileşenleriyle bu yetenekler prototiplenebilir ve optimize edilebilir.
