# Deteksi Gerobak Pedagang Kaki Lima
## Overview
Proyek ini bertujuan untuk mengembangkan sistem deteksi objek secara real-time yang dirancang khusus untuk mengidentifikasi pedagang kaki lima di Indonesia, termasuk gerobak dan tenda yang biasa ditemukan di pinggir jalan. Pedagang kaki lima merupakan bagian penting dari budaya dan perekonomian lokal, namun keberadaan mereka sering menimbulkan tantangan terkait pengelolaan kota, kemacetan lalu lintas, dan perencanaan ruang publik. Dengan memanfaatkan teknologi visi komputer terkini, sistem ini diharapkan mampu memberikan solusi yang efektif untuk memantau dan menganalisis aktivitas pedagang kaki lima.

## Dataset
Dataset didapatkan dari gabungan dataset [Foodcart](https://universe.roboflow.com/barry-aprtz/foodcart-dnty6) dan [Street Vendor](https://universe.roboflow.com/barry-aprtz/street-vendors-6xixf-cll2s/dataset/1) yang memiliki gambar gerobak atau dan tenda yang bervariasi. Setiap gambar pada dataset telah melalui proses augmentasi dengan diputar sebesar 15 derajat. Persebaran data yang digunakan adalah sebagai berikut:  
| Folder  | Image Count | 
| ------------- | ------------- |
| Train  | 2744 | 
| Validation | 420 | 
| Test | 223 |

## Model 
Proyek ini menggunakan model YOLOv11 sebagai algoritma deteksi objek utama, yang telah diimplementasikan dengan melakukan hyperparameter tuning untuk mengoptimalkan performa deteksi.

### Environment
- Quadro RTX 5000
- Python 3.12.1
- Pytorch 2.5.1
- Torchvision 0.20.1
- Torchaudio 2.5.1
- Ultralytics 8.3.39

### Hyper-parameter Tuning
Hyper-parameter tuning dilakukan dengan menggunakan fungsi model.tune yang disediakan pada library ultralytics untuk mencari learning rate yang terbaik. Tuning dilakukan sebanyak 25 iterasi dengan masing-masing iterasi dijalankan selama 100 epoch.

### Metrik Evaluasi
![image](https://github.com/user-attachments/assets/ef53ad62-411f-4897-ac25-de561737a5d9)

| Model | epoch  | Imgsz | lr0  | lrf | Recall  | Precision | mAP50  | mAP50-95 |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| Baseline | 150  | 1280  | 0.01  | 0.01 | 0.89756  | 0.86928  | 0.917 | 0.61526  |
| Hypertuned | 100  | 1280  | 0.0099  | 0.01016 | 0.90661  | 0.9103  | 0.93075 | 0.6401  |

### Hasil
![image](https://github.com/user-attachments/assets/d76d7601-a364-491a-9dcc-bcaee92a6ca0)
![image](https://github.com/user-attachments/assets/a96f2026-b1e9-4b14-8cb6-1f29be5cfac0)






