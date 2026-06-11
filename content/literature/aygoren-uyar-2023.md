---
baslik: "Aygören & Uyar (2023) — Fractal Portfolio Analysis"
slug: "aygoren-uyar-2023"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [literature, fraktal, portfoy, hurst, ana-referans]
yazarlar: ["Aygören, Hakan", "Uyar, Umut"]
yil: 2023
turu: makale
citekey: aygoren2023
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Aygören & Uyar (2023) — Fractal Portfolio Analysis

## Künye
Aygören, H. & Uyar, U. (2023). **Fractal Portfolio Analysis**. (Pamukkale Üniversitesi finans literatürü; Yiğit Kumral'ın akademik danışman çevresinden). Üç PAÜ projesinde de **ana referans**: [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) "ana atılım", [Seminer](../../projects/) "fraktal piyasa örneği", [Tauron](../../projects/tauron/) "motivasyon kaynağı".

## Ana Argüman
Klasik Markowitz mean-variance optimizasyonu portföy seviyesinde kuadratik form $w^T \Sigma w$ kullanır; ancak fraktal/Hurst-tabanlı analoğun ne olabileceği literatürde net değildir. Yazarlar **portföy Hurst $H_p(w)$**'nin ağırlık vektörü $w$'ye bir fonksiyon olarak nasıl davrandığını sistematik olarak incelemiş; ampirik bulgu olarak yaklaşık kuadratik bir form $H_p(w) \approx c + w^T C w$ raporlamış; ancak bu kuadratik formun analitik bir **objective function** olarak kapalı türetimini bulamamışlardır. Makalenin merkezi açık problemi budur: "FPA için doğal objective function nedir?" Bu, Yiğit Kumral'ın FPA projesinin doğrudan motivasyon noktasıdır.

## Yöntem
- BIST veya küresel hisse senedi paneli üzerinde rolling pencere [[hurst-exponent]] tahmini ([[rescaled-range-rs]] yöntemiyle)
- Sabit pencerede Dirichlet/uniform örneklenmiş ağırlıklarla portföy bulutu üretimi (bkz. [[dirichlet-portfoy-agirliklari]])
- $H_p(w)$ değerlerinin lineer/kuadratik regresyonla fit'i; kuadratik formun açıklama gücü ölçümü
- $C$ matrisinin eigendecomposition'ı (bkz. [[eigendecomposition-dusuk-rutbeli]])
- Etkin sınırın fraktal analoğu (bkz. [[frontier-elipsi-hurst-getiri]]) görselleştirmesi

## Bulgular
1. Kuadratik form $H_p \approx c + w^T C w$ tipik $R^2 > 0.85$ ile fit ediyor ([[portfoy-hurst-kuadratik-form]]).
2. $C$ matrisi düşük-rütbelidir; ilk 2-3 eigenvektör baskındır ([[eigendecomposition-dusuk-rutbeli]]).
3. $C$ kapalı-form bir teorik nesneye karşılık gelmez — analitik objective function açık problem.
4. Uygulanabilirlik için stabilite analizi gerekli: makale bunun gerekli olduğuna işaret eder fakat tam çözmez (PAU FPA projesi bu eksiği [[out-of-sample-cokus]] ve [[subspace-stability]] analizleriyle dolduruyor).

## Etkisi
- **FPA projesi**: Doğrudan takip projesi; "objective function bulamadık" cümlesi araştırma sorusunun çekirdeği.
- **Tauron projesi**: Bu makale, Tauron'un alternatif yaklaşımının (ampirik kuadratik form yerine teorik multifraktal ceza) motivasyonu.
- **Seminer**: PAÜ'de fraktal portföy çalışmasının lokal kanıtı olarak sunum.
- Yiğit Kumral'ın hocalarıyla iletişim hattının da merkezi (Toplantı 1, 26 Nisan 2026 — Tauron tanımlanması bu makale temelinde).

## İlgili Kavramlar
- [[portfoy-hurst-kuadratik-form]] — makalenin merkez bulgusu
- [[hurst-exponent]] — temel parametre
- [[markowitz-paralelligi]] — kavramsal köprü
- [[out-of-sample-cokus]] — FPA tarafından eklenen dürüst negatif bulgu
- [[markowitz-portfoy-teorisi]] — genişletilen klasik teori

## Atıf Yapan Projeler
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — birincil takip
- [Tauron](../../projects/tauron/) — motivasyon
- [Seminer](../../projects/) — sunum referansı
