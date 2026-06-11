---
baslik: "Frontier Elipsi: Hurst-Getiri Düzlemi"
slug: "frontier-elipsi-hurst-getiri"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [hurst, frontier, gorsel, fpa]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Frontier Elipsi — (H_p, E[R_p]) Düzlemi

## Özü
Klasik $(\sigma_p, E[R_p])$ etkin sınır düzleminin fraktal analoğu: portföy Hurst $H_p$ ekseninde portföy beklenen getirisinin oluşturduğu sınır.

## Tanım
[[markowitz-portfoy-teorisi]] etkin sınırı $(\sigma_p, E[R_p])$ düzleminde hiperbol biçimindedir. FPA'da bu fikrin paraleli: $H_p$ (portföy Hurst) yatay eksen, $E[R_p]$ dikey eksen. Tüm Dirichlet ile üretilen rastgele portföyler bu düzlemde bir bulut oluşturur; dış sınır bir elips/parça-eğri verir. [[portfoy-hurst-kuadratik-form]] $H_p \approx c + w^T C w$ kuadratik formdur, beklenen getiri ise $E[R_p] = w^T \mu$ lineerdir; iki kuadratik kısıtın gerdiği kümede sınır kapalı-form elips tipinde geometriler verir. Bulut görseli FPA'nın bilişsel-en-değerli grafiklerinden biridir: yatırımcıya "düşük Hurst (anti-persistent) portföyleri seçersen kararlı, yüksek Hurst (trend) portföyleri seçersen volatil-kümeli rejim alırsın" sezgisini iletir. Tauron simülatöründe bu düzlem interaktif — kullanıcı $\tau$ kaydırınca elips şekil değiştirir.

## Formül
$\mu_p = w^T \mu$, $H_p \approx c + w^T C w$ ile parametrize edilen sınır:
$$
\max_w \mu_p \quad \text{s.t.} \quad H_p = h^*, \; w^T \mathbf{1} = 1
$$
Lagrange ile kapalı form (analog Markowitz):
$$
w^*(h^*) = C^{-1}\big(\alpha \mu + \beta \mathbf{1}\big), \quad \alpha, \beta = f(h^*, c, \mu, C)
$$

## Ana Bağlamlar
- [[portfoy-hurst-kuadratik-form]] sınırın kuadratik tarafı
- [[etkin-sinir]] klasik analog
- [[markowitz-paralelligi]] biçimsel paralellik
- [[dirichlet-portfoy-agirliklari]] bulut üretimi

## Projelerde Kullanım
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — projenin hedef görseli; faz1'de elips fitleme, faz2'de zamansal evrim animasyonu
- [Tauron](../../projects/tauron/) — simülatörün ana grafik paneli, $\tau$ kaydırınca elips deformasyonu
- [Seminer](../../projects/) — "Markowitz frontier'ın fraktal eşi" sezgisel anlatımı

## Kaynak
[[aygoren-uyar-2023]]
