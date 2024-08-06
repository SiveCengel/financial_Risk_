Giriş
Bu proje, müşterilerin finansal risk seviyelerini tahmin etmek amacıyla çeşitli demografik ve finansal verileri kullanarak makine öğrenmesi modelleri oluşturmayı amaçlamaktadır. Veriler, müşterilerin yaş, cinsiyet, eğitim düzeyi, gelir, kredi skoru gibi bilgilerini içermektedir. Projenin amacı, hangi müşterilerin daha yüksek risk taşıdığını belirlemek ve bu bilgiler doğrultusunda finansal kararlar almayı kolaylaştırmaktır.
Veri Seti
Veri seti, çeşitli demografik ve finansal bilgileri içermektedir. Veri setindeki temel özellikler arasında yaş, cinsiyet, eğitim düzeyi, medeni durum, gelir, kredi skoru, kredi miktarı, kredi amacı, çalışma durumu, mevcut işte geçen yıl sayısı, ödeme geçmişi, gelir-borç oranı, varlık değeri, bağımlı kişi sayısı, şehir, eyalet, ülke, önceki temerrütler, medeni durum değişikliği ve risk derecesi bulunmaktadır.Bu veri setinde 15000 satır, 20 kolon bulunmaktadır. Kolon isimleri aşağıda açıklamalarıyla belirtilmiştir.
•	Age: Kişinin yaşı.
•	Gender: Kişinin cinsiyeti. 
•	Education Level: Kişinin en yüksek eğitim seviyesi. 
•	Marital Status: Kişinin medeni durumu. 
•	Income: Kişinin yıllık geliri. 
•	Credit Score: Kişinin kredi skoru. 
•	Loan Amount: Talep edilen veya verilen kredi miktarı. 
•	Loan Purpose: Kredinin amacı. 
•	Employment Status: Kişinin istihdam durumu. 
•	Years at Current Job: Kişinin mevcut işinde geçirdiği yıl sayısı. 
•	Payment History: Ödeme geçmişi. 
•	Debt-to-Income Ratio: Borcun gelire oranı. 
•	Assets Value: Kişinin toplam varlık değeri. 
•	Number of Dependents: Kişinin bakmakla yükümlü olduğu kişi sayısı. 
•	City: İkamet edilen şehir. 
•	State: İkamet edilen eyalet. 
•	Country: İkamet edilen ülke. 
•	Previous Defaults: Önceki kredi temerrüt sayısı. 
•	Marital Status Change: Medeni durum değişiklikleri. 
•	Risk Rating: Kişinin risk derecesi.


Yöntem
Veri seti üzerinde ilk olarak ön işleme adımları uygulanmıştır. Eksik veriler Simple Imputer ile doldurulmuş, sayısal veriler Min Max Scaler ile normalize edilmiş ve kategorik veriler One Hot Encoding yöntemiyle işlenmiştir. Verilerin temizlenmesi ve işlenmesi sonrasında, çeşitli makine öğrenmesi modelleri kullanılarak risk tahmini yapılmıştır.
Modeller
Proje kapsamında aşağıdaki modeller kullanılmıştır:

1. Lojistik Regresyon: İlk model olarak kullanılmıştır. Müşterilerin risk seviyelerini tahmin etmek için basit bir model olarak tercih edilmiştir.

2. Dummy Classifier: Karşılaştırma amacıyla kullanılmıştır. Bu model, sınıflandırma doğruluğunu değerlendirmek için basit bir referans model olarak kullanılmıştır.

3. Karar Ağaçları:  Farklı hiperparametre ayarları (max depth, max leaf nodes) ile denenmiştir. Bu model, karar ağaçlarının şeffaf yapısı sayesinde risk tahminlerinde belirli değişkenlerin önemini anlamayı kolaylaştırmıştır.

4. Random Forest: Birden fazla karar ağacının birleşiminden oluşan bu model, daha doğru tahminler elde etmek için kullanılmıştır.
Özet
Model sonuçlarına göre en iyi performansı “Random Forest” modeli vermiştir. Bu model, test verisi üzerinde en yüksek doğruluğu ve en düşük hata oranını sağlamıştır. Karar ağaçları modelleri de iyi sonuçlar vermiş olsa da, Random Forest modeli birden fazla ağacı kullanarak daha sağlam ve tutarlı sonuçlar elde etmiştir.

Lojistik regresyon modeli ve Dummy Classifier modelleri, diğer modellere göre daha düşük performans sergilemiştir. Özellikle Dummy Classifier, basit bir referans noktası olarak, diğer modellerin doğruluğunu değerlendirmede kullanılmıştır.
Sonuç
Bu proje kapsamında farklı makine öğrenmesi modelleri kullanılarak müşterilerin finansal risk seviyeleri tahmin edilmiştir. En iyi sonuçları veren model Random Forest modeli olmuştur. Bu model, veri setinin özelliklerini iyi bir şekilde modelleyerek yüksek doğruluk oranları elde etmiştir. Gelecekteki çalışmalarda, daha fazla veri ve özellik ekleyerek modellerin doğruluğunu artırmak mümkün olabilir.

 
