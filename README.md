# Deteksi Gerobak Pedagang Kaki Lima
## Dataset
Dataset didapatkan dari gabungan dataset [Foodcart](https://universe.roboflow.com/barry-aprtz/foodcart-dnty6) dan [Street Vendor](https://universe.roboflow.com/barry-aprtz/street-vendors-6xixf-cll2s/dataset/1) yang memiliki gambar gerobak atau dan tenda yang bervariasi yang bervariasi. Persebaran data yang digunakan adalah sebagai berikut
| Train  | 2744 | 
| Validation | 420 | 
| Test | 223 |

## Environment
- Quadro RTX 5000
- Python 3.12.1
- Pytorch 2.5.1
- Torchvision 0.20.1
- Torchaudio 2.5.1
- Ultralytics 8.3.39

## Metrik Evaluasi
![results](https://github.com/user-attachments/assets/18e945e4-eb5d-4332-88e6-10b7ceb072e5)

| epoch  | Imgsz | lr0  | lrf | Recall  | Precision | mAP50  | mAP50-95 |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 150  | 1280  | 0.01  | 0.01 | 0.93347  | 0.8932  | 0.91624  | 0.60068  |

## Hasil
![image](https://github.com/user-attachments/assets/61c00312-5f34-40d8-83f6-51544ed585a6)

https://github.com/user-attachments/assets/3b157895-afb4-46f3-abb6-a15ceef131dc




