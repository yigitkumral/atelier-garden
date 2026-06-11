---
baslik: "τ Yatırım Ufku Taraması"
slug: "tau-tarama"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [fraktal, multifraktal, yatirim-ufku, tarama]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# τ — Yatırım Ufku Taraması

## Özü
Optimal portföyün, yatırım ufku $\tau$ değiştikçe nasıl değiştiğini sistematik olarak gözlemlemek için $\tau$ üzerinde ızgara taraması yapma yaklaşımı.

## Tanım
Klasik Markowitz çerçevesinde portföy optimizasyonu tek bir ufka (genelde örtük olarak günlük) bağlıdır. Multifraktal yapıda ise volatilite ve korelasyon ölçek-bağımlıdır; bu nedenle $\tau$ değiştikçe etkin sınır da değişir. $\tau$ taraması, $\tau \in \{1\text{g}, 1\text{h}, 1\text{a}, 3\text{a}, 1\text{y}, ...\}$ gibi logaritmik ızgarada her bir ufuk için optimizasyonu yeniden çalıştırarak ufukla ağırlıkların ($w(\tau)$), risk seviyelerinin ($\sigma_p(\tau)$) ve fraktal cezanın ($\lambda(\tau), \zeta_q(\tau)$) nasıl evrildiğini ortaya koyar. Tauron projesinin ismi de bu parametreden gelir: $\tau$. Bu tarama, klasik teorinin ufuktan bağımsız olduğunu varsaydığı yerlerde fraktal yapının ufukla nasıl etkileştiğini somutlaştırır.

## Formül
Tarama:
$$
\tau \in \{\tau_1, \tau_2, \dots, \tau_K\}, \qquad \log \tau_{k+1} = \log \tau_k + \Delta
$$
Her $\tau_k$ için:
$$
w^*(\tau_k) = \arg\min_w \big[ w^T \Sigma(\tau_k) w + \kappa \, P_{\text{frac}}(w; \zeta_q(\tau_k), \lambda(\tau_k)) \big]
$$
Burada $P_{\text{frac}}$ [[fraktal-duzeltme-cezasi]] terimidir.

## Ana Bağlamlar
- [[fraktal-duzeltme-cezasi]] ufka-bağımlı ceza
- [[multifraktallik-siddeti-lambda]] her $\tau$'da yeniden ölçülür
- [[zeta-q-olcekleme]] ufka göre değişen üstler
- [[markowitz-paralelligi]] biçim aynı, parametre $\tau$'ya bağlı

## Projelerde Kullanım
- [Tauron](../../projects/tauron/) — projenin ismini taşıyan merkez analiz; simülatörün ana etkileşim parametresi
- [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — ufka göre $H_p$ ve $C_t$ değişiminin gözlemi
- [Seminer](../../projects/) — "yatırım ufku önemlidir" mesajının görsel anlatımı

## Kaynak
[[sornette-multifractal]], [[aygoren-uyar-2023]]
