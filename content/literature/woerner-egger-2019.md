---
baslik: "Quantum Risk Analysis"
slug: "woerner-egger-2019"
olusturuldu: 2026-05-11
guncellendi: 2026-05-11
etiketler: [kuantum, risk-yonetimi, var, cvar, qae, piyasa-riski]
citekey: woerner2019
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Woerner & Egger 2019 — Quantum Risk Analysis

## Künye
Stefan Woerner, Daniel J. Egger, "Quantum Risk Analysis", *npj Quantum Information* 5, 15, 2019. (arXiv:1806.06893; DOI: 10.1038/s41534-019-0130-6) — IBM Research Zurich.

## Ana Argüman
Klasik finansta zorunlu olan piyasa risk metrikleri — özellikle **Value-at-Risk (VaR)** ve **Conditional Value-at-Risk (CVaR)** — [[qae|Quantum Amplitude Estimation]] üzerinden klasik Monte Carlo'ya **near-quadratic hızlandırma** ile hesaplanabilir. BS-içi kuantum finans literatürünün temel referansı; [[stamatopoulos-2020|Stamatopoulos 2020]] ve [[stamatopoulos-2022|Stamatopoulos 2022]]'nin altyapısı.

## Yöntem
- Belirsizlik kaynaklarını $n$ qubit üzerinde olasılık dağılımı olarak kuantum durumuna yükle.
- Kayıp fonksiyonu $L$'yi genliğe kodla; eşik $L \geq \ell$ olayının olasılığını QAE ile tahmin et — VaR.
- CVaR için koşullu beklenen değer formülasyonu (kuyruk-bağımlı kuantum altyapı).
- **Devre derinliği / yakınsama dengesi:**
  - En sığ devre (qubit sayısında polinom): $O(M^{-2/3})$ — klasik MC'nin $O(M^{-1/2})$ ölçeklemesinden zaten daha iyi.
  - Daha derin (polinomyal) devrelerde optimal $O(M^{-1})$ — **klasik MC'ye göre kuadratik avantaj**.
- IBM Q Experience donanımında gerçek deneyler.

## Bulgular
- **Toy model 1 (gerçek donanım):** ABD Hazine bonosu (T-bill) portföyünün faiz artışı riski — IBM Q Experience'ta ölçüldü. Kuadratik hızlanmanın küçük örneklerde de gözlenebilir olduğu doğrulandı.
- **Toy model 2 (simülasyon):** İki varlık + farklı vade yapısındaki hükümet borç portföyünde VaR/CVaR — yakınsama klasik MC'den anlamlı şekilde daha hızlı.
- **Hata analizi:** Cross-talk ve enerji gevşeme (T1) gürültüsünün etkisi simülasyonla nicelleştirildi; küçük devrelerde anlamlı sonuçlar alınabiliyor.

## Etkisi
- BS-içi kuantum finans literatürünün **ilk pratik referansı** (2018 önbaskı, 2019 yayın). Stefan Woerner [[stamatopoulos-2020|Stamatopoulos 2020]] ve [[stamatopoulos-2022|Stamatopoulos 2022]]'de de yazar olarak yer alır — bu üç çalışma birbirinin teknik altyapısını paylaşır.
- Bankaların **regülasyon raporlamalarına** (Basel III sermaye yeterlilik, stres testi) doğrudan uygulama domaini önerir: bilanço risk metrikleri saniye-bazında güncellenebilir.
- [[chakrabarti-2021|Chakrabarti 2021]] kuantum-finans üstünlük eşiği analizinin temel girdisi.

## BS-İçi Kuantum Üçlüsündeki Yeri
BS modelinin **dağılımsal sonuçlarını** kuantum altyapıya taşıyan üç-ayaklı yapının risk ayağıdır:

| Soru | Karşılık | Kaynak |
|---|---|---|
| Bu opsiyon kaça satılsın? | QAE + state preparation | [[stamatopoulos-2020]] |
| Faiz/volatilite oynarsa fiyat ne kadar değişir? | Quantum gradient estimation | [[stamatopoulos-2022]] |
| **Portföy en kötü %5 senaryoda ne kaybeder?** | **QAE + tail probability** | **Woerner-Egger 2019** |

## İlgili Kavramlar
- [[qae]]
- [[var-cvar]] (yazılacaksa)
- [[delta-hedging]]
- [[kuantum-turev-fiyatlama]]
- [[banka-bilanco-portfoy-tezi]]

## Atıf Yapan Projeler
- [Seminer](../../projects/ders/2026-bahar-seminer/) — BS-içi kuantum üçlüsünün risk ayağı; sunum Slayt 20 banka bilançosu tezine doğrudan altyapı (VaR/CVaR = Basel III stres testi kuantum karşılığı)
- [Tauron](../../projects/tauron/) — banka bilanço portföy tezi; multifraktal-düzeltmeli Markowitz'in risk yönetimi tarafı için referans
