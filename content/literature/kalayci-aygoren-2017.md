---
baslik: "Kalayci, Ertenlice, Akyer & Aygören (2017) — ABC ile Kardinalite Kısıtlı Portföy Optimizasyonu"
slug: "kalayci-aygoren-2017"
olusturuldu: 2026-05-13
guncellendi: 2026-05-13
etiketler: [literature, abc, metasezgisel, portfoy, optimizasyon, surul-zekasi]
yazarlar: ["Kalayci, Can B.", "Ertenlice, Okkes", "Akyer, Hasan", "Aygören, Hakan"]
yil: 2017
dergi: "Expert Systems with Applications"
cilt: 85
sayfa: "61-75"
doi: "10.1016/j.eswa.2017.05.018"
citekey: "kalayci2017abc"
turu: makale
fon: "TÜBİTAK 214M224"
kaynak_tipi: akademik
dogrulama: mavi
dogrulama_tarihi: 2026-06-11
hakemler: []
tags: ["dogrulama/mavi"]
---

# Kalayci, Ertenlice, Akyer & Aygören (2017) — ABC ile Kardinalite Kısıtlı Portföy Optimizasyonu

## Künye

Kalayci, C.B., Ertenlice, O., Akyer, H. & Aygören, H. (2017). **"An artificial bee colony algorithm with feasibility enforcement and infeasibility toleration procedures for cardinality constrained portfolio optimization."** *Expert Systems with Applications*, **85**, 61-75. DOI: [10.1016/j.eswa.2017.05.018](https://doi.org/10.1016/j.eswa.2017.05.018). Pamukkale Üniversitesi (Mühendislik EM + İİBF İşletme); TÜBİTAK 214M224 destekli.

## Ana Argüman

Markowitz mean-variance portföy modeline kardinalite kısıtı (portföyde tam K hisse) ve hisse-bazlı alt/üst sınır eklendiğinde problem **NP-Complete sınıfına** geçer (karma tamsayılı kuadratik programlama). Kesin çözüm yöntemleri büyük ölçekte yetersiz; metasezgisel algoritmalar tercih edilir. Yazarlar **Karaboğa (2005) ABC algoritmasını** bu probleme uyarlarken, literatürdeki **repair-only (her infeasible çözümü hemen düzelt)** yaklaşımının lokal optimumda takılma riskini eleştirir; alternatif olarak **karma feasibility enforcement + infeasibility toleration** mekanizması önerirler. Bu yaklaşım arılara çözüm uzayında geçici "kural ihlali" özgürlüğü tanıyarak daha iyi yakınsama sağlar.

## Yöntem

- **Problem:** CCPO ([[cardinality-constrained-portfolio]]) — Chang ve diğerleri (2000) formülasyonu temel alınmış; $\lambda$-ağırlıklı risk-getiri trade-off, eşitlik kısıtları (toplam ağırlık=1, hisse sayısı=K), eşitsizlik kısıtları (alt/üst sınır)
- **Algoritma çekirdeği:** [[artificial-bee-colony]] — employed/onlooker/scout arı fazları (Karaboga, 2005)
- **Yenilik (ABC-II):** Repair Procedure II — sadece hard constraint'leri (Eq. 2-3) zorla, alt/üst sınırı (Eq. 4) yumuşak kısıt olarak tolere et; Evaluation Procedure II — fitness'a `violation_value` ile ceza ekle
- **Parametre kalibrasyonu:** Full factorial DOE — optimum `modification_rate = 0.1`, `scout_production_period = 0.1·N`, `limit = 1·N`
- **Veri:** OR-Library 5 benchmark (Hang Seng 31, DAX 100 85, FTSE 100 89, S&P 100 98, NIKKEI 225) + BIST 2 yerel set (XU030 30, XU100 99). Türkiye verisinin literatüre dahili Aygören Hoca katkısı.
- **Metrikler:** MEAPE, MEDPE, MINPE, MAXPE (Chang); VRE-I, MRE-I (Fernández); MEUCD, VRE-II, MRE-II (Cura)

## Bulgular

1. ABC-II, ABC-I'yi tüm veri setlerinde %17-72 iyileştirme ile geçer (Tablo 4); BIST XU030'da en yüksek iyileşme (%64-73)
2. Literatürdeki GA, TS, SA (Chang 2000), PSO (Deng 2012), PBILDE (Lwin 2013), GRASP-QP (Baykasoğlu 2015) ile karşılaştırıldığında rekabetçi veya daha iyi performans
3. Tuba & Bacanin (2014a) ABC+Firefly hibrit'inden daha yavaş olsa da ortalama yakınsama metriklerinde üstün
4. Az parametre + parametre duyarlılığı düşük → yazılım uygulanabilirliği yüksek
5. Pareto efficient frontier'a yakınsama ABC-II'de görsel olarak da daha sıkı (Şekil 10-11)

## Etkisi

- **Akademik:** PAÜ kaynaklı interdisipliner çalışma (EM + İşletme); CCPO için metasezgisel literatüre Türkiye yerel verisini ekler
- **Yöntem felsefesi:** "Sıkı kural uygulama vs. esneklik" trade-off'una somut bir mühendislik cevabı — bu yaklaşım diğer kısıtlı optimizasyon problemlerine genelleştirilebilir
- **Aygören Hoca'nın portföyü:** [[aygoren-uyar-2023]] fraktal piyasa hipotezi makalesinden farklı bir yöntemsel ailede ama aynı amaç (gerçekçi portföy optimizasyonu); Hoca'nın metasezgisel algoritma + finans kesişimindeki konumunu pekiştirir
- **Gelecek araştırma:** İşlem maliyetleri, vergi, sektör çeşitlendirme kısıtları, multi-objective Pareto yaklaşımları
- **Atelier projeleri için:** [[obsidian-abc-arastirma]] projesinin ana referansı; Yiğit Kumral'ın Obsidian Smart Connections embedded vektörler ile ABC arasında sentez sorusu bu makaleyi merkezine alır.

## İlgili Kavramlar

- [[artificial-bee-colony]] — algoritmanın çekirdeği
- [[cardinality-constrained-portfolio]] — problem tanımı
- [[metaheuristic-optimization]] — algoritma ailesi
- [[swarm-intelligence]] — paradigma
- [[markowitz-portfoy-teorisi]] — temel
- [[aygoren-uyar-2023]] — Hoca'nın diğer makalesi (fraktal piyasa)
- [[np-complete]] — hesaplama karmaşıklığı (vault'ta varsa)

## Atıf Yapan Projeler

- [Obsidian-ABC Araştırma](../../projects/obsidian-abc-arastirma/) — Bu proje ana referans olarak kullanır
- Potansiyel ilgi: [Tauron](../../projects/tauron/) ve [Fractal Portfolio Analysis](../../projects/fractal-portfolio-analysis/) — Markowitz çerçevesinde Hoca'nın yöntemsel çeşitliliğini gösterir

## Sornette/Multifraktal ile İlişki

Bu makalede çözüm yöntemi metasezgiseldir — Sornette'nin teorik multifraktal yaklaşımının aksine, ampirik/algoritmik. İki yaklaşım [[tauron]] projesinde karşılaştırılabilir: ABC + multifraktal kovaryans = uygulamada yeni bir hibrit deneme.
