# 🎵 Soundscape — Ses Dünyası

**Oyun:** Yet Another Zombie Defense  
**Kategori:** WorldDesign → Soundscape  
**Amaç:** Minimalist oyun alanında tek sokak lambası altındaki atmosferi güçlendirecek ses tasarımını detaylandırmak.

---

## 🌌 Oyun Alanı Konsepti

- **Minimalist Ses Tasarımı:**  
  - Oyunun geçtiği alan neredeyse boş; sesler oyuncunun dikkatini düşmanlara ve stratejik objelere yönlendirir.  
- **Atmosfer:**  
  - Hafif rüzgar, lambanın elektrik sesi veya çevresel ambient seslerle gerilim yaratılır.  
- **Düşman Sesleri:**  
  - Zombilerin yaklaşma sesleri, oyuncuya yön ve tehdit hissi verir.  
- **Objeler ve Eylemler:**  
  - Taret ateşi, barikat yerleştirme, silah ateşi gibi interaktif sesler oyuncuya geri bildirim sağlar.

---

## 🔄 Mekanik Detaylar

- **Ambient Sound:**  
  - Alanın boşluğunu ve gece atmosferini hissettirmek için düşük seviyeli ambient sesler.  
- **Enemy Audio Cues:**  
  - Zombilerin farklı uzaklık ve hızlarına göre ses seviyeleri ayarlanır.  
  - Yakın düşmanlar daha yüksek ve net, uzaklar hafif ve bulanık olur.  
- **Player Action Sounds:**  
  - Silah ateşi, taret ateşi, barikat kurma ve pickup toplama sesleri.  
- **Interactive Feedback:**  
  - Her eyleme sesle geri bildirim verilerek oyun deneyimi güçlendirilir.

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Ambient Sound | `AmbientSoundActor` → Alanın boşluğunu dolduracak düşük seviye loop sesler |
| Directional / 3D Sound | `Attenuation` ve `Spatialization` kullanımı → Düşman ve objelerin konumuna göre ses seviyesi |
| Action Feedback | `Play Sound at Location` → Taret, silah ve barikat eylemleri için |
| Volume Control | Player UI veya Options → Ses seviyeleri ve mixer ayarları |
| Optimization | Minimal ses kanalları ve loop kullanımı → Performans için kritik |

---

## 💡 Geliştirme Notları

- Minimalist alan, seslerin önemini artırır; her ses oyuncuya bilgi ve gerilim sağlar.  
- Düşman sesleri, oyuncunun stratejik kararlarını doğrudan etkiler.  
- Atmosferik ambient sesler, gerilimi ve yalnızlık hissini pekiştirir.  
- Multiplayer’da ses senkronizasyonu, her oyuncu için doğru spatialization ile yapılmalıdır.

---

## 📌 Özet

> Soundscape.md, minimalist oyun alanındaki ses tasarımını ve oyuncuya geri bildirim sağlayan audio cues sistemini detaylandırır.  
> Unreal Engine 5’te AmbientSoundActor, PlaySound at Location ve 3D spatialization kullanımı ile prototiplenebilir ve optimize edilebilir.
