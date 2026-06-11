---
baslik: "Dirichlet Portföy Ağırlıkları"
slug: "dirichlet-portfoy-agirliklari"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [istatistik, simulasyon, portfoy, dirichlet]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Dirichlet Portföy Ağırlıkları

## Özü
Long-only portföy simpleksinden ($w_i \ge 0$, $\sum w_i = 1$) düzgün ve kontrollü dağılımla rastgele ağırlık örnekleyen yöntem; Monte Carlo portföy taramasının standart aracı.

## Tanım
$N$ varlıklı bir portföy için $w \in \Delta^{N-1}$ standart simpleks üzerinde tanımlıdır. Dirichlet dağılımı $\text{Dir}(\alpha_1, \dots, \alpha_N)$ tam olarak bu simpleks üzerinde olasılık dağılımıdır; $\alpha = (1, 1, \dots, 1)$ seçimi düzgün dağılımdır. Konsantrasyon parametresi $\alpha = c \cdot \mathbf{1}$ ile $c$ büyüdükçe ağırlıklar eşit-ağırlık $1/N$'e yakın yoğunlaşır; $c$ küçüldükçe köşelere (tek varlık) yakın yoğunlaşır. FPA pipeline'ında Dirichlet, optimum portföyün etrafındaki rastgele örneklemler üreterek (a) [[frontier-elipsi-hurst-getiri]] gibi düzlemlerde portföy bulutunu çizmek, (b) optimum aramanın stabilitesini ölçmek, (c) bootstrap-tarzı belirsizlik bantları üretmek için kullanılır. Tauron simülatöründe de kullanıcı "rastgele portföy üret" butonuyla bu örnekleme tetiklenir.

## Formül
Yoğunluk:
$$
p(w; \alpha) = \frac{1}{B(\alpha)} \prod_{i=1}^{N} w_i^{\alpha_i - 1}, \quad w \in \Delta^{N-1}
$$
Beklenen değer ve varyans:
$$
\mathbb{E}[w_i] = \frac{\alpha_i}{\sum_j \alpha_j}, \qquad \text{Var}(w_i) = \frac{\alpha_i (\alpha_0 - \alpha_i)}{\alpha_0^2 (\alpha_0 + 1)}
$$
Düzgün simpleks: $\alpha_i = 1 \,\forall i$.

## Ana Bağlamlar
- [[frontier-elipsi-hurst-getiri]] üretilen bulut bu düzlemde gösterilir
- [[rolling-backtest]] alternatif strateji üreteci
- [[markowitz-portfoy-teorisi]] etkin sınıra ulaşma yolu
- [[block-bootstrap]] tamamlayıcı belirsizlik aracı

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — portföy bulutu görselleştirme ve stabilite tarama aracı
- [Tauron](../../projects/tauron/) — simülatörde "rastgele başlangıç ağırlığı" üretiminde
- [IMF527 Portföy](../../projects/ders/) — etkin sınırın simulasyonla doğrulanmasında

## Kaynak
Standart istatistik literatürü; özel atıf yok.
