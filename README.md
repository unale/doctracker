# doctracker

Doçentliğe hazırlanan akademisyenler için puan hesaplama ve dosya takip aracı.
Hesaplama **ÜAK Tablo 10 · Sağlık Bilimleri (Mart 2026)** ölçütlerine göre yapılır.

**Canlı:** https://unale.github.io/doctracker/

---

## Ne yapar

- **Yayınlarını puanlar** — tür, yazar sayısı ve yazar sırasına göre ÜAK yazar payı kuralını uygular
- **Süreçteki çalışmalarını takip eder** — fikir, etik kurul, veri, analiz, yazım, submit, revizyon, red, resubmit, kabul
- **Kesin ve potansiyel puanı ayırır** — yayımlanmış olan ile "kabul edilirse ulaşacağın" puanı karıştırmaz
- **Zorunlu şartları izler** — dokuz gate, hangisinin sağlandığını gösterir
- **13 maddenin tamamını kapsar** — makale, atıf, bildiri, kitap, tez danışmanlığı, proje, patent, ödül, editörlük, h-indeksi
- **Kural hatırlatır** — her giriş panelinde o maddenin ÜAK kuralları
- **Hedef döneme göre uyarır** — başvuruna kalan sürede hangi çalışmanın yetişmeyeceğini söyler

## Veriler nerede

**Yalnız senin tarayıcında.** Sunucu yok, hesap yok, kayıt yok. Hiçbir veri dışarı gönderilmez.

Bunun bedeli: tarayıcı verisini temizlersen ya da başka cihaza geçersen **veriler kaybolur**.
Alt bilgideki **"Yedek al"** düğmesiyle JSON kopyası indir, düzenli olarak.

## Sorumluluk reddi

Bu araç **ön hesap** yapar. Resmî kaynak **ÜAK kılavuzu** ve **Doçentlik Bilgi Sistemi**'dir;
beyanın doğruluğu ve sorumluluğu adaya aittir.

Araç bazı şeyleri **denetleyemez**: yağmacı/şaibeli dergi listesi, jüri yorumu, belge geçerliliği,
derginin yayın tarihindeki indeks durumunun resmî teyidi.

**Yalnız Sağlık Bilimleri temel alanı içindir.** Diğer temel alanların ölçütleri farklıdır.

## Kullanım

Tek dosya, bağımlılık yok. `index.html`'i tarayıcıda aç — o kadar.
Kendi sunucunda barındırmak istersen dosyayı kopyalaman yeterli.

### Temalar

Klasik (krem/kiremit) · Akamedika (beyaz/mavi) · Koyu — sağ üstten seçilir.

Gömülü dağıtım için dosyanın başındaki iki satır:

```javascript
const TEMA_SECICI=true;        // false → seçici gizlenir
const VARSAYILAN_TEMA='klasik'; // 'klasik' | 'akamedika' | 'koyu'
```

## Dış servisler

Uygulama isteğe bağlı olarak üç açık uca sorgu yapar. Hiçbiri anahtar gerektirmez,
hiçbirine kişisel veri gönderilmez:

| Servis | Ne için |
|---|---|
| [Akamedika JournalFinder](https://akamedika.com/journal-finder/) | Dergi indeks ve quartil ön taraması |
| CrossRef | DOI ile yayın künyesi |
| Web of Science çıktısı | Atıf listesi dosyadan okunur (tarayıcıda işlenir, gönderilmez) |

Quartil bilgisi **ön tarama**dır; resmî kaynak Web of Science / JCR'dir.

## Katkı

Hata bildirimi ve öneri için issue açabilirsiniz.
ÜAK ölçütleri değiştiğinde puan tabloları `KINDS`, `MD3`, `MD9`, `ELLE_MADDELER` ve
`MADDE13` sabitlerinden güncellenir.

## Lisans

MIT — bkz. [LICENSE](LICENSE)
