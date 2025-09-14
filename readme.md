# Git Temel Kullanım Rehberi

Bu doküman, yazılım geliştirme sürecinde **Git** versiyon kontrol
sistemini kullanmaya yeni başlayanlar için hazırlanmıştır. Git sayesinde
yapılan değişiklikleri takip edebilir, projeyi ekip arkadaşlarınızla
birlikte yönetebilir ve gerektiğinde geçmiş versiyonlara geri
dönebilirsiniz.

------------------------------------------------------------------------

## 1. Git Kurulumu ve İlk Ayarlar

### Versiyon kontrol

Git'in yüklü olup olmadığını kontrol etmek için:

``` bash
git --version
```

### Kullanıcı adı ve e-posta tanımlama

Git üzerinde yapacağınız tüm commit'lerin kime ait olduğunu belirlemek
için kullanıcı bilgilerinizi ayarlamanız gerekir:

``` bash
git config --global user.name "Adınız Soyadınız"
git config --global user.email "mail@adresiniz.com"
```

Tanımlamaları kontrol etmek için:

``` bash
git config --global user.name
git config --global user.email
```

------------------------------------------------------------------------

## 2. Yeni Proje Oluşturma

Öncelikle bir klasör oluşturun ve içerisine gidin:

``` bash
mkdir proje-adi
cd proje-adi
```

Bu klasörü Git projesi haline getirmek için:

``` bash
git init
```

------------------------------------------------------------------------

## 3. Dosya ve Commit İşlemleri

### Dosya ekleme

Çalışma dizinindeki tüm dosyaları **staging area** (geçiş alanı) içine
eklemek için:

``` bash
git add .
```

### Commit oluşturma

Değişiklikleri kalıcı hale getirmek için commit mesajı eklenir:

``` bash
git commit -m "İlk commit"
```

### Durum kontrolü

Projede yapılan değişiklikleri görmek için:

``` bash
git status
```

### Değişiklikleri inceleme

Dosya bazlı değişiklikleri görmek için:

``` bash
git diff
```

Staging alanındaki farklılıkları görmek için:

``` bash
git diff --staged
```

------------------------------------------------------------------------

## 4. Dosya Yönetimi

### Dosya silme

``` bash
git rm dosya.txt
```

Klasör silmek için:

``` bash
git rm -r klasor/
```

### Dosya taşıma veya ad değiştirme

``` bash
git mv eski.txt yeni.txt
```

------------------------------------------------------------------------

## 5. Geri Alma İşlemleri

### Çalışma dizinindeki değişiklikleri geri almak

``` bash
git checkout -- dosya.txt
```

### Staging alanından çıkarmak

``` bash
git reset HEAD dosya.txt
```

### Versiyon değiştirme

Belirli bir commit'e geçmek için:

``` bash
git checkout <commit_hash> -- .
```

Commit'lerin listesini görmek için:

``` bash
git log
```

------------------------------------------------------------------------

## 6. Branch (Dal) Yönetimi

### Mevcut dalları listeleme

``` bash
git branch
```

Uzak depodaki tüm dalları listeleme:

``` bash
git branch --all
```

### Yeni dal oluşturma

``` bash
git branch yeni-dal
```

### Dallar arasında geçiş yapma

``` bash
git checkout yeni-dal
```

### Dalları birleştirme

``` bash
git merge yeni-dal
```

------------------------------------------------------------------------

## 7. Uzak Depo ile Çalışma

### Uzak repo ekleme ve push

``` bash
git remote add origin <repo-url>
git push -u origin master
```

### Uzak repodan güncelleme çekme

``` bash
git pull
```

------------------------------------------------------------------------

## 8. GitHub Üzerinde İş Birliği

GitHub üzerinden ekip çalışması için **Issues** bölümünü
kullanabilirsiniz.\
Bir sorun ya da geliştirme talebi oluşturmak için:

-   `Issues` → `New Issue`\
    Başlık ve açıklama ekleyip ekip arkadaşlarınızla paylaşabilirsiniz.

------------------------------------------------------------------------

## 9. SSH Anahtar Oluşturma

GitHub ile daha güvenli bağlantı kurmak için SSH anahtarı
oluşturabilirsiniz:

``` bash
ssh-keygen
```

Oluşturulan anahtar, `~/.ssh/id_rsa.pub` dosyasında bulunur. İçeriğini
GitHub hesabınıza ekleyerek SSH üzerinden bağlantı kurabilirsiniz.

------------------------------------------------------------------------

## Özet

Bu doküman ile:\
- Git kurulumu ve kullanıcı tanımlaması\
- Proje oluşturma\
- Dosya ekleme, commit, log ve diff işlemleri\
- Branch ve merge işlemleri\
- Uzak repo yönetimi\
- GitHub üzerinde Issues ile iş birliği\
temel seviyede öğrenilmiş olur.
