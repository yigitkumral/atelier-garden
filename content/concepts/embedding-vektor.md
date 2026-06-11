---
baslik: "Embedding Vektörü (Embedding Vector / Yoğun Temsil)"
slug: "embedding-vektor"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [makine-ogrenmesi, vektor, neural-network, temsil-ogrenme]
aliases: ["embedding", "embedding vector", "yoğun temsil", "dense representation"]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Embedding Vektörü

**Yapay sinir ağı (neural network) ile öğrenilmiş, yüksek boyutlu yoğun (dense) vektör temsili.** Metin, ses, görsel veya kategorik veriyi sayısal uzayda ifade eder; benzer girdiler birbirine yakın konumlanır.

[[boyutluluk-laneti|Yüksek boyutlu uzaylar]] ile akrabadır — tipik 384, 768, 1024, 1536 boyut.

## Sınıflandırma

| Tür | Örnekler | Bağlam |
|---|---|---|
| **Statik word embedding** | Word2Vec (Mikolov 2013), GloVe (Pennington 2014), FastText | Her kelimenin tek vektörü |
| **Kontekstüel embedding** | BERT (Devlin 2018), RoBERTa, GPT family | Bağlama göre değişen vektör |
| **Sentence/paragraph embedding** | Sentence-BERT, Multilingual E5 | Cümle/paragraf seviyesinde tek vektör |
| **Multimodal embedding** | CLIP (görsel + metin) | Farklı modaliteler aynı uzayda |
| **Domain-specific** | Stock embedding (Dolphin 2022) | Finansal time-series için özel |

## Klasik ML Feature Vektörlerinden Farkı

| Boyut | Klasik Feature | Embedding |
|---|---|---|
| Üretim | Manuel (uzman mühendisliği) | Öğrenme (NN) |
| Yoğunluk | Sparse (çoğu 0) | Dense (tüm boyutlar anlamlı) |
| Yorumlanabilirlik | Yüksek (her boyut bilinir) | Düşük (latent uzay) |
| Boyut | 10-100 | 384-2000+ |

## Smart Connections'da

Obsidian Smart Connections eklentisi **Multilingual E5 Small** modelini kullanır — 384 boyutlu sentence-level embedding. Her not bir vektörle temsil edilir; sorgular [[semantic-search|semantik arama]] ile en yakın K notu döndürür ([[cosine-similarity|cosine similarity]] metriğiyle).

## Makine Öğrenmesi İçinde Yeri

Embedding kesinlikle ML'in alt-ailesidir: neural network ile üretilen yoğun temsillerdir. Klasik "ML feature" kavramından farkı *otomatik öğrenme*'dir.

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — Smart Connections embedding'lerinin ABC algoritmasıyla potansiyel sentezi araştırılıyor; "semantic fitness function" hipotezi (E3 ekseni)
- Atelier vault'unun semantic arama altyapısı

## Kaynak

- Mikolov, T., Chen, K., Corrado, G., Dean, J. (2013). "Efficient Estimation of Word Representations in Vector Space." arXiv:1301.3781
- Devlin, J., Chang, M.W., Lee, K., Toutanova, K. (2018). "BERT: Pre-training of Deep Bidirectional Transformers." arXiv:1810.04805
- Wang, L. ve diğerleri (2024). "Text Embeddings by Weakly-Supervised Contrastive Pre-training" (E5). arXiv:2212.03533

## İlgili Kavramlar

- [[cosine-similarity]]
- [[semantic-search]]
- [[boyutluluk-laneti]]
- [[stock-embedding]]
