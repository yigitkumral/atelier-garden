---
baslik: "Block Bootstrap"
slug: "block-bootstrap"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [istatistik, bootstrap, zaman-serisi, fraktal]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Block Bootstrap

## Özü
Zaman-bağımlı verilerde kısa-vadeli korelasyonları ve fraktal yapıyı koruyacak biçimde, sabit/değişken uzunlukta ardışık blokların rastgele yeniden örneklenmesi.

## Tanım
Klasik (i.i.d.) bootstrap her gözlemi bağımsız ve özdeş dağılımlı varsayar; finansal seriler için bu yanlıştır — volatilite kümeleri, otokorelasyonlar ve uzun-vadeli hafıza i.i.d. varsayımını ihlal eder. Block bootstrap çözümü: seriden uzunluk $\ell$ olan ardışık bloklar al ve bu blokları yerine koyma ile yeni örneklem oluştur. Blok uzunluğu $\ell$ kritiktir: çok küçükse zaman bağımlılığı kaybolur, çok büyükse efektif örneklem azalır. Pratik kural: $\ell \sim T^{1/3}$. Politis-Romano stationary bootstrap ise blok uzunluğunu geometrik dağılımla rasgeleleştirir, sınır artefaktlarını azaltır. FPA'da $\zeta_q$, $H$ ve $C_t$ tahminlerinin güven aralıklarını üretmek için block bootstrap zorunludur (klasik bootstrap fraktal yapıyı yok ettiği için bias yapar).

## Formül
Sabit bloklu (overlapping):
$$
\text{blok sayısı: } B = \lceil T / \ell \rceil, \qquad \text{indeks: } I_b \sim \text{Uniform}\{1, \dots, T - \ell + 1\}
$$
Stationary bootstrap blok uzunluğu:
$$
\ell_b \sim \text{Geometric}(p), \quad \mathbb{E}[\ell_b] = 1/p
$$
Optimal $\ell$: $\ell^* \propto T^{1/3}$ (Hall-Horowitz).

## Ana Bağlamlar
- [[estimator-gurultusu-bias-variance]] güven aralığı üretim aracı
- [[m-q-tau-momentleri]] yapı fonksiyonu için resampling
- [[rolling-backtest]] performans güven bantları

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — tüm fraktal tahmincilerin SE hesabında zorunlu adım
- [Tauron](../../projects/tauron/) — $\lambda$ ve $\zeta_q$ kalibrasyonunun belirsizlik bantları için
- [Seminer](../../projects/) — "fraktal hesap için klasik bootstrap yetmez" mesajının teknik dayanağı

## Kaynak
Politis & Romano (1994); Hall, Horowitz, Jing (1995).
