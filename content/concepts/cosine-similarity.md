---
baslik: "Kosinüs Benzerliği (Cosine Similarity)"
slug: "cosine-similarity"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [matematik, vektor, benzerlik-metrik, ml]
aliases: ["cosine similarity", "cos similarity", "kosinüs benzerliği"]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Kosinüs Benzerliği

İki vektör arasındaki **açının kosinüsü** ile ölçülen benzerlik metriği. Yüksek boyutlu [[embedding-vektor|embedding uzaylarında]] [[semantic-search|semantik arama]] için standart ölçüt.

## Matematiksel Tanım

$$\text{cos\_sim}(\mathbf{a}, \mathbf{b}) = \frac{\mathbf{a} \cdot \mathbf{b}}{\|\mathbf{a}\| \cdot \|\mathbf{b}\|}$$

- Aralık: $[-1, 1]$ (genel vektörler için), genelde $[0, 1]$ (pozitif embedding'lerde)
- Değerler:
  - $1$ = tam aynı yön (en benzer)
  - $0$ = dik (ilişkisiz)
  - $-1$ = zıt yön

## Neden Cosine?

| Metrik | Avantaj | Dezavantaj |
|---|---|---|
| **Cosine** | Vektör uzunluğundan bağımsız; yön odaklı | Mutlak büyüklük kaybolur |
| Euclidean | Büyüklük + yön | Yüksek boyutta [[boyutluluk-laneti|patlar]] |
| Dot product | Hızlı (normalize edilmiş) | Uzunluk etkisi var |
| Manhattan (L1) | Robust | Yön bilgisi zayıf |

Embedding'lerde **modeller cosine'a göre eğitilir** (contrastive loss) — bu nedenle cosine doğal ölçü olur.

## Hesaplama Örneği

İki cümle embedding'i:
- $\mathbf{a} = [0.2, 0.5, 0.1, ...]$ (384 boyut)
- $\mathbf{b} = [0.3, 0.4, 0.2, ...]$

$\text{cos\_sim} = \frac{0.06 + 0.20 + 0.02 + ...}{\sqrt{...} \cdot \sqrt{...}}$ → örneğin 0.87

Cosine 0.87 = "çok benzer" (Smart Connections tipik eşik: 0.5-0.6 üstü "related" sayılır).

## Smart Connections Bağlamı

Obsidian Smart Connections panelinde her note için skor cosine similarity'dir; varsayılan eşik ~0.5. Skorlar normalize edilerek listelenir, kullanıcı en yakın K notu görür.

## Portföy Optimizasyonu Bağlantısı (Olası)

Stock embedding literatüründe (Dolphin 2022, SimStock 2024) cosine similarity hisse senetleri arasındaki anlamsal/davranışsal yakınlığı ölçmek için kullanılıyor — klasik [[kovaryans-matrisi|kovaryans matrisi]] alternatifi. Bu yaklaşım [[artificial-bee-colony|ABC]] tabanlı [[cardinality-constrained-portfolio|CCPO]] çözümünde fitness fonksiyonuna eklenebilir (semantic diversification penalty, [Obsidian-ABC](../../projects/obsidian-abc-arastirma/) projesi E3 sentez ekseni).

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — Smart Connections semantic skor; potansiyel ABC fitness entegrasyonu

## İlgili Kavramlar

- [[embedding-vektor]]
- [[semantic-search]]
- [[kovaryans-matrisi]]
- [[boyutluluk-laneti]]
