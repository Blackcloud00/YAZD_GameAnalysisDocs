# ⚡ Feedback — Oyuncuya Geri Bildirim

**Oyun:** Yet Another Zombie Defense  
**Kategori:** UI/UX → Feedback  
**Amaç:** Oyuncuya eylemler ve oyun olayları hakkında anlık geri bildirim sağlayarak deneyimi güçlendirmek.

---

## 🌌 Feedback Konsepti

- **Minimalist ve anlaşılır:** Tek alan ve tek ışık kaynağı ile oynandığından, feedback öğeleri görsel karmaşaya yol açmadan oyuncuya bilgi vermeli.  
- **Odak Noktası:** Oyuncunun eylemleri ve çevresel olaylar hakkında anlık ve anlaşılır geri bildirim.  

---

## 🔄 Feedback Türleri

1. **Damage Feedback**  
   - Oyuncu hasar aldığında ekran kenarlarında kırmızı overlay veya pulse efekti.  
   - Ses efekti: kısa alarm veya zombi saldırı sesi.  

2. **Enemy Kill / Score Feedback**  
   - Zombi öldürüldüğünde küçük floating text veya puan animasyonu.  
   - Ses efekti: kısa reward sound.  

3. **Pickup Feedback**  
   - Sağlık, ammo veya kaynak toplandığında kısa bir ikon animasyonu ve ses efekti.  
   - Screen corner veya UI slotta gösterilebilir.  

4. **Taret / Barikat Placement Feedback**  
   - Taret veya barikat yerleştirildiğinde onay animasyonu (green tick veya kısa glow).  
   - Ses efekti: metal veya build sound.  

5. **Wave / Event Alerts**  
   - Yeni dalga başladığında ekran üstünde kısa bir banner veya HUD flash.  
   - Ses efekti: alarm veya gong sesi ile oyuncu uyarılır.  

---

## ⚙️ UE5 Tasarım Önerileri

| Feedback Türü | Unreal Engine 5 Uygulaması |
|---------------|---------------------------|
| Damage Overlay | Widget Blueprint + `Set Render Opacity` → Health Variable ile bind |
| Enemy Kill Text | `Spawn Actor` veya `UMG Widget` → Floating Text + Animation |
| Pickup Animation | Widget Animation veya Particle Effect → Pickup Blueprint ile bind |
| Taret / Barikat | Material Flash veya Particle Effect → Construction Blueprint ile bind |
| Wave Alert | UMG Banner + Animation → WaveController Blueprint ile bind |
| Sound Feedback | `Play Sound at Location` veya `Play Sound 2D` → Action Event ile bind |

---

## 💡 Geliştirme Notları

- Feedback öğeleri oyuncunun dikkatini dağıtmadan bilgi vermeli.  
- Görsel ve işitsel feedback kombinasyonu deneyimi güçlendirir.  
- Animasyonlu feedback (pulse, glow, floating text) anlık bilgi sağlar ve oyuncuya ödül hissi verir.  
- Multiplayer modda feedback her oyuncuya ayrı ve senkronize gösterilmeli.  

---

## 📌 Özet

> Feedback.md, oyuncuya eylemler ve oyun olayları hakkında anlık görsel ve işitsel geri bildirim sağlayan sistemleri detaylandırır.  
> Unreal Engine 5’te Widget Blueprint, Material Effects ve Particle System kullanımıyla prototiplenebilir ve dinamik hale getirilebilir.
