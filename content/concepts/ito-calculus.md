---
baslik: "Itô Kalkülüsü"
slug: "ito-calculus"
olusturuldu: 2026-05-10
guncellendi: 2026-05-10
etiketler: [matematik, stokastik-analiz]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Itô Kalkülüsü

## Özü
Türevsiz Wiener yörüngeleri üzerinde tanımlı stokastik integraller ve değişken-değişimi formülünü sağlayan kalkülüs çerçevesidir.

## Tanım
[[brownian-motion-wiener]] sürecinin yörüngeleri klasik anlamda diferansiyellenemediği için Riemann-Stieltjes integrali tanımsız kalır; Itô bu eksikliği "sol-uç" toplam yaklaşımıyla çözer ve uyumlu bir stokastik integral inşa eder. Itô lemması, $f(t, X_t)$ dönüşümlerinin diferansiyelini hesaplarken $(dW_t)^2 = dt$ kuralını kullanan ikinci dereceden bir Taylor açılımıdır; bu ek terim klasik kalkülüsten en önemli ayrışma noktasıdır. Tüm sürekli-zaman türev fiyatlama (örn. [[black-scholes]] PDE'si) Itô lemmasının doğrudan uygulamasıdır.

## Formül
Itô lemması, $X_t$ bir Itô süreci ve $f \in C^{1,2}$ ise:
$$
df(t, X_t) = \frac{\partial f}{\partial t}dt + \frac{\partial f}{\partial x}dX_t + \frac{1}{2}\frac{\partial^2 f}{\partial x^2}(dX_t)^2
$$
ve $(dW_t)^2 = dt$, $dt \cdot dW_t = 0$, $(dt)^2 = 0$ kuralları geçerlidir.

## Ana Bağlamlar
- [[brownian-motion-wiener]] — kalkülüsün üstüne kurulduğu süreç
- [[geometric-brownian-motion]] — Itô lemması ile çözülen tipik SDE
- [[black-scholes]] — PDE türetimi Itô lemmasıyla yapılır
- [[euler-maruyama]] — sayısal SDE diskretizasyonu

## Projelerde Kullanım
- [Seminer](../../projects/ders/2026-bahar-seminer/) — stokastik analizin pedagojik temeli
- [Quantum Computing](../../projects/herman-2026-ceviri-egitim/) — kuantum SDE simülasyonunun matematiksel altyapısı

## Kaynak
[[hull-2008]]
