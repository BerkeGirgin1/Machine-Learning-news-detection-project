# **Machine Learning News Detection Project**

## **Projenin Amacı**
Bu projede amaç, haberlerin gerçek mi yoksa sahte mi olduğunu tahmin etmek için makine öğrenmesi tekniklerini kullanarak bir model geliştirmektir. Projede, haberlerin **site URL'si**, **haber metni**, **başlık**, **yazar** ve **dil** gibi özellikler analiz edilip sayısallaştırılarak, bu veriler üzerinden **Logistic Regression** ve **KMeans** gibi algoritmalar uygulanmaktadır. Nihai hedef, bu özellikleri kullanarak haberlerin doğruluğunu otomatik olarak sınıflandıran bir sistem oluşturmak ve sahte haberlerin tespit edilmesini sağlamaktır.

---

## **Veri Seti**
Bu veri seti, haberlerin sahte veya gerçek olup olmadığını belirlemek için çeşitli özellikleri içermektedir. Aşağıda veri setindeki sütunlar ve açıklamaları bulunmaktadır:

- **author**: Haberi yazan kişinin adı veya takma adı.
- **published**: Haber makalesinin yayınlanma tarihi ve saati.
- **title**: Haber makalesinin başlığı.
- **text**: Haber makalesinin tam metni.
- **language**: Haber makalesinin yazıldığı dil (örneğin, İngilizce).
- **site_url**: Haberin yayımlandığı web sitesinin URL'si.
- **main_img_url**: Haberde kullanılan ana resmin URL'si.
- **type**: Haberin türü (örneğin, "bias" olarak etiketlenmiş).
- **label**: Haberin gerçek (**Real**) veya sahte (**Fake**) olduğunu belirten etiket.
- **title_without_stopwords**: Başlıktan durdurma kelimeleri çıkarılmış hali.
- **text_without_stopwords**: Metinden durdurma kelimeleri çıkarılmış hali.
- **hasImage**: Haber makalesinde görsel olup olmadığını gösteren bir bayrak (**1**: var, **0**: yok).

---

## **Model Seçimi**
1. **Logistic Regression**:  
   Haber makalelerinin gerçek veya sahte olma durumunu tahmin etmek için kullanılan gözetimli bir sınıflandırma algoritmasıdır. Bu model, metin verileri ve diğer özellikler kullanılarak eğitilmiş ve doğruluk oranı ile ölçülmüştür.

2. **KMeans**:  
   Gözetimsiz öğrenme algoritmalarından biri olan KMeans, haberleri kümeleyerek gruplayıp hangi haberlerin sahte veya gerçek olduğunu kümeleme yaklaşımı ile belirlemeye çalışır. Bu model, metin özelliklerine dayalı olarak verileri iki kümeye ayırır.

Her iki modelin de performansları karşılaştırılmış ve model sonuçlarına göre değerlendirilmiştir. **Logistic Regression**, denetimli bir yöntem olarak daha iyi performans göstermiştir. **KMeans** ise farklı küme sayılarıyla denenmiş, ancak denetimsiz bir yöntem olması nedeniyle sınıflandırma performansı düşük kalmıştır.

### https://www.kaggle.com/models/berkegirgin/news_detection/
