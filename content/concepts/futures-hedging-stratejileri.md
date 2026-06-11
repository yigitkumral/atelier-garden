---
baslik: "Futures Hedging Stratejileri (Short Hedge / Long Hedge)"
slug: "futures-hedging-stratejileri"
olusturuldu: 2026-05-24
guncellendi: 2026-05-24
etiketler: [finans, turev, hedge, risk-yonetimi, emtia, futures]
aliases: [short-hedge, long-hedge, futures-hedge]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Futures Hedging Stratejileri

## Özü
Fiziki bir varlığa veya ileride gerçekleşecek bir nakit akışına maruz kalan kuruluşun, ters yönlü futures pozisyonu açarak fiyat riskini kısmen veya tamamen nötralize etmesi. **Hedger ≠ spekülatör**: amaç kâr değil, ticari marjı sabitlemek.

## Tanım
İki temel hedge tipi vardır:

**1. Short Hedge (Satış Hedge'i / Stok Koruma)**
Fiziki mal stoğunda olan veya ileride satacak kuruluşun futures'ta **short** pozisyon açmasıdır. Fiyat düşerse fiziki stok değer kaybeder, futures short kâr eder → net etki nötralize.

**2. Long Hedge (Alış Hedge'i / Maliyet Sabitleme)**
İleride mal alacak kuruluşun futures'ta **long** pozisyon açmasıdır. Fiyat artarsa fiziki alım maliyeti artar, futures long kâr eder → net etki nötralize.

Hull, Ch. 3 bu mantığı **anticipated transaction hedge** çerçevesinde kurgular. Pratikte hedge **mükemmel değildir** ([[basis-risk]] her zaman vardır); [[optimal-hedge-ratio]] korelasyon bazlı kısmi hedge formülü kullanılır.

## Türk Gıda Toptancısı Örnekleri

| Senaryo | Risk | Pozisyon | Tipik Kontrat |
|---|---|---|---|
| 100 ton un stoku, 2 ay sonra satacak | Fiyat düşerse zarar | **Short** Euronext Milling Wheat (EBM1) | EBM1 (50 ton) → 1-2 kontrat (%50-70 hedge) |
| 2 ay sonra 10 ton kahve alacak | Fiyat artarsa marj erir | **Long** ICE Coffee C (KC) | KC (17 ton) → 1 kontrat büyük → option spread tercih |
| 500 ton palm yağı stoku | Fiyat düşerse zarar | **Short** FCPO1 (Bursa Malaysia) | FCPO1 (25 ton) → 10-20 kontrat |
| Müşteriye sabit fiyatlı buğday sözü | Fiyat artarsa zarar | **Long** Euronext Milling Wheat | EBM1 long |

## Options ile Hedge Alternatifi
Futures'ta variation margin riski sınırsızdır; options'ta maksimum zarar primdir.

| Risk | Futures çözümü | Options çözümü |
|---|---|---|
| İleride kahve alacak, fiyat artmasın | Long futures | **Call option** almak |
| Stoktaki kakao düşmesin | Short futures | **Put option** almak |
| Yağ fiyatı artmasın | Long futures | **Call spread** |

KOBİ için options/spread daha yönetilebilir ama prim maliyeti yüksek olabilir. Çok volatil ürünlerde (kahve, kakao) options tercih edilir.

## İşleyiş Tablosu (Short Hedge Örneği)

| Piyasa Hareketi | Fiziki Stok | Futures Short | Net |
|---|---|---|---|
| Fiyat düşer | Zarar | Kâr | ≈ 0 (basis hariç) |
| Fiyat yükselir | Kâr | Zarar | ≈ 0 (basis hariç) |

Net sıfır değil [[basis-risk]] kadar sapma vardır.

## Ana Bağlamlar
- [[basis-risk]] — hedge mükemmel olmamasının nedeni
- [[optimal-hedge-ratio]] — h* formülü ile kısmi hedge
- [[delta-hedging]] — opsiyon tarafında ilk dereceden hedge
- [[cme-micro-ag-futures]] — KOBİ ölçeği için ideal kontrat tipi

## Projelerde Kullanım
- [Gıda Toptancı Emtia Hedging](../../projects/gida-toptanci-emtia-hedging/) — birincil uygulama vakası
- [IMF527 Portföy Ödevi](../../projects/ders/2026-bahar-imf527-portfoy-odev/) — risk yönetimi ders bağlamı

## Kaynak
- Hull, J. (2018). *Options, Futures, and Other Derivatives*, Ch. 3
- CME Group, *Grain and Oilseed Hedger's Guide*
- USDA ERS, EIB-219
