---
baslik: "Monte Carlo Entegrasyonu"
slug: "monte-carlo-entegrasyonu"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [numerik, montecarlo, entegrasyon]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Monte Carlo Entegrasyonu

## Özü
Yüksek boyutlu integralleri rastgele örneklemeyle hesaplayan numerik yöntem; hata oranı boyuttan bağımsız olarak $\mathcal{O}(1/\sqrt{N})$ ile azalır.

## Tanım
$\mathbb{E}[f(X)] = \int f(x)\, p(x)\, dx$ türündeki bir beklenen değeri hesaplamak için $X_1, \dots, X_N$ i.i.d. örnekler $p$ dağılımından çekilir ve örneklem ortalaması alınır:

$$
\hat{I}_N = \frac{1}{N} \sum_{i=1}^{N} f(X_i).
$$

Büyük sayılar yasası $\hat{I}_N \to \mathbb{E}[f(X)]$ yakınsamasını, merkezi limit teoremi ise hatanın $\mathrm{Var}(f(X))/N$ varyansıyla normal dağıldığını verir. Standart hata:

$$
\mathrm{SE}(\hat{I}_N) = \frac{\sigma_f}{\sqrt{N}}.
$$

Türev fiyatlamada $f$ iskonto edilmiş payoff, $X$ ise altında yatan varlık yörüngesidir; risk-nötr ölçümde $\mathbb{E}^{\mathbb{Q}}[e^{-rT} \cdot \text{payoff}]$ hesaplanır.

## Ana Bağlamlar
- [[boyutluluk-laneti]] — MC'nin grid yöntemlerine üstünlük sebebi
- [[euler-maruyama]] — yörünge üretimi için ayrıklaştırma
- [[mlmc]] — varyans azaltma için çok-seviyeli uzantı
- [[qmci]] — kuantum hızlandırılmış sürümü

## Projelerde Kullanım
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — klasik baseline, kuantum hızlanmanın karşılaştırma noktası
- [Seminer](../../projects/ders/2026-bahar-seminer/) — kuantum çağ slaydında klasik MC tanıtımı

## Kaynak
[[glasserman-2003]], [[herman-2026]]
