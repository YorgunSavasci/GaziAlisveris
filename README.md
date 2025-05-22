# GaziShop E-Ticaret Platformu

## Proje Hakkında

GaziShop, kullanıcıların kolayca **item'ları** listeleyebildiği, sepetlerine ekleyebildiği, sipariş oluşturabildiği ve yönetebildiği tam teşekküllü bir e-ticaret platformudur. . Modern web teknolojileri kullanılarak hem kullanıcı dostu bir arayüz hem de güçlü, ölçeklenebilir bir arka plan mimarisi sunmayı hedeflemektedir.

## Özellikler

* **Kullanıcı Yönetimi:**
    * Kullanıcı kaydı ve girişi
    * Kullanıcı mail görüntüleme ve güncelleme
    
* **Item Yönetimi:**
    * **Item'ları** kategoriye göre listeleme ve arama
    * **Item** detaylarını görüntüleme
    *item** ekleme, güncelleme ve silme (Admin yetkileri ile )
* **Sepet ve Sipariş:**
    * **Item'ları** sepete ekleme, sepetten çıkarma ve miktar güncelleme
    * Sepet içeriğini görüntüleme
    * Sipariş oluşturma 
* **Kategori Yönetimi:**
    * **Item** kategorilerini listeleme
    * Admin paneli üzerinden kategori ekleme, güncelleme ve silme (Admin yetkileri ile)
* **Güvenlik:**
    
    * Parola şifreleme

## Kullanılan Teknolojiler

Bu proje, aşağıdaki temel teknolojiler kullanılarak geliştirilmiştir:

**Backend (Arka Yüz):**
* **Java 17+:** Temel programlama dili.
* **Apache Tomcat:** Java web uygulamalarını çalıştırmak için kullanılan web sunucusu ve Servlet/JSP konteyneri.
* **Servlet API / JSP:** Dinamik web içeriği oluşturmak ve HTTP isteklerini işlemek için.
* **MySQL:** İlişkisel veritabanı yönetim sistemi.
* **JDBC / Hibernate / JPA:** Java uygulamalarının veritabanı ile etkileşim kurmasını sağlayan teknolojiler 
* **Lombok:** Boilerplate (tekrar eden) kodları azaltmak için kullanılan kütüphane.
* **Maven:** Proje bağımlılık yönetimi ve derleme aracı.

**Frontend (Ön Yüz):**
* **HTML5:** Web sayfalarının yapısal iskeleti.
* **JavaScript (ES6+):** Sayfaların interaktifliği ve dinamik içeriği için.

## Kurulum ve Çalıştırma

Projeyi yerel makinenizde çalıştırmak için aşağıdaki adımları izleyin:

### Ön Gereksinimler

* Java Development Kit (JDK) 17 veya üzeri
* Maven
* MySQL Veritabanı Sunucusu
* Apache Tomcat Sunucusu (versiyonunu belirtin, örn: Tomcat 9.x)

### Adımlar

1.  **Projeyi Klonlayın:**
    ```bash
    git clone [https://github.com/KullaniciAdiniz/GaziShop.git](https://github.com/KullaniciAdiniz/GaziShop.git)
    cd GaziShop
    ```

2.  **Veritabanı Kurulumu:**
    * MySQL sunucunuzda `gazishop_db` adında yeni bir veritabanı oluşturun.
    * Veritabanı bağlantı bilgilerini ve şema oluşturma/güncelleme ayarlarını ilgili dosyalarda (örn: `persistence.xml` veya kendi yapılandırma dosyanızda) kendi MySQL yapılandırmanıza göre güncelleyin.

3.  **Backend'i Derleyin ve Paketleyin (WAR dosyası oluşturun):**
    * Projenin kök dizininde ( `pom.xml` dosyasının bulunduğu yer) terminali açın.
    * Aşağıdaki Maven komutunu çalıştırarak projenizi derleyin ve bir `.war` dosyası oluşturun:
        ```bash
        mvn clean install
        ```
    * Bu komut, projenizi derleyecek ve `target/` dizini altında `GaziShop.war` (veya `pom.xml`'deki `finalName`'e göre farklı bir isimde) gibi bir `.war` dosyası oluşturacaktır.

4.  **Tomcat Sunucusuna Dağıtın:**
    * Apache Tomcat sunucunuzun `webapps` dizinine gidin (örn: `C:\Program Files\Apache Software Foundation\Tomcat 9.0\webapps` veya `/opt/tomcat/webapps`).
    * Oluşturduğunuz `.war` dosyasını (`GaziShop.war`) bu `webapps` dizinine kopyalayın.
    * Tomcat sunucusunu başlatın (eğer çalışmıyorsa). Tomcat, `.war` dosyasını otomatik olarak açacak ve uygulamayı dağıtacaktır.

5.  **Uygulamaya Erişin:**
    * Uygulamanıza genellikle şu adresten erişebilirsiniz: `http://localhost:8080/GaziShop/` (Eğer `.war` dosyanızın adı `GaziShop.war` ise. Farklı bir isimse, o ismi kullanın.)
    * Frontend dosyalarınız (HTML, CSS, JS) eğer `src/main/webapp` altında yer alıyorsa, Tomcat tarafından sunulacaktır. Eğer frontend ayrı bir dizinde ve farklı bir şekilde çalışıyorsa, o kısım için ek talimatlar eklemeniz gerekebilir.

---
