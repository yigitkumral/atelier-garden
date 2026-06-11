---
baslik: "Quantum Amplitude Estimation (QAE)"
slug: "qae"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [kuantum, hizlanma, montecarlo]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Quantum Amplitude Estimation (QAE)

## Özü
Klasik Monte Carlo'nun $\mathcal{O}(1/\sqrt{N})$ hata oranını $\mathcal{O}(1/N)$'e indiren ikinci-dereceden (quadratic) kuantum hızlanma algoritması; finansal beklenen değer hesaplamasının kuantum standardı.

## Tanım
$\mathcal{A}|0\rangle = \sqrt{1-a}\,|\psi_0\rangle |0\rangle + \sqrt{a}\,|\psi_1\rangle |1\rangle$ biçiminde kodlanan bir devrede $a \in [0,1]$ bilinmeyen genliği tahmin etmek istiyoruz.

QAE, [[grover-1996]]'ın amplitude amplification operatörü $\mathcal{Q} = -\mathcal{A} S_0 \mathcal{A}^{-1} S_\chi$ ile faz tahmini (phase estimation) algoritmasını birleştirir:

$$
\hat{a} = \sin^2\!\big(\pi \tilde{m} / 2^M\big), \quad |\hat{a} - a| = \mathcal{O}(2^{-M}).
$$

$N = 2^M$ Grover iterasyonu ile $a$ değeri $\mathcal{O}(1/N)$ doğrulukla bulunur — klasik MC ise aynı doğruluk için $\mathcal{O}(1/\varepsilon^2)$ örnek gerekir, kuantum ise $\mathcal{O}(1/\varepsilon)$.

**Beklenen değer kodlaması:** $a = \mathbb{E}[f(X)]$ ifadesi $f$'in kuantum aritmetik devresi ile genliğe yüklenir; bu noktada [[mcardle-2022]] gibi aritmetik-içermeyen yöntemler maliyeti düşürür.

**Pratik varyantlar:** Iterative QAE (IQAE, Grinko 2019), Maximum Likelihood QAE (Suzuki 2020) — faz tahmini kubit yükünü azaltır.

## Ana Bağlamlar
- [[grover-1996]] — amplitude amplification atası
- [[brassard-2002]] — kurucu makale
- [[qmci]] — entegrasyona uygulaması
- [[montanaro-2015]] — kanonik MC speedup teoremi
- [[fast-forwardability]] — payoff yüklemesi koşulu

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — Herman et al. ana algoritması
- [Seminer](../../projects/ders/2026-bahar-seminer/) — kuantum çağ slaydının çekirdeği

## Kaynak
[[brassard-2002]], [[montanaro-2015]], [[herman-2026]]
