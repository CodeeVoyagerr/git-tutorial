
# 🌟 Git Eğitimi

<br>

## 🚀 Git Nedir?

**Git**, yazılım geliştirme sürecinde kod versiyonlarını takip etmek için kullanılan **dağıtık bir versiyon kontrol sistemidir**. 

Kod üzerinde yapılan değişiklikleri kaydederek, farklı zamanlardaki durumlardan geri dönebilir veya belirli versiyonlar arasında karşılaştırma yapabilirsiniz. 

Git, özellikle birden fazla geliştiricinin aynı proje üzerinde çalışmasını kolaylaştırır ve çatışmaları önler.

<br>

---

## 📚 Git'in Temel Kavramları
- **📁 Repository (Depo):** Projenizin dosyalarını ve bu dosyalarda yapılan tüm değişikliklerin geçmişini içeren bir veri tabanı.
- **💾 Commit:** Bir dizi değişikliğin kaydedildiği anlık görüntü. Her commit, proje üzerindeki belirli bir durumu temsil eder.
- **🌿 Branch (Dal):** Projede paralel olarak çalışmanızı sağlayan ayrılmış kod kopyası. Ana dal (`main` veya `master`), genellikle projenin en güncel ve kararlı versiyonunu temsil eder.
- **🔀 Merge:** Farklı dallardaki değişiklikleri birleştirme işlemi.
- **📥 Clone:** Uzak bir repository'nin yerel bir kopyasını oluşturma işlemi.
- **⬇️ Pull:** Uzak repository'deki değişiklikleri yerel repository'ye getirme işlemi.
- **⬆️ Push:** Yerel repository'deki değişiklikleri uzak repository'ye gönderme işlemi.

---

<br>
<br>

## 🛠️ Git Komutları ve Kullanımları

### 1. 🖥️ Git Kurulumu
Git'i kurmak için:

