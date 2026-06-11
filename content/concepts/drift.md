---
baslik: "Drift (SDE Deterministik Bileşeni)"
slug: "drift"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [stokastik-surec, matematiksel-finans]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Drift (SDE Deterministik Bileşeni)

## Özü
Bir stokastik diferansiyel denklemde gürültüsüz, $dt$ ile orantılı eğilim terimi; sürecin ortalama yönelimini belirler.

## Tanım
$dX_t = \mu(t, X_t)\, dt + \sigma(t, X_t)\, dW_t$ biçimindeki bir SDE'de $\mu$ fonksiyonuna drift denir. Drift, sürecin küçük bir zaman aralığındaki koşullu beklenen değişimini verir ve süreç dinamiklerinin uzun-vade davranışını şekillendirir. Risk-nötr ölçüye geçildiğinde drift terimi yeniden tanımlanır (genellikle risksiz faize eşitlenir); bu, [[black-scholes]] türetiminin temel adımıdır. [[mean-reversion]] modellerinde drift, sürecin uzun-vade ortalamasına geri çekildiği yapıdadır.

## Formül
Genel SDE:
$$
dX_t = \underbrace{\mu(t, X_t)}_{\text{drift}}\, dt + \sigma(t, X_t)\, dW_t
$$
Risk-nötr ölçüde GBM: $\mu = r$ (risksiz faiz). Mean-reverting örnek: $\mu(X_t) = \kappa(\theta - X_t)$.

## Ana Bağlamlar
- [[brownian-motion-wiener]] — drift'le birlikte SDE oluşturan stokastik bileşen
- [[geometric-brownian-motion]] — sabit yüzdesel drift örneği
- [[mean-reversion]] — geri çekilen drift biçimi
- [[ito-calculus]] — drift terimini içeren değişken değişimi

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — stokastik finansın temel yapı taşı
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — risk-nötr ölçüye geçişin operasyonel parametresi

## Kaynak
[[hull-2008]]
