# +Proje Yapılma Aşamaları
 ## ++Django ve React'i entegre etme adımları
 NodeJS ve npm kurulu olduğundan emin olun.Kurulu olup olmadığını aşağıdaki aşağıdaki adımlarla test edebilirsiniz.
 ***node --version***
 ***npm --version***
 Yukarıdaki komutların sürümlerini döndürürse kurulum başarılı olmuştur.
 ### +++Sanal bir ortam başlatmak
 ***pyenv virtualenv system venv***

Yukarıdaki komut, proje dizininde sanal bir ortam oluşturur.

***pyenv activate venv***

Yukarıdaki komut sanal ortamı etkinleştirir.

 ### +++Django'yu Kurmak
 Şimdi Django'yu kuralım
 python -m pip install django
 Yukarıdaki komutu kullanmak, kurulumun kök python için değil sanal ortam için yapılmasını sağlar.

### +++Django Projesi Oluşturma
***django-admin startproject <project_name>***

Az önce kullanarak oluşturduğunuz projeye dizini değiştirin

***cd <project_name>***

Şimdi şunu kullanarak bir Django uygulaması başlatın:

***django-admin startapp frontend***

### +++Uygulamayı ayarlar dosyasına ekleme

<project_name>/settings.py

Az önce oluşturduğunuz uygulamaya gidin ve yüklü uygulamalar listesine ekleyin.
### +++Gösterilecek frontend için bir url oluşturma.

Eklemede, <project_name>/urls.py yeni bir url ekleyin.

Şimdi frontend/ gidin ve urls.py adlı yeni bir dosya oluşturun.

frontend/urls.py Oluşturduğunuz url'ye gidin ve bir görünüm ekleyin.

### +++Frontend için Şablonlar, Statik dosyalar ve React için klasör yapısının oluşturulması

<project_name>/frontend içine templates adlı bir klasör oluştur.

Şimdi frontend adında başka bir klasör oluşturun ve içinde index.html oluşturun.

Dosyanız frontend/templates/frontend/index.html böyle olmalı.

<project_name>/frontend içine static adlı bir klasör oluştur

Şimdi içinde frontend ,css, images adlı üç klasör oluşturun.

Şimdi tamamen React ve Webpack'in kullanılabilmesi için başka bir klasör yapısı oluşturacağız.

<project_name>/frontend altına src adlı başka bir klasör ekle ve içinde index.js oluştur

Şimdi frontend/src içinde  bir components klasörünü ekleyin ve .App.js adlı bir dosya ekleyin 

Artık dizininizde aşağıdaki dosya yollarına sahip olmalısınız.

frontend/src/index.js ve frontend/src/components/App.js

 ### +++Webpack başlatma ve gerekli bağımlılıkları yükleme
 <project_name>/frontend dizinine gidin ve gerekli bağımlılıkları yüklemek için bu komutları izleyin.
 
 İlk olarak, aşağıdaki komutla npm başlat
***npm init -y***

sonra, webpack kurun
***npm install webpack webpack-cli --dev***

şimdi babel ve diğer gerekli babel bağımlılıklarını kurun
***npm install @babel/core @babel/preset-react @babel/preset-env --dev***

şimdi gerekli Webpack yükleyicilerini kurun
***npm install babel-loader css-loader style-loader --dev***

react ve react-dom yükleyin
***npm install react react-dom --dev***

kalan birkaç paketi daha indirin
***npm install react-router-dom @babel/plugin-proposal-class-properties***

### +++Webpack ve Babel'i Yapılandırma

<project_name>/frontend webpack.config.js dosya oluşturun

<project_name>/frontend babel.config.json dosya oluşturun

Dizini projenin olduğu konuma getirin (manage.py nin olduğu konuma) ve terminalinizde aşağıdaki komutları çalıştırın.
python manage.py migrate

Ve daha sonra

***python manage.py runserver***

Farklı bir terminalde <project_name>/frontend dizinine gidin ve Webpack'in siz çalışırken paketleri dinlemesi ve oluşturması için aşağıdaki komutu çalıştırın.
 ***npm run dev***


# +Proje çalıştırma aşamaları
## ++Projeyi indir
*projeyi indirin ve terminalde kök dizini projedeki requirements.txt'nin olduğu dizine getirin*
## ++Paketleri yükle
 
***pip install -r requirements.txt***
 
Yukardaki kodu çalıştırın daha sonra Python'un en güncel versiyonunu indiriniz...
 
## ++Projeyi Çalıştırma

***python.exe .\manage.py runserver***

Yukardaki kod ile django projemizi çalıştırıyoruz.
