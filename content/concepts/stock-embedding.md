---
baslik: "Hisse Senedi Embedding'i (Stock Embedding)"
slug: "stock-embedding"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [finans, embedding, portfoy, ml, alternatif-temsil]
aliases: ["stock embedding", "asset embedding", "hisse embedding"]
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Hisse Senedi Embedding'i

**Finansal varlıkların** (hisse senedi, ETF, kripto, vb.) **yüksek boyutlu dense vektör temsili** — getiri zaman serisi, haber metni veya işlem örüntülerinden öğrenilen [[embedding-vektor|embedding]] yaklaşımının finansa uygulanmış hali.

Geleneksel finansta hisse senetleri **kovaryans matrisi** ile temsil edilir; stock embedding bu temsile **veri-driven, anlamsal ek katman** sağlar.

## Üretim Yöntemleri

| Yöntem | Veri Kaynağı | Örnek |
|---|---|---|
| **Word2Vec analoji** | Günlük getiriler (context window) | Dolphin et al. (2022) |
| **Multimodal** | Getiri + haber metni | ACL 2020 (news + price) |
| **Contrastive learning** | Time-series pencereleri | SimStock (2024), arXiv 2407.18645 |
| **Transformer encoder** | Sequence of returns | Encoding Stock Returns (Springer 2024) |

## Geleneksel Kovaryans Matrisiyle Karşılaştırma

| Boyut | [[kovaryans-matrisi\|Kovaryans]] | Stock Embedding |
|---|---|---|
| Boyut sayısı | N (hisse sayısı) | 64-256 (öğrenilmiş dim) |
| Hesaplama | Tarihsel getiri varyans | NN eğitimi |
| Bilgi türü | İstatistiksel (linear) | Semantik / non-linear |
| Sektör bilgisi | Yok (sayısal) | Var (haber/context'ten gelir) |
| Yenilenme | Her dönem (rolling) | Dönemsel re-train |

## Portföy Optimizasyonunda Kullanımı

1. **Çeşitlendirme:** Embedding uzayında uzak hisseler "semantik olarak farklı" → daha iyi çeşitlendirme
2. **Sektör sınıflandırma:** Klasik GICS gibi subjektif sınıflandırmalara veri-driven alternatif
3. **Korelasyon proxy:** Cosine similarity korelasyon yerine kullanılabilir (SimStock 2024)
4. **Hedge oluşturma:** Anti-similar hisseler doğal hedge

## Kritik Soru: ABC ile Birleşim

[[kalayci-aygoren-2017|Kalayci-Aygören 2017 ABC tabanlı CCPO çalışması]] sayısal getirileri kullanır, **embedding kullanmaz**. Stock embedding literatürü ise klasik kuadratik programlama (QP) ile çalışır, **metasezgisel kullanmaz**. Bu kesişim **literatürde doldurulmamış**:

> **Hipotez (E3 sentez ekseni):** [[artificial-bee-colony|ABC]] algoritmasının fitness fonksiyonuna stock-embedding tabanlı **semantic diversification penalty** eklenirse, [[cardinality-constrained-portfolio|CCPO]] çözümleri daha iyi çeşitlendirilmiş olabilir mi?

$$F_{yeni}(w) = F_{Markowitz}(w) + \gamma \cdot \text{SemanticConcentration}(w, E)$$

burada $E$ stock embedding matrisi, $\gamma$ ağırlık parametresi.

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — Hocaya sunulacak rapor için **en güçlü sentez adayı**

## Kaynak

- Dolphin, R., Smyth, B., Dong, R. (2022). "Stock Embeddings: Learning Distributed Representations for Financial Assets." arXiv:2202.08968
- SimStock — Temporal Representation Learning for Stock Similarities (2024). arXiv:2407.13751
- Stock Embeddings from News Articles and Price History (ACL 2020)
- Encoding Stock Returns Relationships via Latent Embeddings (Springer 2024)

## İlgili Kavramlar

- [[embedding-vektor]]
- [[cosine-similarity]]
- [[cardinality-constrained-portfolio]]
- [[artificial-bee-colony]]
- [[kovaryans-matrisi]]
- [[markowitz-portfoy-teorisi]]
