---
baslik: "Fraktal Portföy — Map of Content (MOC)"
slug: "fraktal-portfoy-moc"
tip: moc
olusturuldu: 2026-05-24
guncellendi: 2026-05-24
etiketler: [moc, fraktal, portfoy, hurst, multifraktal]
aliases: ["FMH", "Fraktal Portfolio", "Fractal Portfolio Analysis"]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Fraktal Portföy — Map of Content

Bu MOC, fraktal piyasa hipotezi (FMH), Hurst tabanlı portföy analizi ve multifraktal düzeltmeler etrafındaki tüm vault notlarını, projeleri ve literature referanslarını tek dosyadan navigable yapar. Tezsel araştırma, sunum hazırlığı veya yeni bir konuyla bağ kurma anında **giriş noktası** olarak okunmalı.

## Niçin Bu MOC?

Atelier'de fraktal portföy ekseninde **3 aktif proje, 7 ana literature kaynağı ve 20+ atomic concept** yaşıyor. Bu yoğunluk wikilink ağına dağılmış olarak duruyor — wikilinkler yön verir ama "konunun başı nere?" sorusuna cevap **MOC** verir. Yiğit'in 3-12 ay içinde planlanan tez/makale yazımında bu MOC bölüm planının iskeleti olabilir.

## Ana Literature Kaynakları

| Citekey | Künye | Rol |
|---------|-------|-----|
| [@aygoren2023] | [[aygoren-uyar-2023]] — Aygören & Uyar (2023) — Portfolio Selection and Fractal Market Hypothesis | **Hocanın ana makalesi, FPA + Tauron'un motivasyon kaynağı** |
| [@sornette-multifractal] | [[sornette-multifractal]] — Sornette — Multifractal Returns ve Hiyerarşik Portföy | Tauron'un matematiksel kalbi |
| [@mandelbrot1963] | [[mandelbrot-1963]] — Mandelbrot (1963) — Variation of Certain Speculative Prices | Tarihsel orijin: fat-tail + fraktal |
| [@hurst1951] | [[hurst-1951]] — Hurst (1951) — Long Term Storage Capacity | R/S analizinin orijin makalesi |
| [@peters1991] | [[peters-1991]] — Peters (1991, 1994) — Fractal Market Analysis | FMH'nin finans literatürüne aktarımı |
| [@mandelbrothudson] | [[mandelbrot-hudson]] — Mandelbrot & Hudson — Misbehavior of Markets | Popüler/pedagojik fraktal piyasa kaynağı |
| [@bouchaud-volatility] | [[bouchaud-volatility-clustering]] — Bouchaud — Volatility clustering | Fiziksel finans yan bağlamı |

## Concept Ailesi

### Temel Kavramlar (Tanım + Formül)

- [[hurst-exponent]] — H ∈ (0,1), uzun-vadeli korelasyon ölçütü
- [[fraktal-piyasa-hipotezi-fmh]] — EMH'ye alternatif çerçeve
- [[multifraktal-spektrum]] — tek H değil, ölçek-bağımlı spektrum
- [[multifraktallik-siddeti-lambda]] — λ² parametresi (MRW)
- [[zeta-q-olcekleme]] — ζ(q) momentlerin ölçeklenmesi
- [[rescaled-range-rs]] — H tahmini yöntemi
- [[m-q-tau-momentleri]] — moment yapısı
- [[fat-tailed-dagilim]] — fraktal dağılım altyapısı

### Portföy Uygulama Katmanı

- [[markowitz-paralelligi]] — klasik MPT ile fraktal analoğun köprüsü
- [[portfoy-hurst-kuadratik-form]] — Hp(w) ≈ c + wᵀCw ampirik
- [[fraktal-duzeltme-cezasi]] — multifraktal-tabanlı düzeltme terimi
- [[frontier-elipsi-hurst-getiri]] — etkin sınır fraktal analoğu
- [[dirichlet-portfoy-agirliklari]] — uniform ağırlık örnekleme
- [[eigendecomposition-dusuk-rutbeli]] — C matrisi düşük-rütbeli yapı
- [[markowitz-portfoy-teorisi]] — temel teori (genişletilen)
- [[banka-bilanco-portfoy-tezi]] — Hakan Hoca'nın tez fikri (ALM açısı)

### Tahmin & Doğrulama Katmanı

- [[parabolik-fit-modeli]] — kuadratik regresyon
- [[tau-tarama]] — parametre taraması
- [[estimator-gurultusu-bias-variance]] — tahmin hatası analizi
- [[block-bootstrap]] — zaman serisi bootstrap
- [[rolling-backtest]] — out-of-sample değerlendirme
- [[survivorship-bias-duzeltmesi]] — veri temizliği
- [[subspace-stability]] — eigenvector kararlılığı
- [[out-of-sample-cokus]] — FPA'nın dürüst negatif bulgusu

## İlgili Projeler

| Proje | Bağlam |
|-------|--------|
| [Tauron](../../projects/tauron/) | Multifraktal düzeltme cezasıyla portföy optimizasyonu, Sornette çatısı |
| [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) | Aygören-Uyar 2023'ün doğrudan takip projesi; objective function açık problemi |
| [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) | ABC algoritması + embedding sentezi; fraktal motivasyon ikincil |
| [2026 Bahar Seminer](../../projects/ders/2026-bahar-seminer/) | Aygören-Uyar makalesi seminerin Slayt 13-14 atıfı |

## Açık Sorular / Araştırma Yönü

- **Açık problem (Aygören-Uyar 2023):** FPA için doğal **objective function** nedir? Kuadratik ampirik form `Hp(w) ≈ c + wᵀCw` var, ama analitik türetim yok.
- **Tauron yaklaşımı:** Ampirik kuadratik yerine **teorik multifraktal ceza** (Sornette MRW λ² parametresi) — bu hipotez doğrulamada (test set).
- **Stabilite:** FPA projesi `subspace-stability` + `out-of-sample-cokus` analizleriyle bu eksiği dolduruyor.

## Sonraki Adımlar (Tez Planı İçin)

Bu MOC bir tez bölüm taslağına dönüştürülebilir:
1. **Bölüm 1 — Teorik Çerçeve:** Hurst → FMH → Multifraktal (Hurst-1951, Mandelbrot-1963, Peters-1991, Sornette)
2. **Bölüm 2 — Portföy Genişlemesi:** Markowitz (1952) → Aygören-Uyar (2023) → Tauron alternatifi
3. **Bölüm 3 — Tahmin Disiplini:** R/S, bootstrap, rolling backtest, subspace stabilite
4. **Bölüm 4 — Uygulama:** BIST veya küresel hisse paneli (Aygören-Uyar veri çerçevesini takip)

---

*Bu MOC'a yeni concept/literature notu eklendiğinde elle güncellenir. Otomatik index için Dataview veya Bases sorgusu da kurulabilir (P2 aksiyonu).*
