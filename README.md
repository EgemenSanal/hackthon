# GÖZPEDİ KALİTE KONTROL SİSTEMİ  



## PROJE TANIMI
Bu sistem, üretim hattındaki medikal göz pedlerinin kalite kontrolünü görüntü işleme ve yapay zeka teknikleriyle otomatik hale getirmeyi amaçlamaktadır. Python backend servisi, gerçek zamanlı analizler yaparak hatalı ürünleri tespit eder. Mobil uygulama ile kullanıcıya anlık bilgi sunulur ve geçmiş analizler takip edilebilir.



## ÖZELLİKLER  

Python Back-end  
LLAMA ile yapay zeka analizi  
Derin Öğrenme  
Görsel İşleme  
REST API desteği  


Mobil Uygulama  
Yapay Zeka  
Android/İOS platformu desteği  
Gerçek Zamanlı Analiz  
Yerel Depolama  
Analiz Geçmişi  
Kamera Entegrasyonu  


## FPS ÖLÇÜMÜ  

Test Süresi: 1 dakika  
İşlenen Görüntü Sayısı: 90 frame  
Ortalama FPS: 1.5  
Test Cihazı: Mobil kamera 1080p  


## ZAMAN VE MEKÂN KARMAŞIKLIĞI
Adım	Zaman Karmaşıklığı	Mekân Karmaşıklığı
Özellik çıkarımı	O(N × M × N)	O(N × D)
SVM eğitimi	O(N × D × min(N, D))	O(N × D)
Tahmin (prediction)	O(D)	O(S × D)


## ALGORİTMA KARMAŞIKLIĞI

Özellik Çıkarımı (extract_features) Her görsel için sabit işlemler:
cv2.cvtColor ve cv2.resize: O(1)

Canny Edge: O(N) (N = toplam piksel = 64x64)

Histogram: O(N)

Simetri (ayna ile fark): O(N)

Flatten: O(N)

Hepsi birlikte O(N) (N: 4096)

Yani: Her görsel için lineer karmaşıklık

Döngüyle Veri Hazırlama O(M x N) (M = Görsel sayısı, N = 4096; yani her görsel için extract_features çağrısı)

Model Eğitimi (SVC) Linear SVM için eğitim karmaşıklığı:

O(M x N x min(M, N)) (sklearn için pratikte; teorik olarak daha az, çünkü linear kernel seçtin)

M: Görsel sayısı (örnek), N: özellik sayısı

Prediction Tek test için: O(N)
Tüm test seti için: O(T x N) (T = test seti uzunluğu)

Bellek (Mekân) Karmaşıklığı Veri matrisi: O(M x N)
SVM Model parametreleri: O(N)

Ortalama RAM: Görüntü başına özellik vektörleri tutulduğu için, büyük veri setlerinde dikkat edilmeli.

Kısaca Sonuç Zaman karmaşıklığı: Özellik çıkarımı için O(M x N) Linear SVM eğitimi için O(M x N x min(M, N))

Mekân karmaşıklığı: O(M x N)

Kodun avantajı: Linear kernel seçildiği için yüksek boyutlu vektörlerde hızlı ve kararlı.

Ekstra: Özellik çıkarımı işlemi sabit olduğu için paralel programlama ile hızlandırılabilir.



## TEKNOLOJİLER  

Python  
Opencv  
LLama  
Numpy  
Joblib  
Sckit-learn  


## MOBİL  

React-Native expo  


## KAMERA ÖZELLİKLERİ  

Desteklenen Kamera Türleri:  
Mobil cihaz kamerası  
Önerilen Çözünürlük: 1080p  
FPS Değeri: 1.5FPS  


## KURULUM TALİMATLARI  


### PYTHON UYGULAMA YÖNERGE  

Reponun Klonlanması  
Python Bağımlılıklarının Yüklenmesi(pip install -r requirements.txt)  
API’yi Başlatın(python api.py)  


### MOBİL UYGULAMA YÖNERGE (REACT NATIVE – EXPO)  

Node.js Yükleyin  
Expo CLI Kurulumu(npm install -g expo-cli)  
Bağımlılıkları Yükleyin(npm install)  
Uygulamayı Başlatın(npx expo start)  
Expo go indirin  
QR kodu okutarak uygulamaya erişin veya build ederek telefona kurun  


## SİMÜLASYON ORTAMI YÖNERGE 

Visual studio ve C# kurulu olmalı  
Unity kurulu olmalı  


## PROJE DETAYLARI  

Takım Adı: Sharingans  

Klasör: Sharingans
Github Kodu :
#ttg5hackathon2025
