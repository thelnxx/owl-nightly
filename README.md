# ‼️ Dikkat
- Aşağıda yer alan dökümantasyon sadece projeyi betimlemek içindir proje kademeli olarak geliştirilmekte ve sürümleri yayımlanacaktır bilginize ...
- Yerel ortamda projenin çalışabilmesi için kullanılan program ve framework'lerin en az şu sürümlerde kullandığınızdan emin olun:
  - **Python**: v3.14.7
  - **Django**: v6.1
  - **Bootstrap**: v5.3
# 🚀 Owl Nightly

> Öğrenciler için yardımcı baykuş.

<!-- BADGES -->
[![Python](https://img.shields.io/badge/Python-3.14.7-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Django](https://img.shields.io/badge/Django-6.1-092E20?style=for-the-badge&logo=django&logoColor=white)](https://djangoproject.com)
![SQLite](https://img.shields.io/badge/SQLite-Sqlite3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)

## 📌 Proje Hakkında

Bu proje, Django web framework kullanılarak geliştirilmiş modern bir web uygulamasıdır. Amacı öğrenciler için dinamik olarak geliştirilmiş bir eğitim-öğretim ortamıdır. 

### 📸 Ekran Görüntüleri
| Ana Sayfa | Yönetim Paneli |
| :---: | :---: |
| ![Home Page](https://via.placeholder.com/400x220?text=Henüz+bir+görsel+eklenmedi) | ![Admin Panel](https://via.placeholder.com/400x220?text=Henüz+bir+görsel+eklenmedi) |

---

## ✨ Özellikler

- ⚡ **RESTful API:** Django REST Framework ile entegre API uç noktaları.
- 🎨 **Arayüz:** Bootstrap v5.3 CSS ile hoş arayüzler.
- 🗄️ **Veritabanı Optimization:** SQLite3 ile indeksleme ve ORM sorgu optimizasyonları.
---

## 🛠️ Kullanılan Teknolojiler

- **Backend:** Python 3.14.7, Django 5.3, Django REST Framework
- **Frontend:** HTML5, Bootstrap, JavaScript
- **Veritabanı:** SQLite3
- **DevOps & Araçlar:** Docker, Docker Compose, Git, VSCode

---

## ⚙️ Kurulum & Çalıştırma

### 1. Yerel Kurulum (Local Setup)

Projeyi kendi bilgisayarınızda çalıştırmak için aşağıdaki adımları sırasıyla uygulayın:

#### Ön Koşullar
* Python 3.14+
* Git
* SQLite

#### Adım 1: Depoyu klonlayın
```bash
git clone [https://github.com/thelnxx/owl-nightly.git](https://github.com/thelnxx/owl-nightly.git)
cd owl-nightly
```

#### Adım 2: Sanal ortamı (virtual environment) oluşturun ve aktif edin
```bash
# Linux / macOS
python3 -m venv venv
source venv/bin/activate

# Windows (Command Prompt / PowerShell)
python -m venv venv
venv\Scripts\activate
```

#### Adım 3: Bağımlılıkları yükleyin
```bash
pip install -r requirements.txt
```

#### Adım 4: Ortam değişkenlerini hazırlayın
```bash
cp .env.example .env
```
*(Dosya içeriğindeki `SECRET_KEY` ve Veritabanı bilgilerinizi kendinize göre güncelleyin).*

#### Adım 5: Veritabanı migrasyonlarını yapın
```bash
python manage.py migrate
```

#### Adım 6: Süper kullanıcı (Admin) oluşturun
```bash
python manage.py createsuperuser
```

#### Adım 7: Geliştirme sunucusunu başlatın
```bash
python manage.py runserver
```
Uygulamaya tarayıcınızdan `http://127.0.0.1:8000/` adresinden erişebilirsiniz.

---

### 2. Docker ile Kurulum (Opsiyonel)

Eğer sisteminizde Docker ve Docker Compose kuruluysa, tüm servisleri tek bir komutla ayağa kaldırabilirsiniz:

```bash
docker-compose up --build -d
```
Sistem ayağa kalktıktan sonra migrasyonları çalıştırmak için:
```bash
docker-compose exec web python manage.py migrate
```

## 🧪 Testleri Çalıştırma

Projedeki birim testlerini (unit tests) çalıştırmak için:

```bash
py manage.py test
```

Veya `pytest` kullanıyorsanız:
```bash
pytest
```
---
## 🪲 Projeyi Debug Modunda Çalıştırma
Projenin üstünde eklemeler/çıkarmalar, yenilemeler, düzeltmeler vb. şeyleri görmek için;

projenizin `settings.py` dosyası içerisinde yer alan `DEBUG=FALSE` bölümünü aşağıdaki kod bloğu ile değiştiriniz. Böylece proje üstünde yapılan değişiklikleri anlık görebilir ve gelişimini takip edebilirsiniz:
```python
DEBUG=TRUE
```
ardından bu komutu çalıştırabilirsiniz:
```bash
py manage.py runserver
```

---

## 📄 Lisans

Bu proje [MIT Lisansı](LICENSE) ile lisanslanmıştır.
