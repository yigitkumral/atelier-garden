---
baslik: "Quantum Monte Carlo Integration (QMCI)"
slug: "qmci"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, montecarlo, hizlanma]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Quantum Monte Carlo Integration (QMCI)

## Özü
Klasik [[monte-carlo-entegrasyonu]]'nu [[qae]] üzerinden quadratic olarak hızlandıran genel çerçeve; $\mathbb{E}[f(X)]$ tahminini $\mathcal{O}(1/\varepsilon)$ kuantum sorgusuyla yapar.

## Tanım
İki temel adım:

1. **Dağılım yüklemesi:** $|0\rangle^{\otimes n} \to \sum_x \sqrt{p(x)}\,|x\rangle$ — $X$ rastgele değişkeninin dağılımını kuantum süperpozisyonuna kodla.
2. **Payoff oracle + amplitude:** $f(x) \in [0,1]$ değerini bir ek kubitin genliğine yükle: $\sum_x \sqrt{p(x)}|x\rangle\big(\sqrt{1-f(x)}|0\rangle + \sqrt{f(x)}|1\rangle\big)$. Ek kubit $|1\rangle$ olma olasılığı tam olarak $a = \mathbb{E}[f(X)]$.
3. Bu $\mathcal{A}$ devresine [[qae]] uygulayarak $a$'yı $\mathcal{O}(1/\varepsilon)$ ile tahmin et.

**Hızlanma:** Klasik $\mathcal{O}(\sigma^2/\varepsilon^2)$ vs. kuantum $\mathcal{O}(\sigma/\varepsilon)$ örnek karmaşıklığı — Montanaro 2015'in temel sonucu.

**Engel:** Adım 1 (P-loader) ve özellikle adım 2 (payoff aritmetiği) için derin devreler gerekebilir; kuantum hızlanması ancak bu maliyetler $\mathcal{O}(\text{poly}\log)$ ölçeğinde tutulduğunda korunur. [[mcardle-2022]] ve Chebyshev polinom yaklaşımları bu sorunu adresler.

## Ana Bağlamlar
- [[qae]] — temel kuantum motor
- [[montanaro-2015]] — formal speedup teoremi
- [[monte-carlo-entegrasyonu]] — klasik karşıt
- [[mcardle-2022]] — verimli yükleme
- [[kuantum-turev-fiyatlama]] — finansal uygulama

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al.'in tüm fiyatlama önerilerinin omurgası
- [Seminer](../../projects/ders/2026-bahar-seminer/) — kuantum-finans slaydı

## Kaynak
[[montanaro-2015]], [[stamatopoulos-2020]], [[herman-2026]]
