# 🖥️ HUD — Heads-Up Display

**Oyun:** Yet Another Zombie Defense  
**Kategori:** UI/UX → HUD  
**Amaç:** Oyuncuya hayatta kalma ve stratejik bilgi sağlayacak HUD öğelerini detaylandırmak.

---

## 🌌 Oyun Alanı ve HUD Konsepti

- **Minimalist ve işlevsel:** Tek alan ve tek ışık kaynağı ile oynandığından, HUD ekranın bir köşesinde yer alacak ve oyuncunun görüşünü engellemeyecek.  
- **Odak Noktası:** Oyuncunun hayatta kalması, dalga durumu ve stratejik objeler.  

---

## 🔄 HUD Öğeleri

1. **Health Bar / HP**  
   - Oyuncunun can durumunu gösterir.  
   - Ekranın sol üst köşesinde yer alabilir.  
   - Renk değişimi: Yeşil → Sarı → Kırmızı (düşük HP)  

2. **Ammo / Taret Durumu**  
   - Kullandığı silah veya yerleştirdiği taretlerin durumu.  
   - Ekranın sağ üst köşesinde veya crosshair yakınında gösterilebilir.  

3. **Wave / Enemy Info**  
   - Mevcut dalga numarası ve kalan düşman sayısı.  
   - Sağ üst veya üst orta bölgede görünür.  

4. **Score / Points**  
   - Öldürülen düşman veya topladığı puanlar.  
   - Alt köşe veya üst köşe tercih edilebilir.  

5. **Pickup / Resource Indicators**  
   - Oyuncunun topladığı itemler veya kaynaklar.  
   - Sağ alt köşede küçük ikonlarla gösterilebilir.  

---

## ⚙️ UE5 Tasarım Önerileri

| HUD Öğesi | Unreal Engine 5 Uygulaması |
|-----------|---------------------------|
| Health Bar | `ProgressBar` → Bind Health Variable |
| Ammo / Taret | `TextBlock` veya `ProgressBar` → Weapon / Turret Blueprint ile bind |
| Wave / Enemy Info | `TextBlock` → WaveController Blueprint ile bind |
| Score / Points | `TextBlock` → PlayerState veya GameMode ile bind |
| Pickup / Resource | `Image` veya `Overlay` → Item Blueprint ile bind |
| Widget Placement | `Anchor` ve `Canvas Panel` → Minimalist ve responsive tasarım |

---

## 💡 Geliştirme Notları

- Minimalist ve hızlı okunabilir HUD, oyuncunun dikkatini oyundan ayırmamalı.  
- Color coding ve ikonlar ile önemli bilgilerin hızlı algılanması sağlanmalı.  
- Multiplayer modda HUD bilgileri her oyuncuya göre ayrı ve senkronize gösterilmeli.  
- Animasyonlu feedback (örn. can azaldığında pulse efekt) oyuncuya görsel geri bildirim verir.  

---

## 📌 Özet

> HUD.md, oyuncuya hayatta kalma, dalga durumu, silah ve taret bilgisi ile puan ve pickup bilgilerini aktaran minimalist HUD tasarımını detaylandırır.  
> Unreal Engine 5’te UMG Widget Blueprint ile kolayca prototiplenebilir, bind ve animation sistemi ile dinamik hale getirilebilir.
