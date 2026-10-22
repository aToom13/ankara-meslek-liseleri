# Ankara Meslek Liseleri Rehberi

Ankara'daki meslek liselerini ilçe, yerleştirme türü ve puan bilgileriyle karşılaştırmak için hazırlanmış statik bir web uygulaması. Depodaki veri seti 196 okulu ve 25 ilçeyi kapsar.

**Yayın durumu:** GitHub Pages yayını kaldırılmıştır. Kaynak kodu ve veri dosyaları bu depoda bulunur; uygulama yerel olarak çalıştırılabilir.

## Özellikler

- Okul adına göre arama ve ilçe bazlı filtreleme
- Merkezi yerleştirme, yerel yerleştirme ve özel okul bilgileri
- Taban puanı ve yüzdelik dilim bulunan kayıtları karşılaştırma
- Alan bazlı puan bilgileri ve kaynak notları

## Yerel çalıştırma

Python 3 ile proje klasöründe bir HTTP sunucusu başlatın:

```bash
git clone https://github.com/aToom13/ankara-meslek-liseleri.git
cd ankara-meslek-liseleri
python3 -m http.server 8000 --bind 127.0.0.1
```

Tarayıcıda <http://127.0.0.1:8000> adresini açın. Build işlemi, npm paketi veya backend gerekmez.

## Dosyalar

| Dosya | İçerik |
|---|---|
| [index.html](index.html) | Arayüz, stiller ve filtreleme mantığı |
| [data.js](data.js) | Arayüzün yüklediği okul verileri |
| [data/ankara_meslek_liseleri.json](data/ankara_meslek_liseleri.json) | Okul veri seti ve meta bilgiler |
| [data/](data/) | Araştırma kayıtları ve kaynak dosyaları |

Arayüz `data.js` dosyasını kullanır. JSON veri setini değiştirmek tek başına arayüzü güncellemez; ilgili değişiklikleri `data.js` dosyasına da yansıtın. Bu depoda otomatik veri üretme veya doğrulama scripti bulunmuyor.

## Veri kapsamı ve güncellik

Veriler MEB, yerleştirme sonuçları, resmi okul siteleri ve web araştırmalarından derlenmiştir. Veri setinin meta bilgilerinde son güncelleme 5 Ağustos 2026 olarak kayıtlıdır.

LGS 2026 tercihleri için hazırlanmış olsa da tüm puanlar 2026 yılına ait değildir. Kayıtların `lgs_yil` alanını ve alan bazlı puanların yıl/kaynak bilgisini kontrol edin. Eksik bilgiler `null` olabilir. Bu proje resmi bir tercih veya yerleştirme hizmeti değildir; tercih öncesinde güncel MEB kılavuzunu ve okulun resmi bilgilerini esas alın.

## Veri kaynakları

Kaynak notları ve araştırma kayıtları [data/](data/) klasöründe tutulur.
