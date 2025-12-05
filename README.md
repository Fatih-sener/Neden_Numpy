# Performans Testi: Python Listeleri vs. NumPy Dizileri

Bu script, büyük ölçekli matematiksel işlemlerde standart Python döngüleri (`for loop`) ile NumPy kütüphanesinin **vektörizasyon** yeteneği arasındaki performans farkını (execution time) ölçer.

## Test Metodolojisi
Kod, 1.000.000 adet sayının 100. kuvvetini hesaplamak için iki farklı yöntem kullanır ve işlem sürelerini kıyaslar:

1.  **Iterative Approach (Standart Python):**
    * `for` döngüsü kullanılarak her sayı tek tek işlenir.
    * Sonuçlar standart bir listeye (`list`) eklenir.
2.  **Vectorized Approach (NumPy):**
    * `np.arange()` ile oluşturulan dizi üzerinde vektörel işlem yapılır.
    * Döngü kullanılmadan tüm dizi tek seferde işlenir (C tabanlı optimizasyon).

## ⏱️ Beklenen Sonuçlar
NumPy yaklaşımı, bellek yönetimi (contiguous memory) ve optimize edilmiş C backend'i sayesinde standart Python döngüsüne göre **yaklaşık 50-100 kat daha hızlı** çalışmaktadır.
