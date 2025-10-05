# 🧟 Wave Management — Zombi Dalga Sistemi

**Oyun:** Yet Another Zombie Defense  
**Kategori:** Gameplay → Wave Management  
**Amaç:** Oyundaki düşman dalga sistemini, zorluk artışlarını ve spawn mekaniklerini analiz etmek ve Unreal Engine 5’te yeniden tasarlamak.

---

## 🕹️ Dalga Mekaniklerinin Özeti

Oyuncular, her gece **gittikçe zorlaşan zombi dalgalarına** karşı hayatta kalmaya çalışır:

- **Dalga Sistemi:**  
  - Her dalga, önceki dalgadan daha fazla veya daha güçlü düşman içerir  
  - Dalga arası kısa süreli dinlenme veya hazırlık zamanı olabilir  

- **Düşman Çeşitleri:**  
  - Yavaş ve zayıf zombiler  
  - Hızlı ve düşük HP zombiler  
  - Tank veya mini-boss tipi yüksek HP düşmanlar  

- **Spawn Noktaları:**  
  - Sabit veya rastgele spawn noktaları  
  - Oyuncuya yakın spawn engellenir (fair play)  

- **Zorluk Artışı:**  
  - Dalga sayısı arttıkça düşman sayısı, sağlık, hız ve hasar artar  

---

## 🔄 Mekanik Detaylar

- **Dalga Yönetimi:**  
  - Dalga numarası → düşman tipi ve sayısını belirler  
  - Dalga arası süre, oyuncunun hazırlık yapması için optimize edilir  

- **Spawn Mekaniği:**  
  - Düşmanlar belirli spawn noktalarından veya random bölgelerden çıkar  
  - Çarpışma ve görünürlük kontrolü yapılır  

- **Zorluk Eğrisi:**  
  - Enemy HP ve Damage Scaling: Dalga ilerledikçe artar  
  - Enemy Count Scaling: Dalga başına düşen düşman sayısı artar  

- **Özel Düşmanlar / Mini-Bosslar:**  
  - Belirli dalgalarda güçlü düşmanlar veya özel yetenekli düşmanlar gelir  
  - Oyuncuya stratejik zorluk sunar

---

## ⚙️ UE5 Tasarım Önerileri

| Mekanik | Unreal Engine 5 Uygulaması |
|---------|---------------------------|
| Wave Controller | Blueprint Actor → Dalga numarasına göre düşman spawn planı |
| Enemy Spawn | Spawn Points Array + Random Selection + `SpawnActor` |
| Difficulty Scaling | Enemy Stats → Struct veya DataTable ile dalga numarasına göre artış |
| Special Enemies | Custom Enemy Blueprint → Unique Abilities veya High HP |
| Player Safety | Spawn noktalarını oyuncuya yakınlaştırma engeli (`SphereOverlap` ile) |
| Wave Timer | `FTimerHandle` veya `SetTimer` ile dalga başlatma ve arası süre yönetimi |
| Multiplayer Sync | `Replicated Variables` ve Server-controlled spawn sistemi |

---

## 💡 Geliştirme Notları

- Dalga ve spawn sistemi, oyuncunun hayatta kalma süresini ve stratejisini doğrudan etkiler  
- Zorluk eğrisi dengeli olmalı; ne çok kolay ne çok zor olmalı  
- Co-op modda tüm oyuncuların spawn ve dalga durumları senkronize edilmelidir  
- Mini-boss veya özel düşmanlar, oyuncuya çeşitlilik ve heyecan katar

---

## 📌 Özet

> WaveManagement.md, oyunun dalga ve düşman spawn sistemlerini detaylandırır.  
> Unreal Engine 5’te Blueprint tabanlı Wave Controller, Enemy Blueprints ve timer yönetimi ile prototiplenebilir, optimize edilebilir ve multiplayer modlarıyla uyumlu hale getirilebilir.

