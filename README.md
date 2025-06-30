# Knapsack Algoritması Performans Analizi

Bu proje, farklı Knapsack algoritmalarının çeşitli problem boyutlarındaki çalışma sürelerini ve verimliliklerini karşılaştırmalı olarak analiz eder. Çalışma Python ile gerçekleştirilmiş, algoritmaların performansı görsel grafiklerle desteklenmiştir.

## Proje Sahibi

Zeynep Gülten 
10 Haziran 2025


##  Proje Yapısı

```bash
knapsack-performance-analysis/
│
├── data/                   # Test edilen problem dosyaları
│   ├── ks_40_0
│   ├── ks_300_0
│   ├── ks_1000_0
│   └── ks_10000_0
│
├── results/                # Görseller ve test çıktıları
│   ├── knapsack_performance.png
│   └── knapsack_sonuclar.csv
│
├── report/                 # PDF formatında rapor
│   └── RAPOR3.pdf
│
├── notebook/               # Python Jupyter Notebook
│   └── Untitled5.ipynb
│
└── README.md               # Bu dosya



## Amaç

- Knapsack problemi için uygun algoritma seçim stratejisini belirlemek.
- Problem boyutu, kapasite ve hafıza sınırlarına göre **adaptif algoritma seçimleri** uygulamak.
- Python ile algoritmaların performansını ölçmek ve görselleştirmek.

---

##  Kullanılan Algoritmalar

| Algoritma            | Kullanım Durumu                                  |
|----------------------|--------------------------------------------------|
| Standart DP          | Küçük problemler (n ≤ 100)                       |
| Hafıza Verimli DP    | Orta büyüklükte problemler (100 < n ≤ 2000)      |
| Greedy               | Büyük problemler veya yüksek hafıza gereksinimi  |

---

## Sonuç Özeti

| Problem Boyutu | Algoritma           | Süre (saniye) | Verimlilik (%) |
|----------------|----------------------|---------------|-----------------|
| 40             | Standart DP          | 0.8982        | 99.84           |
| 300            | Greedy               | 0.0002        | 99.99           |
| 1000           | Hafıza Verimli DP    | 32.5982       | 99.97           |
| 10000          | Greedy               | 0.0060        | 100.00          |

- En büyük fark: **n=300 (0.0002s)** ile **n=1000 (32.6s)** arasında → **~163.000 kat**

---

## Öne Çıkan Bulgular

- Hafıza sınırlamaları algoritma seçiminde kritik rol oynar.
- Greedy algoritma beklenenden çok daha başarılı sonuçlar vermiştir.
- Hafıza verimli DP, maliyetli olmasına rağmen kaliteli çözümler üretmiştir.
- **Adaptif yaklaşım**, her problem boyutuna uygun en iyi algoritmayı seçmede oldukça başarılıdır.

---

##  Görsel Örnek

![Knapsack Performans Grafiği](/knapsack_performance.png)

---

## Rapor

Detaylı açıklamalar ve analizler için:  
 `report/RAPOR3.pdf`

---

##  Not

Bu proje ders kapsamında hazırlanmış olup akademik kullanım amaçlıdır.

---

##  Lisans

Bu proje açık kaynak değildir. İzinsiz kopyalanamaz.
