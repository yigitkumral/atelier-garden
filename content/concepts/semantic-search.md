---
baslik: "Semantik Arama (Semantic Search)"
slug: "semantic-search"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [bilgi-erisimi, embedding, retrieval, neural-arama]
aliases: ["semantic search", "anlamsal arama", "vector search", "neural search"]
kaynak_tipi: diger
dogrulama: kirmizi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/kirmizi"]
---

# Semantik Arama

**Anlamsal benzerliğe dayalı bilgi erişim yöntemi.** Klasik anahtar kelime aramasından farklı olarak, sorgu ve dokümanlar [[embedding-vektor|yüksek boyutlu vektörlere]] dönüştürülür ve [[cosine-similarity|cosine similarity]] gibi metriklerle yakınlık ölçülür. "Benzer anlamlı" notlar, kelimeler ayna olmadan da bulunur.

## Klasik vs Semantik Arama

| Boyut | Klasik (BM25, TF-IDF) | Semantik (Vector) |
|---|---|---|
| Eşleşme türü | Lexical (kelime) | Semantic (anlam) |
| Tip metni | "kar yağışı" araması "snow" bulamaz | "kar yağışı" araması "winter precipitation" bulur |
| Hız | Çok hızlı (inverted index) | Daha yavaş (vector distance) |
| Donanım | CPU yeterli | GPU/optimized index önerilir |
| Hibrit | — | BM25 + vector (RRF, weighted) yaygın |

## Çalışma Akışı

1. **İndeksleme:** Tüm dokümanlar embedding modelinden geçer, vektörler vektör veritabanına kaydedilir
2. **Sorgu:** Kullanıcının sorgusu aynı modelle vektöre dönüştürülür
3. **Arama:** Yaklaşık k-NN (FAISS, HNSW, Annoy) ile en yakın K vektör bulunur
4. **Sıralama:** Cosine score'a göre sıralanır

## Obsidian Smart Connections Bağlamı

Smart Connections 4.5.0:
- Embedding modeli: Multilingual E5 Small (384 dim, [[embedding-vektor]])
- İndeksleme: yerel `.smart-env/multi/` cache (her not için ajson)
- Sorgu: kullanıcı bir not açtığında, o notun embedding'i ile diğer notlar karşılaştırılır
- Görüntüleme: "show related notes" paneli, score sırasıyla

## Foraging Metaforuyla Bağlantı

Semantik arama [[swarm-intelligence|sürü zekası]] literatüründe "foraging" benzeri tanımlanır: kullanıcı current note (kaynak) civarında semantic neighborhood'u keşfeder. Bu metaforik paralellik [[artificial-bee-colony|ABC algoritmasının]] employed/onlooker davranışına yapısal benzerlik gösterir — ancak temel mekanizma farklıdır (semantic search statik retrieval, ABC dinamik iteratif optimizasyon).

## Akademik Kullanım

- Literatür incelemesi (literature discovery)
- Atıf önerisi (citation recommendation)
- Konu kümeleme (topic clustering)
- Cross-domain bağlantı keşfi (interdisipliner)

## Projelerde Kullanım

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — Smart Connections semantic arama mekanizması proje merkezi sorusunda
- Atelier vault'unda 105+ atomic notun semantic arama altyapısı

## Kaynak

- Reimers, N., Gurevych, I. (2019). "Sentence-BERT: Sentence Embeddings using Siamese BERT-Networks." EMNLP
- ACM CSAIDE (2025). Survey of Swarm Intelligence Approaches to Search Documents Based on Semantic Similarity

## İlgili Kavramlar

- [[embedding-vektor]]
- [[cosine-similarity]]
- [[swarm-intelligence]]
- [[boyutluluk-laneti]]
