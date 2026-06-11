---
baslik: "Banka Bilançosu = Çok Parametreli Dinamik Portföy Tezi"
slug: "banka-bilanco-portfoy-tezi"
olusturuldu: 2026-05-11
guncellendi: 2026-05-11
etiketler: [bankacilik, portfoy-teorisi, dinamik-portfoy, tauron, hakan-aygoren]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Banka Bilançosu = Çok Parametreli Dinamik Portföy Tezi

## Özü
Bir bankanın bilançosu (aktif + pasif tarafı), klasik portföy teorisinin **çok parametreli, çok vadeli ve dinamik** bir genelleştirmesi olarak modellenebilir. Bu tez bankacılık domeninde Markowitz portföy teorisinin genişletilmesini öneren bir çerçevedir. Multifraktal düzeltmeli portföy optimizasyon araçlarının (örn. [Tauron](../../projects/tauron/)) **olası uygulama domeni**lerinden biridir — projenin matematiksel çekirdeği değil.

## Tezin Kanonik İfadesi

> **"Banka bilançosu çok parametreli, çok vadeli ve dinamik bir portföydür."**
>
> — Hakan Aygören Hoca'nın 2026-05-09 görüşmesinde onayladığı çekirdek cümle

## Tanım

### Bilanço Bileşenleri Portföy Olarak
- **Aktif (varlık):** krediler, menkul kıymet portföyü, döviz pozisyonları, türev pozisyonlar — her birinin **getirisi** ($\mu$), **vadesi** ($T$) ve **riski** ($\sigma$, kredi olasılığı vb.) vardır
- **Pasif (yükümlülük):** mevduat, ihraç edilen tahviller, repo, sermaye — her birinin **maliyeti** + **vadesi** vardır
- **Net pozisyon** = aktif − pasif; bankacının görevi bu pozisyonu optimize etmek

### Klasik Markowitz'ten Genelleştirme
Klasik Markowitz'in (bkz. [[markowitz-portfoy-teorisi]]) kuadratik optimizasyonu üç eksende genişler:

1. **Çok parametreli** — Tek risk faktörü (varyans) yerine: faiz, döviz kuru, kredibilite (kredi geri ödeme olasılığı), likidite riski
2. **Çok vadeli** — Tek-periyot yerine: kısa dönem (mevduat, repo) ↔ uzun dönem (krediler, tahviller) — vade uyumsuzluğu (maturity mismatch) bilinçli kullanılır
3. **Dinamik** — Statik ağırlık yerine: piyasa şartları değişince ağırlık matrisi **anlık** güncellenmeli (kuantum altyapısıyla)

## Operasyonel Uygulanması

**Greek letter + ağırlık matrisi birleşimi:**
Black-Scholes Greek letter'ları (bkz. [[greeks]]) banka pozisyonu için yeniden yorumlanır:
- **Delta** → döviz pozisyonunun spot fiyat hassasiyeti
- **Gamma** → konveksite, büyük şoklara karşı kırılganlık
- **Vega** → volatiliteye maruziyet
- **Theta** → vade uyumsuzluğunun zaman değeri etkisi

**Somut senaryo (Hakan Hoca aktarımı):**
- Bugün: "X kadar dolar, Y kadar Sterling tutuyoruz"
- Pasif tarafında: Sterling artır, dolar azalt
- Aktif tarafında: dolar artır, Sterling de artır
- Hedging: "Doları azaltırken Euro'yu artıracak" (bkz. [[delta-hedging]])

## Klasik Markowitz ile Karşılaştırma

| Klasik Markowitz | Banka Bilançosu Tezi |
|---|---|
| Tek-periyot, statik | Çok vadeli, dinamik |
| Tek risk faktörü (varyans) | Çoklu risk: faiz + döviz + kredi + likidite |
| Sadece aktif tarafı | Aktif + pasif birlikte |
| Yatırımcı için | Banka bilançosu için |
| Statik ağırlık | Anlık güncellenen ağırlık matrisi |
| Normal dağılım varsayımı | Multifraktal düzeltme |
| Klasik bilgisayar yeterli | Kuantum hızlandırma gerekir (anlık karar için) |

## Bu Tezi Operasyonelleştirecek Araçlar

Banka bilançosunun "çok parametreli, çok vadeli, dinamik portföy" karakterini ele alabilmek için klasik Markowitz yetmez. Tauron gibi multifraktal-düzeltmeli portföy araçları bu domain'e uygulandığında tez operasyonelleşir:

1. **Multifraktal düzeltme** ([[multifraktal-spektrum]], [[multifraktallik-siddeti-lambda]]): klasik varyans varsayımının yetersizliğini ($H \neq 0.5$, fat tails) düzeltir
2. **Yatırım ufku τ** parametresi: farklı vadeli pozisyonları aynı çerçevede ele alır
3. **Kuantum hızlandırma** ([[qmci]], [[qae]]): anlık karar mekanizmasını gerçek zamanlıya yaklaştırır

Tauron formülü (genel portföy için, banka özel değil):

$$\nu_i = \underbrace{\left(\frac{A\mu_i}{D} - \frac{B}{D}\right)}_{\text{Markowitz}} - \underbrace{\gamma \cdot \frac{1}{8} \cdot \sigma_i^4 \cdot \lambda_i^2 \cdot \left(\frac{\tau}{T_i}\right)^{1/3}}_{\text{Multifraktal düzeltme}}$$

Bu formül **genel** portföy optimizasyonu içindir; banka bilançosuna uygulandığında pasif tarafının vadeli yapısı ve kredibilite riski ek girdi olarak modele dahil edilir.

## Ana Bağlamlar
- [[markowitz-portfoy-teorisi]] — klasik temel
- [[abcd-parametreleri]] — kapalı-form çözümün ABCD katsayıları
- [[etkin-sinir]] — çözüm kümesinin geometrisi
- [[greeks]] — pozisyon hassasiyet ölçütleri
- [[delta-hedging]] — döviz pozisyonu hedge stratejisi
- [[multifraktal-spektrum]] — fraktal düzeltme
- [[multifraktallik-siddeti-lambda]] — λ parametresi
- [[fraktal-duzeltme-cezasi]] — düzeltme terimi
- [[hurst-exponent]] — zaman ölçeği bağımlılığı
- [[qmci]] — Kuantum Monte Carlo Integration
- [[qae]] — Kuantum Amplitude Estimation

## Projelerde Kullanım
- [Seminer 2026 Bahar](../../projects/ders/2026-bahar-seminer/) — sunum kapanış slide'ında bu tez sunulur (Hakan Hoca onaylı). Yigit'in araştırmasına **uygulama hikâyesi çerçevesi** sağlar
- [Tauron](../../projects/tauron/) — bu tez Tauron'un **olası uygulama domeniden biri**. Tauron'un matematiksel çekirdeği "multifraktal düzeltmeli Markowitz + τ (yatırım ufku)" parametresidir; banka bilançosuna uygulandığında bu tezi operasyonelleştirebilir (ileride banka müşterileri için ürünleşme potansiyeli)

## Kaynak
Hakan Aygören Hoca ile 2026-05-09 yüz yüze görüşmesinde tez doğrulandı. Bkz. [`Hakan-Hoca-Sunum-Review.md`](../../projects/ders/2026-bahar-seminer/kaynaklar/Hakan-Hoca-Sunum-Review.md) Bölüm 7-8.
