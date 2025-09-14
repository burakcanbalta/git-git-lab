## Git Kurulumu ve İlk Ayarlar
Ben git indirip bu işlemleri git bash üzerinden yapacağım.

### Versiyon kontrol

Git'in yüklü olup olmadığını kontrol etmek için:

``` bash
git --version
```

<img width="469" height="54" alt="version" src="https://github.com/user-attachments/assets/baebf250-9cb4-46be-aec5-a89695b545f4" />

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
Öncelikle bir klasör oluşturun ve içerisine gidin:

``` bash
mkdir proje-adi
cd proje-adi
```

Bu klasörü Git projesi haline getirmek için:

``` bash
git init
```

<img width="640" height="180" alt="user+check" src="https://github.com/user-attachments/assets/a9bfef45-412a-4cab-af14-89b42dc06629" />

<img width="597" height="137" alt="email+check" src="https://github.com/user-attachments/assets/8505f2d0-fc52-44a9-9970-b8bb566240ca" />

<img width="599" height="197" alt="mkdirproje+gitinit" src="https://github.com/user-attachments/assets/7d9dcc60-a171-466c-a8fc-69d5b6acc5ec" />

## Dosya ve Commit İşlemleri

### Dosya ekleme

<img width="695" height="228" alt="gitdrawio" src="https://github.com/user-attachments/assets/40d4b2bd-437e-43bb-9239-30b1be270476" />


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
<img width="718" height="508" alt="iş2" src="https://github.com/user-attachments/assets/4e6f9cad-def7-4ce4-ad7a-c49de5630a33" />

<img width="764" height="474" alt="iş1" src="https://github.com/user-attachments/assets/18d77764-7df7-4e92-be08-63cdd91ece46" />

### Durum kontrolü

Projede yapılan değişiklikleri görmek için:

``` bash
git status
```
<img width="489" height="69" alt="gitstatus" src="https://github.com/user-attachments/assets/d7c74e6a-b425-497a-9529-669fc5c96a0e" />


### Değişiklikleri inceleme

Dosya bazlı değişiklikleri görmek için:

``` bash
git diff
```

Staging alanındaki farklılıkları görmek için:

``` bash
git diff --staged
```
<img width="654" height="520" alt="diff2" src="https://github.com/user-attachments/assets/bc3a3530-7337-43db-8f46-d72904e63ae3" />

<img width="729" height="505" alt="diff1" src="https://github.com/user-attachments/assets/9147ee21-3074-4b93-a135-eca9fd0d4c69" />

------------------------------------------------------------------------

## Dosya Yönetimi

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

## Geri Alma İşlemleri

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

## Branch (Dal) Yönetimi

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
