# Ankara Meslek Liseleri Rehberi (LGS 2026)

Ankara'daki 196 meslek lisesini tek sayfada karşılaştıran açık kaynak bir LGS tercih rehberi. Filtreleme, arama, puan sıralaması ve adrese göre (yerel yerleştirme) bilgisi tek ekranda.

## Canlı Site

https://atoom13.github.io/ankara-meslek-liseleri/

## İçerik

- 196 okul / 25 ilçe
- 53 sınavlı (merkezi yerleştirme) okul — LGS taban puanı ve yüzdelik dilimleri
- 106 yerel yerleştirme (adrese göre) okul
- 37 özel meslek lisesi — tek tek araştırıldı, yayınlanmış puanı bulunan yalnızca ASO Teknik Koleji (%6, 2026)
- Alan bazlı MEB 2025 taban puanları (`alan_puanlari`)

## Veri

- Ana veri: `data/ankara_meslek_liseleri.json`
- Kaynaklar: MEB / LGS yerleştirme sonuçları / web araştırması
- Taban puanlar kaynağa göre farklı yıllara ait olabilir — `lgs_yil` alanına bakınız
- Araştırma kanıtları: `data/arama_G1..G6`, `data/arama_tektek.json`

## Geliştirme

```bash
python3 tools/validate_data.py   # veri doğrulama
python3 tools/build_webui_data.py # data.js üretimi
node tools/test_webui.js          # arayüz testi
```

## Lisans

Veri kamuya açık kaynaklardan (MEB, resmi okul siteleri) derlenmiştir.
