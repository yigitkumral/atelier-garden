---
baslik: "CME Micro Ag Futures (2025)"
slug: "cme-micro-ag-futures"
olusturuldu: 2026-05-24
guncellendi: 2026-05-24
etiketler: [finans, turev, futures, emtia, kobi, cme]
aliases: [micro-wheat, micro-corn, micro-soybean, micro-ag]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# CME Micro Ag Futures (2025)

## Özü
CME Group'un Şubat 2025'te lanse ettiği, standart tarım (grain/oilseed) futures kontratlarının **1/10 büyüklüğünde** ve **nakdi uzlaşılı** versiyonları. KOBİ ölçeğindeki şirketlerin tarım emtia hedging'ine giriş eşiğini dramatik şekilde düşürür.

## Tanım
Standart CBOT corn/wheat/soybean kontratları 5.000 bushel (≈127-136 ton) büyüklüğündedir; bir kontratın notional değeri 20-50K USD aralığında, başlangıç teminatı 1-2K USD. Bu boyut **küçük toptancı/üretici için fazla**. CME 2025'te bu sorunu Micro Ag suite ile çözdü: 500 bushel kontratlar nakdi uzlaşılı, standartla aynı fiyat hareketini izler.

[[futures-hedging-stratejileri]] çerçevesinde, KOBİ ölçekli Türk gıda toptancısı için ZW/ZC yerine **Micro Wheat / Micro Corn** ilk pratik adımdır.

## Kontrat Tablosu

| Micro Kontrat | Standart Karşılığı | Büyüklük | Yaklaşık Notional (2026) |
|---|---|---|---|
| Micro Wheat (MZW) | CBOT Wheat (ZW) 1/10 | 500 bushel ≈ 13.6 ton | ~$3,235 |
| Micro Corn (MZC) | CBOT Corn (ZC) 1/10 | 500 bushel ≈ 12.7 ton | ~$2,318 |
| Micro Soybean (MZS) | CBOT Soybean (ZS) 1/10 | 500 bushel | değişken |
| Micro Soybean Oil (MZL) | CBOT Soybean Oil (ZL) 1/10 | 6,000 lb ≈ 2.7 ton | ~$4,437 |
| Micro Soybean Meal (MZM) | CBOT Soybean Meal (ZM) 1/10 | 10 short ton | değişken |

**Önemli özellik:** Tüm Micro Ag kontratları **financially settled** (nakdi uzlaşılı) — fiziki teslim yok, expirasyonda CME fiyat endeksine göre nakit ödemesi. Bu KOBİ için ek avantaj: depo, teslim, kalite uyumsuzluğu sorunu yok.

## KOBİ Sermaye Avantajı
50K USD nakit imkanı ile:
- **Standart ZW:** 1-2 kontrat hedge edilebilir (136-272 ton notional, dar manevra)
- **Micro Wheat:** 10-15 kontrat hedge edilebilir (136-204 ton notional, geniş ayarlama)

Bu **granularity** (ince ayar) KOBİ'nin gerçek stok seviyesine yakın hedge oranı tutmasını sağlar. [[optimal-hedge-ratio]] formülünde hesaplanan $h^*$ değeri (örn. 50 ton hedge gereği) standart kontratta yuvarlanır; Micro kontratta daha yakın yakalanır.

## Türk Toptancı İçin Pratik Başlangıç Portföyü
- **Micro Wheat (MZW)** — un/buğday stok riski
- **Micro Corn (MZC)** — mısır/yem ithalat hedge'i
- **Micro Soybean Oil (MZL)** — bitkisel yağ proxy
- ICE Coffee C (KC) izleme — sadece sinyal, opsiyon ile pozisyon
- USD/TRY hedge — kur riski (futures veya banka forward)

## Sınırlamalar
- **Likidite:** 2025'te başladı, henüz standart kontratlar kadar derin değil. Order book kontrolü şart.
- **Tüm ürünler için Micro yok:** Pamuk, kahve, kakao, şeker için Micro versiyon henüz yok.
- **Brokerlar:** Tüm brokerlar listede tutmuyor — IBKR/Saxo destekliyor, bazı Türkiye aracı kurumlar henüz eklemedi.

## Ana Bağlamlar
- [[futures-hedging-stratejileri]] — Micro kontratlar bu stratejilerin KOBİ-friendly uygulayıcısı
- [[optimal-hedge-ratio]] — h* hesabı Micro ile daha hassas uygulanır
- [[basis-risk]] — Micro / standart kontrat arasında basis yok (aynı fiyat endeksi); basis riski [[futures-hedging-stratejileri]] standart düzeyinde kalır

## Projelerde Kullanım
- [Gıda Toptancı Emtia Hedging](../../projects/gida-toptanci-emtia-hedging/) — KOBİ'nin ilk denemesi için **kritik araç**

## Kaynak
- [CME Group basın bülteni, 30 Ocak 2025](https://www.cmegroup.com/media-room/press-releases/2025/1/30/cme_group_to_launchmicro-sizedgrainsandoilseedfuturesonfebruary2.html)
- [CME Group Micro Ag Futures FAQ](https://www.cmegroup.com/articles/faqs/faq-micro-agriculture-futures.html)
