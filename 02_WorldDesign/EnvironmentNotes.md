# 🗺️ Level Structure — Oyun Alanı Yapısı

**Oyun:** Yet Another Zombie Defense  
**Kategori:** WorldDesign → Level Structure  
**Amaç:** Minimalist oyun alanının yapısını, oyuncu ve düşman spawn noktalarını ve dalga ilerleyişini detaylandırmak.

---

## 🌌 Oyun Alanı Konsepti

- **Boş Alan:** Oyun, tek bir açık alanda geçer; çevrede binalar veya ekstra objeler yoktur.  
- **Sokak Lambası:** Alanın ortasında tek bir ışık kaynağı vardır; hem görsel odak hem de oyuncu stratejisi için referans noktasıdır.  
- **Sınırlar:** Oyuncu ve düşmanlar alanın belirli sınırları içinde hareket eder. Çarpışma ile alanın dışına çıkmak engellenir.  

---

## 🔄 Mekanik Detaylar

- **Spawn Noktaları:**  
  - Düşmanlar alanın kenarlarından veya belirlenmiş spawn noktalarından çıkar.  
  - Oyuncuya yakın spawn engellenir.  
- **Dalga İlerleyişi:**  
  - Her dalga, bir önceki dalgadan daha fazla veya daha güçlü zombiler içerir.  
  - Dalga arası kısa hazırlık süresi oyuncuya strateji kurma şansı verir.  
- **Player Start:**  
  - Oyuncu, lambanın yakınında başlar ve barikat/taret yerleştirmeleri yapacak şekilde alanı kullanır.  
- **Interactable Objects:**  
  - Tek alan içindeki objeler: barikatlar, taretler, pickup itemler  

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Oyun Alanı | Tek Level Blueprint veya Persistent Level → sınırlar ve tek alan setup |
| Player Spawn | PlayerStart Actor → lambanın yakınında konumlandırma |
| Enemy Spawn | Array of Spawn Points → Random Selection + `SpawnActor` |
| Dalga Yönetimi | WaveController Blueprint → Dalga sayısı, spawn miktarı ve zorluk skalası |
| Sınırlar / Collision | Blocking Volume → oyuncu ve düşmanların alan dışına çıkmasını engelleme |
| Minimal Visuals | Sokak lambası için Point Light / Spot Light + basit zemin mesh |

---

## 💡 Geliştirme Notları

- Minimalist tasarım, odak noktayı oyuncu ve dalga yönetimine yönlendirir.  
- Sokak lambası, hem görsel çekicilik hem de stratejik referans sağlar.  
- Tek alan olması, performans optimizasyonu açısından avantajlıdır; dinamik ışık ve spawn yönetimi daha kolaydır.  
- Multiplayer için spawn noktaları ve dalga yönetimi server tarafında kontrol edilmelidir.

---

## 📌 Özet

> LevelStructure.md, minimalist oyun alanını, oyuncu ve düşman spawn noktalarını ve dalga ilerleyişini detaylandırır.  
> Unreal Engine 5’te Persistent Level, PlayerStart ve Blueprint tabanlı WaveController ile prototiplenebilir, optimize edilebilir ve multiplayer modlarıyla uyumlu hale getirilebilir.
