# 🤖 El İşareti Tespit Projesi

Bu proje, yapay zeka kullanarak el işaretlerini tanımlayan bir sistem geliştirmeyi amaçlamaktadır. OpenCV, MediaPipe ve TensorFlow kullanılarak el hareketleri tespit edilerek analiz edilir.

## 🎯 Özellikler
- 🖐️ Gerçek zamanlı el işareti algılama
- 📷 Kamera ile anlık görüntü işleme
- 🧠 Makine öğrenmesi modeli ile doğruluk analizi
- 🔍 Önceden belirlenmiş el işaretlerinin tespiti ve sınıflandırılması

## 🚀 Kurulum

Bu projeyi çalıştırmak için aşağıdaki adımları takip edebilirsiniz:

### 📌 Gerekli Bağımlılıkları Kurun

```bash
pip install opencv-python mediapipe tensorflow numpy scikit-learn
```

### 📂 Projeyi Klonlayın
```bash
git clone <repository-url>
cd <repository-folder>
```

## 🏗️ Proje Yapısı

1. **Veri Toplama**: 
   - Kullanıcıdan el işaretleri toplanır ve `data/` klasörüne kaydedilir.
   - `cv2` ile gerçek zamanlı görüntü işleme yapılır.

2. **Veri Ön İşleme**: 
   - Toplanan görseller, MediaPipe kullanılarak işlenir.
   - El noktaları çıkarılarak `data.pickle` dosyasında saklanır.

3. **Makine Öğrenmesi Modeli**: 
   - `RandomForestClassifier` kullanılarak bir model eğitilir.
   - Model, el işaretlerini sınıflandırır ve `model.p` dosyasında saklanır.

4. **Gerçek Zamanlı Tahmin**: 
   - Eğitilmiş model ile kamera görüntüsünden el işaretleri tespit edilir.
   - Sınıflandırılan işaret, ekranda gösterilir.

## ▶️ Çalıştırma

1. **Veri Toplama:**
```bash
python collect_data.py
```
2. **Model Eğitme:**
```bash
python train_model.py
```
3. **Gerçek Zamanlı Tahmin:**
```bash
python predict.py
```

## 🎮 Nasıl Kullanılır?
1. 📷 Kameranızı açın ve ellerinizi ekrana gösterin.
2. 🔍 Algoritma el işaretlerini tanıyacak ve çıktıyı ekranda gösterecektir.
3. 📊 Model, işaretlerin doğruluğunu analiz ederek sınıflandırma yapacaktır.

⭐ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın!

