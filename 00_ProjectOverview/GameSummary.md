# 🎮 Game Summary

## 🧩 Genel Bilgi
- **Oyun Adı:** [YET ANOTHER ZOMBIE DEFENSE]  
- **Tür:** [Zombi / Hayatta Kalma / Çok Oyunculu - Eşli / Kule Savunma]  
- **Perspektif:** [izometrik]  
- **Platform(lar):** [PC-Steam]  
- **Motor:** [XNA Engine]  
- **Geliştirici:** [Awesome Games Studio]  
- **Yayın Tarihi:** [28 Mart 2014]  

---
---

## 🕹️ Oyunun Temel Amacı
Oyuncu, her gece giderek güçlenen **zombi dalgalarına** karşı hayatta kalmaya çalışır.  
Amaç, **mümkün olan en uzun süre savunmayı sürdürmek** ve **liderlik tablosunda en yüksek puanı elde etmektir**.

> Oyuncu için kaçınılmaz olan “ölüm” sonu vardır, fakat önemli olan *ne kadar dayanabileceği*dir.  
> Bu yönüyle oyun, süreye dayalı bir beceri testi ve kaynak yönetimi deneyimi sunar.

---

## 🌍 Oynanış Özeti
Oyun, klasik arcade shooter formülünü temel alır fakat strateji unsurları ile genişletilmiştir.

- Gündüzleri savunma alanını planlar, **taretler** ve **barikatlar** kurarsın.  
- Geceleri zombiler dalgalar hâlinde saldırır.  
- Her tur sonunda kazandığın para ile yeni silahlar veya savunmalar satın alırsın.  
- Oyun döngüsü, sürekli olarak “planla → savun → geliştir” mantığına dayanır.

**Ana mekanikler:**
- Farklı silah türleri (SMG, shotgun, sniper, flamethrower vb.)  
- Otomatik taretler ve yerleştirilebilir savunma objeleri  
- Co-op modda iş bölümü (ör. biri tamir yaparken diğeri savunma ateşi açar)  
- PvP deathmatch modunda oyuncular birbirine karşı savaşabilir  

> Oynanış temposu giderek artar; her gece düşman sayısı ve zorluk seviyesi yükselir.  
> Bu nedenle oyuncunun kaynak yönetimi ve alan kontrolü becerisi kritik hale gelir.

---

## 🎭 Temalar ve Atmosfer
- **Tema:** Kıyamet sonrası hayatta kalma  
- **Atmosfer:** Soğuk, karanlık ve sürekli tehdit altındaki bir ortam  
- **Görsel stil:** Minimalist, lo-fi modelleme ve sabit kamera açısı  
- **Renk paleti:** Karanlık griler, kırmızılar ve turuncular  
- **Ses tasarımı:** Düşük tempolu elektronik müzik, yoğun silah sesleri ve zombi çığlıkları  

> Oyun, dramatik hikâye anlatımı yerine “gerilim ve adrenalin” atmosferi yaratmaya odaklanır.  
> Oyuncunun kendini giderek artan baskı altında hissetmesi amaçlanmıştır.

---

## 🧠 Oyuncu Deneyimi Özeti
- **Zorluk Düzeyi:** Artan zorluk (her dalga sonrası güçlenir)  
- **Hedef Kitlesi:** Refleks odaklı arcade oyuncuları, skor peşinde koşanlar  
- **Oyun Süresi:** Ortalama 15–40 dakika (tek oturum)  
- **Yeniden Oynanabilirlik:** Yüksek — her denemede farklı strateji kombinasyonları  

> Oyun kısa ama tekrar oynanabilir yapısıyla “bir tur daha” hissi yaratır.  
> Oyuncular genellikle kendi stratejilerini optimize etmeye çalışır (örneğin taret dizilimi veya silah seçimi).

---

## 💡 Unreal Engine 5 için Notlar
Bu oyunu Unreal Engine 5’te yeniden tasarlarken dikkat edilebilecek noktalar:

| Orijinal Özellik | UE5 Uygulaması |
|------------------|----------------|
| Üstten görünüm kamera | UE5 `SpringArm + CameraComponent` setup |
| Dalgalar halinde düşman üretimi | `WaveManager` Blueprint sınıfı + `SpawnActor` kullanımı |
| Otomatik taret sistemi | Blueprint tabanlı `TargetingComponent` + `LineTrace` saldırı sistemi |
| Co-op çok oyunculu mod | UE5 `Online Subsystem` (Steam veya EOS) ile `Replicated Actors` |
| Basit ekonomi sistemi | Blueprint veya C++ tabanlı `CurrencyManager` |
| Işıklandırma | `Lumen` ile dinamik gece aydınlatması, vurgu spotları |
| Ses tasarımı | `MetaSounds` ile dalgaya göre yoğunluk değişen müzik sistemi |

> Amaç, UE5’in modern sistemleriyle (Lumen, Niagara, MetaSounds) aynı arcade yapıyı güncel hisle yeniden yaratmaktır.  

---

## ⚙️ HD Remastered Notları
HD sürümü; görseller, fizik, karakter animasyonları ve genel performans açısından geliştirilmiş bir versiyondur.

- Yeni zombi türleri ve saldırı animasyonları  
- İyileştirilmiş fizik etkileşimleri  
- Bulut kayıt desteği  
- Kontrolcü remap sistemi  
- Geliştirilmiş lokalizasyon ve chat özellikleri  

> UE5 sürümünde bu farkların çoğu zaten doğal olarak sağlanabilir (özellikle fizik, gölgelendirme ve input remapping konularında).

---

## 🔞 Yetişkin İçerik Açıklaması
> Bu oyunda sık sık **şiddet ve kan** içeren sahneler yer alır.  
> İçerik 16+ yaş üzeri için uygundur.

---

## 🧾 Özet
> *Yet Another Zombie Defense*, minimal ama zorlu bir **hayatta kalma simülasyonu** sunar.  
> Oyuncunun stratejik planlama ve refleks becerilerini test eden arcade bir deneyimdir.  
> Unreal Engine 5 üzerinde yeniden tasarlandığında, bu yapı modern grafikler ve daha derin sistemlerle genişletilebilir.

---

## 🧭 Sonraki Adım
- [Gameplay Analizi →](../01_Gameplay/Movement.md)

