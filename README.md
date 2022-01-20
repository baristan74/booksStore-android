# BOOKS STORE
## Proje aşamaları:
######	1. Projenin oluşturulması
######	2. Firabase uygulamaya entegre edilmesi
######	3. Giriş ve kayıt ol ekranlarının yaratılması
######	4. Sisteme kitap eklenebilmesi için admin paneli oluşturulması
######	5. Admin paneli üzerinden kitapların veritabanına eklenmesi
######	6. Anasayfa oluşturulması
######	7. Anasayfada veritabanındaki kitapların listelenmesi
######	8. Arama optimizasyonunun oluşturululması
######	9. Sepet ekranının oluşturulması
######	10. Kullanıcı için sepete ekleme işlemlerinin gerçekleştirilmesi
######	11. Kullanıcı için sepetten kaldırma işlemlerinin gerçekleştirilmesi
######	12. Satın alma işleminin gerçekleştirilmesi
######	13. Kullanıcı profil ekranının oluşturulması
######	14. Kullanıcı bilgileri düzenleme operasyonlarının gerçekleştirilmesi


## Uygulamanın İşleyişi
### Giriş ve Kayıt Ol

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150346576-6dba4e17-e5de-4e25-a860-c19d64a53b04.png">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150346713-2a44b03d-982c-4a3f-8879-bc5a16e53dc2.png">
</p>

-	Giriş ve Kayıt ol ekranları Fragment olarak oluşturuldu
-	Eğer kullanıcı kayıtlı değil ise kayıt ol ekranı üzerinden kayıt gerçekleştirebilir.
-	Eğer giriş işleminde veya kayıt ol ekranlarında boş alanları doldurmamış veya hatalı doldurmuş ise Toast mesajları ile kullanıcı uyarılır.

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150346971-32e1c155-2a64-4aa6-9253-47997dbdaa65.png">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347038-7e398b08-c9ce-48f1-9754-19f27bf4a751.png">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347128-0dd0f577-c537-43ff-8cba-64f13d476758.png">
</p> 
     
-	Kayıt işlemi eğer başarılı bir şekilde gerçekleştiyse anasayfaya geçiş yapar.

<p align="center">
<img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347174-3b47a10e-2fdc-44d7-9832-940ece3ab7df.png">
</p>
 
-	Veritabanındaki veriler adaptör yardımı ile anasayfaya bastırıldı.

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347214-80443348-6a16-45df-a5a8-558f685aca38.png">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347258-d5d69713-60bf-4883-a0b3-2a57820ca73e.png">
</p> 
     
-	Kullanıcı aramak istediği kitabın ismini yada yazar adını girerek istediği kitaba ulaşabilir
-	EditText’e girilen veri okunur ve okunan veri adaptör üzerinden veritabanındaki verileri filtreleyerek ekrana getirir.
-	Kullanıcı satın almak istediği kitabı sepete ekle butonu yardımı ile kendi sepetine ekleme yapar.

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347337-b49daf4c-07eb-41db-8d96-b89524cdaf7b.png">
</p> 
  
-	Sepete ekleme işlemi gerçeşleştiğinde Toast mesajı ile belirtilir.
-	Kullanıcının kendine ait sepetinin veritabanındaki görüntüsü aşağıda gösterildiği gibidir.

<p align="center">
  <img width="500" height="400" src="https://user-images.githubusercontent.com/61651202/150347383-4c65b98f-eee4-4729-8cf7-25d2c6e78e8f.png">
</p> 

### Sepet

-	Kullanıcı sepetine gittiğinde eklemiş olduğu kitaplar adapter yardımı ile ekranda görüntülenir.
-	Kullanıcı sepetinden kitap kaldırmak istediğinde sepetten kaldır butonu ile bu işlemi gerçektirir. İşlem gerçekleştiğinde Toast mesajı ile kullanıcı bilgilendirilir.

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347454-d57d4536-4361-4458-a9ff-fb44b05df8e1.png">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347487-bc97936b-a09c-4b46-94b7-5533b93bad9b.png">
</p> 
    
-	Yukarıda sepetten kaldırılan kitap Yuval Noah Harari’nin Sapiens kitabıdır.

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347541-9cd93e85-1e95-468c-829b-696642a8dfdd.png">
</p> 

-	Eğer kullanıcı sepetindeki kitapları satın almak isterse satın al butonu  satın alma işlemini gerçekleştirir. İşlem gerçekleştiğinde Sepet boşaltılır ve Toast mesajı ile Kullanıcı bilgilendirilir.

-	Satın alma işlemi gerçekleştikten sonra veritabanında kullanıcı içerisindeki sepet alanı temizlenir. 


### Kullanıcı Profili

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347628-fff65780-68b8-4275-aad6-a20f1910d823.png">
</p> 
 
-	Kullanıcı kendi bilgilerini profil kısmından görüntüleyebilmektedir.
-	Eğer kullanıcı bilgilerini güncellemek isterse kalem butonu üzerinden profil güncelleme sayfasına geçiş yapabilir.
-	Eğer çıkış yapmak isterse çıkış butonu üzerinden çıkış yapabilir.

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347687-118fb9b7-7fd6-4df1-b223-93245052a745.png">
</p> 
 
-	Kullanıcı eğer profil resmini değiştirmek isterse resmin üzerinde bulunan kalem butonu üzerinden telefonun galerisine bağlanarak profil resmini güncelleyebilir.
      
<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347786-4e770fae-d58f-4342-a688-a54e8ad5f8ea.png">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347838-849006a6-c7c4-404e-b8db-6374348245ac.png">
</p>

-	Resim güncellendiğinde Firebase Storage alanına ilgili resim depolanır.
      
<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347906-ac12f4bc-c562-479d-8b55-a7b7a4d109d4.png">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150347936-7aa4d903-06c9-4861-9bfe-06ae3d4d74b7.png">
</p>

-	Kullanıcı profil resmi veya bilgilerini değiştirdiğinde kayıt işleminin gerçekleşmesi için tik butonunu kullanır. 
-	Kullanıcı bilgilerini eksik olarak kaydetme işlemi gerçekleştirirse hata mesajı ile uyarılır. Eğer bilgilerini eksiksiz doldurduysa Toast mesajı ile işlemin gerçekleştiğine dair kullanıcı bilgilendirilir.

### Yönetim Paneli
  
<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150348002-e5d90085-4f60-44da-95e2-95152e7ffb87.png">
</p>

-	Giriş ekranında giriş yapan kullanıcının veritabanındaki userType alanına göre ayırt edilir. userType alanı eğer admin ise Admin paneline yönlendirilir.

<p align="center">
  <img width="250" height="400" src="https://user-images.githubusercontent.com/61651202/150348033-666e299e-28c1-4ae7-8672-b8189a127776.png">
</p>
 
-	Yukarıda görülen pencere üzerinden veritabanına kitap ekleme işlemi admin tarafından gerçekleştirilir. Kitap resimleri Firebase Storage bölümüne depolanır. Kitap bilgileri ise Firebase RealTime Database alanına kaydedilir.
 
## FAYDALANMIŞ OLDUĞUM KAYNAKLAR
-	Firabase :  https://firebase.google.com/docs
-	Android :  https://developer.android.com/docs
-	Picasso: https://github.com/square/picasso
-	Glide : https://github.com/bumptech/glide
