# Örnek testler

Bu senaryolar akış şemalarını elle izlemek ve karar dallarını doğrulamak için hazırlanmıştır.

## 01 - Öğrenci başarı sistemi

| Girdi | Beklenen sonuç |
|---|---|
| Tür 1, notlar 80 ve 60 | Ortalama 70; İYİ |
| Tür 2, vize 50 ve final 60 | Ağırlıklı ortalama 56; GEÇTİ |
| Tür 2, vize 30 ve final 40 | Ağırlıklı ortalama 36; KALDI |
| Tür 3 veya 0–100 dışında not | Hata mesajı; yeniden giriş |

## 02 - Geometrik hesap ve doğrulama

| Girdi | Beklenen sonuç |
|---|---|
| Tür 1, kenarlar 5 ve 8 | Dikdörtgen alanı 40 |
| Tür 1, kenarlardan biri 0 veya negatif | Hata mesajı; kenarları yeniden iste |
| Tür 2, açılar 60 ve 70 | Üçüncü açı 50 derece |
| Tür 2, açılar 100 ve 90 | Hata mesajı; açıları yeniden iste |

## 03 - Ürün ve komisyon analizi

Komisyon kuralı: fiyatı 50 TL'ye kadar olan ürünlerde `%3`, 50 TL'den büyük ürünlerde `%2`.

| Girdi | Beklenen sonuç |
|---|---|
| 10, 20, 30, 40, 50 | Toplam 150; ortalama 30; komisyon 4.50 |
| 100, 100, 100, 100, 100 | Toplam 500; ortalama 100; komisyon 10 |
| 50, 51, 25, 75, 100 | Her ürün doğru oranla hesaplanır ve toplam komisyon biriktirilir |
| Sıfır veya negatif fiyat | Hata mesajı; aynı ürün yeniden istenir |

## 04 - Sayı analiz aracı

| Girdi | Beklenen sonuç |
|---|---|
| 562 | Pozitif; yüzler 5, onlar 6, birler 2 |
| -347 | Negatif; yüzler 3, onlar 4, birler 7 |
| 0 | Sıfır; üç basamaklı değil |
| 42 veya 1234 | İşaret gösterilir; üç basamaklı olmadığı bildirilir |

## 05 - Faktöriyel hesabı

| Girdi | Beklenen sonuç |
|---|---|
| 0 | `0! = 1` |
| 1 | `1! = 1` |
| 5 | `5! = 120` |
| -3 veya tam sayı olmayan değer | Hata mesajı; yeniden giriş |

## 06 - Tek ve çift sayı istatistikleri

| Girdi | Beklenen sonuç |
|---|---|
| N = 1 | Tek toplam 1, tek çarpım 1, çift toplam 0, çift kare toplam 0 |
| N = 5 | Tek toplam 9, tek çarpım 15, çift toplam 6, çift kare toplam 20 |
| N = 100 | Çift toplam 2550; oynatma listesindeki 1–100 örneğini kapsar |
| N ≤ 0 veya tam sayı olmayan değer | Hata mesajı; yeniden giriş |

## 07 - Çalışan ücret ve yardım sistemi

| Girdi | Beklenen sonuç |
|---|---|
| Tür 1, maaş 20.000, çocuk 0 | Yardım 0; ödenecek tutar 20.000 |
| Tür 1, maaş 20.000, çocuk 2 | Yardım %10 = 2.000; ödenecek tutar 22.000 |
| Tür 1, maaş 20.000, çocuk 3 | Yardım %15 = 3.000; ödenecek tutar 23.000 |
| Tür 2, 40 saat, saat ücreti 100 | Ödenecek tutar 4.000 |
| Tür 2, 45 saat, saat ücreti 100 | 4.000 + 5 × 100 × 2 = 5.000 |
| Negatif maaş, çocuk, saat veya ücret | Hata mesajı; ilgili girişi yeniden iste |

## 08 - Menülü dört işlem

| Girdi | Beklenen sonuç |
|---|---|
| Kod 1, A = 8, B = 2 | Sonuç 10 |
| Kod 2, A = 8, B = 2 | Sonuç 6 |
| Kod 3, A = 8, B = 2 | Sonuç 16 |
| Kod 4, A = 8, B = 2 | Sonuç 4 |
| Kod 4, B = 0 | Sıfıra bölme hatası; yeniden giriş |
| Kod 1–4 dışında | Geçersiz işlem kodu; yeniden giriş |
