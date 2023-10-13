# Turkiye-Is-Bankasi-ML-Challenge5

## Overview
Bir mobil uygulamanın kullanım verileriyle bir yapay zeka modeli geliştirerek her bir kullanıcıya o uygulamada en çok ihtiyaç duyacağı menüyü önermenizdir. Veri setinde hedef olarak, her bir kullanıcının geçmiş kullanımında tercih ettiği menüleri binary olarak belirten 9 tane menü yer almaktadır. Bu 9 menüden hangi 3 tanesinin kullanıcı arayüzüne ekleneceğini tahminlemeniz gerekmektedir.

## Evaluation
Metrik kriteri olarak Jaccard Score belirlenmiştir. Her bir menünün önerilip önerilmeyeceğini gösteren 9 adet binary değerden oluşan tahminleriniz bu metrik ile kıyaslanacaktır. Yarışma tamamlandığında Private Leaderboard'da toplamda en iyi tahmin skoruna önce ulaşan yarışmacı final sunumu yapmaya hak kazanacaktır.

Örnek çıktı şu şekildedir:
Müşteri A -> 000101010 (Müşteri A’ya 4., 6., ve 8. Menüler önerilmesi tahminlenmiştir.)
Müşteri B -> 100000011 (Müşteri A’ya 1., 8., ve 9. Menüler önerilmesi tahminlenmiştir.)
*Tahminlerin yalnızca 3 adet menüyü içermesi gerekmektedir.

![image](https://www.googleapis.com/download/storage/v1/b/kaggle-user-content/o/inbox%2F4892477%2Faa0b1ca8db259ef7cf9967544de9185a%2FScreenshot%202023-09-25%20at%2018.26.16.png?generation=1695655590746328&alt=media)

## Dataset Description
### AÇIKLAMALAR
#### Train ve Test Veri Setleri

**ID**
Maskelenmiş müşteri ID'si

**MONTH**
İşlemin yapıldığı ay

**N_SECONDS_[*]**
Menülerde geçirilen süre (target sıralaması ile verilmiştir.)

**CARRIER**
İşlemin yapıldığı telefon hattı

**DEVICEBRAND**
İşlemin yapıldığı cihazın markası

**FEATURE_[*]**
Müşteriye has verileri temsil eden maskelenmiş öznitelikler

**TARGET**
Müşterinin belirli bir ayda en çok vakit geçirdiği 3 menü

#### Submission Dosyası

**ID**
Tahminlenmesi beklenen maskelenmiş müşteri ID'si

**TARGET**
0-1 değerlerinden oluşan menüleri tanımlayan değer

#### Dış Veri Kullanımı

Dönemsel enflasyon verisi, maaş ödenme günleri, (SGK ve devlet memurlarının maaş günleri vb…), resmi ve dini bayramlara ilişkin veriler, döviz kurları, mevsime göre ülkemizde görülen ortalama sıcaklık verileri gibi modelin kurulumunda size faydalı olabileceğini düşündüğünüz her türlü dış veriyi kullanabilirsiniz.