- **Windows:** [Git for Windows](https://git-scm.com/download/win)
- **Mac:** Terminal üzerinden `brew install git` komutunu kullanabilirsiniz.
- **Linux:** Çoğu dağıtımda `sudo apt-get install git` veya `sudo yum install git` komutlarıyla kurulabilir.

Kurulumdan sonra Git yapılandırması yapmak için:

```
git config --global user.name "Kullanıcı Adı"
git config --global user.email "email@example.com"
```

### 2. 📂 Yeni Bir Git Deposu Oluşturmak

#### Yerel bir repository oluşturmak için:

```
git init
```

Bu komut, bulunduğunuz dizinde gizli bir .git klasörü oluşturur ve bu klasör, Git'in değişiklikleri izlemesini sağlar.

### 3. 🌐 Var Olan Bir Depoyu Klonlama

#### Uzak bir repository’yi klonlamak için:

```
git clone <repository-url>
```

Bu komut, belirtilen URL'deki repository'nin yerel bir kopyasını oluşturur.

### 4. 📝 Değişiklikleri İzleme

#### Çalışma dizinindeki tüm dosyaların durumunu görmek için:

```
git status
```

Bu komut, değişiklik yapılmış, eklenmiş veya izlenmemiş dosyaları gösterir.

#### Dosyaları ekleme (stage) alanına eklemek için:

```
git add <dosya-adı>
```

#### Tüm değişiklikleri eklemek için:

```
git add .
```

#### İki commit, iki branch veya çalışma alanınızdaki değişiklikleri karşılaştırmak için:

```
git diff                      # Çalışma alanı ile index arasındaki farkları gösterir
git diff <branch1> <branch2>  # İki branch arasındaki farkları gösterir
git diff <commit1> <commit2>  # İki commit arasındaki farkları gösterir
```


### 5. 💾 Değişiklikleri Kaydetme (Commit)

#### Commit yapmak için:

```
git commit -m "Yapılan değişiklikleri açıklayan bir mesaj"
```

Bu komut, ekleme (stage) alanındaki tüm değişiklikleri kaydeder.

#### Commit’i düzenlemek (ammend): 

```
git commit --amend -m "Yeni mesaj"
```

#### Commit'leri parçalamak (sparse): 

```
git commit -p
```


### 6. 🌿 Branch (Dal) Yönetimi

#### Yeni bir dal oluşturmak için:

```
git branch <dal-adı>
```

#### Branch’ler arasında geçiş yapmak için:

```
git checkout <dal-adı>
```

#### Yeni bir branch oluşturup bu branch’e geçmek için:

```
git checkout -b <dal-adı>
```


### 7. 🔄 Değişiklikleri Birleştirme (Merge)

#### Branch’leri birleştirmek için, önce ana branch’e geçin (genellikle main veya master):

```
git checkout main
```

#### Farklı bir dalı mevcut dala birleştirmek için:

```
git merge <dal-adı>
```

Bu komut, belirtilen dalda yapılan değişiklikleri mevcut dala birleştirir.

### 8. ⬆️ Değişiklikleri Uzak Depoya Gönderme (Push)

#### Değişiklikleri uzak bir repository'ye göndermek için:

```
git push                      # Yerel branch’i uzak repository’ye gönderir
git push origin <branch-adı>  # Belirli bir branch’i uzak repository’ye gönderir
```

Bu komut, yerel dalınızı uzak depoya gönderir.

### 9. ⬇️ Uzak Depodan Değişiklikleri Getirme (Pull)

#### Uzak depodaki değişiklikleri almak ve yerel dalınıza birleştirmek için:

`git pull` ,  `git fetch ve git merge` komutlarının birleşimidir. Uzak repository’den güncellemeleri alır ve mevcut branch’inize uygular.

```
git pull                   # Uzak repository'den güncellemeleri çeker ve birleştirir
git pull <remote> <branch> # Belirli bir branch'ten güncellemeleri çeker ve birleştirir
```

### 10. 🔍 Geçmişi İnceleme

#### Commit geçmişini görmek için:

```
git log                        # Standart commit geçmişi
git log --oneline              # Kısa commit geçmişi
git log --graph --oneline      # Grafikli commit geçmişi
git log --author="Author Name" # Belirli bir yazarın commit'lerini gösterir
```

### 11. 🔙 Değişiklikleri Geri Alma

#### Dosyadaki değişiklikleri geri almak için:

```
git checkout -- <dosya-adı>
```

#### Stage alanından bir dosyayı çıkarmak için:

```
git reset HEAD <dosya-adı>
```

#### Belirli bir commit’in değişikliklerini geri almak için:

```
git revert <commit-id>
```

#### Commit’leri geri almak veya değişiklikleri iptal etmek için:

```
git reset --hard <commit-id>
```

### 12. 🏷️ Etiketleme

#### Belirli bir commit’e etiket eklemek için:

Commit’lere etiket ekler. Genellikle sürüm numaraları için kullanılır.

```
git tag <tagname>           # Yeni bir etiket oluşturur
git tag -d <tagname>        # Bir etiketi siler
git tag -a <tagname> -m "Message" # Annotated tag oluşturur
git push origin <tagname>  # Etiketi uzak repository'ye gönderir
```

### 13. 🧩 Rebase

#### Bir branch’i başka bir branch’in üzerine “taşımak” için:

```
git rebase <branch-adı>   # Mevcut branch’i belirtilen branch’e yeniden tabanlar
git rebase -i <commit>    # Interaktif rebase yapar, commit geçmişini düzenlemenizi sağlar
```


## ⚙️ Gelişmiş Git Komutları

### 14. 🗂️ Git Stash

#### Değişiklikleri geçici olarak kaydetmek için:

```
git stash            # Değişiklikleri saklar
git stash pop        # Saklanan değişiklikleri geri getirir
git stash list       # Saklanan stash'leri listeler
git stash apply      # Belirli bir stash'i uygular
```

### 15. 🕵️‍♂️ Git Bisect

#### Hangi commit’in hataya neden olduğunu bulmak için:

```
git bisect start
git bisect bad
git bisect good <commit-id>
```

### 16. 🍒 Git Cherry-Pick

#### Belirli bir commit’i başka bir dala eklemek için:

```
git cherry-pick <commit-id>
```

### 17. 🗒️ Git Reflog

#### Git geçmişindeki tüm hareketleri görmek için:

```
git reflog
```

### 18. 🧹 Git Clean

#### Çalışma alanındaki izlenmeyen dosyaları temizlemek için:

```
git clean -n              # Temizlenecek dosyaları listeler
git clean -f              # İzlennmeyen dosyaları siler
git clean -fd             # İzlennmeyen dosyaları ve dizinleri siler
```

### 19. 🔗 Git Remote

#### Uzak repository'ler ile ilgili işlemler yapar. Uzak repository'leri listeleyebilir, ekleyebilir veya kaldırabilirsiniz.

```
git remote -v                       # Uzak repository'leri listeler
git remote add <name> <url>         # Yeni bir uzak repository ekler
git remote remove <name>            # Uzak repository'yi kaldırır
git remote set-url <name> <new-url> # Uzak repository URL'ini değiştirir
```

<br>
<br>


## 💡 Git İpuçları ve Best Practices

### Küçük ve Anlamlı Commit’ler Yapın

#### Sık ve Küçük Commit'ler: 
Büyük değişiklikleri küçük parçalara bölerek commit yapmak, sorunları tespit etmeyi ve geri almayı kolaylaştırır.
#### Bir İşlem İçin Bir Commit: 
Her commit, belirli bir işlevsel değişiklik veya düzeltmeyi temsil etmelidir. Örneğin, bir commit yalnızca bir özelliği eklemeli ya da bir hatayı düzeltmelidir.

### Açıklayıcı Commit Mesajları Kullanın

#### Başlık ve Açıklama: 
Commit mesajları genellikle iki kısımdan oluşur: başlık ve açıklama. Başlık kısa ve öz olmalı, açıklama ise detaylı bilgi içermelidir.

### Düzenli Olarak Pull Yapın

#### Senkronize Olun: 
Uzak depodaki güncellemeleri düzenli olarak çekmek, çakışmaları önlemeye yardımcı olur ve projenin güncel kalmasını sağlar.

#### Pull Before Push: 
Her zaman push işleminden önce pull yaparak, yerel ve uzak depolar arasındaki farklılıkları kontrol edin.

### Branch'leri Akıllıca Kullanma

#### Feature Branches: 
Her yeni özellik veya düzeltme için ayrı branch'ler kullanın. Bu, ana branch’i (genellikle main veya master) karışıklıklardan korur.

#### Branch İsimlendirme: 
Branch isimlendirmede anlaşılır ve standart isimler kullanın.

###  Etiket (Tag) Kullanımı

#### Sürüm Etiketleri: 
Projenizin önemli sürümlerini etiketleyin (örneğin, v1.0.0, v2.1.0). Bu, sürüm geçişlerini ve değişikliklerini takip etmeyi kolaylaştırır.

#### Tag'leri Kullanma: 
Etiketler, belirli commit’leri işaretlemek için kullanılır. Örneğin, bir sürüm çıktığında veya önemli bir özellik eklendiğinde etiket oluşturun.

### Gitignore Dosyası Kullanımı

#### Yüklenmeyecek Dosyalar: 
Projeye dahil edilmemesi gereken dosya ve klasörleri `.gitignore` dosyasında tanımlayın. Örneğin, geçici dosyalar, derleme çıktıları vb.

Örnek :

```
*.log
node_modules/
.env
```

### Ekstra Tavsiyeler:

#### Sürekli Entegrasyon (CI) ve Sürekli Dağıtım (CD): 
Git ile entegrasyon sağlayarak kodunuzun sürekli olarak test edilmesini ve dağıtılmasını sağlayın.

#### Pull Request (PR) Kullanımı: 
Özellikle ekip projelerinde, kod incelemesi ve tartışma için pull request’ler oluşturun.


<br>
<br>


## 🌐 GitHub ve GitLab

GitHub ve GitLab, Git tabanlı projeleri barındırmak ve yönetmek için kullanılan popüler platformlardır. 

Her ikisi de çeşitli işbirliği araçları sunarak yazılım geliştirme süreçlerini daha verimli hale getirir.


### GitHub Nedir?

GitHub, Git tabanlı projeleri barındırmak, sürüm kontrolü yapmak ve ekiplerle işbirliği yapmak için kullanılan bir web tabanlı platformdur. 

GitHub, özellikle açık kaynak projelerinin barındırılması ve yönetilmesi için geniş bir kullanıcı kitlesine sahiptir.


### GitLab Nedir?

GitLab, Git tabanlı proje yönetimi ve DevOps platformudur. 

GitLab, kod barındırmanın yanı sıra, sürekli entegrasyon, sürekli dağıtım ve proje yönetimi için kapsamlı araçlar sunar.

<br>
<br>
