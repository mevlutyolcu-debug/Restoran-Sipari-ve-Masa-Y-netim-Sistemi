# Restoran Sipariş ve Masa Yönetim Sistemi

## Proje Amacı
Bu projenin amacı, restoranların günlük operasyonlarını (masa durumu takibi, menü yönetimi, sipariş alma ve hesap kesim işlemleri) dijital bir ortamda yönetebilmesini sağlamaktır. Sistem, terminal (konsol) tabanlı çalışarak personelin hızlıca işlem yapmasına olanak tanırken, arka planda işletmenin günlük satış verilerini JSON formatında kalıcı olarak saklamaktadır. 

## Kullanılan Teknolojiler
- Python
- JSON (Veri okuma ve yazma işlemleri için)
- OOP (Nesne Yönelimli Programlama)

## Kullanılan OOP Yapıları
- **Class:** Masa, MenuUrunu, Siparis, Garson, RestoranSistemi sınıfları oluşturulmuştur.
- **Object:** Oluşturulan her masa, sipariş, ürün ve çalışan sınıflardan türetilmiş birer nesnedir.
- **Inheritance (Kalıtım):** `Garson` sınıfı, temel bir sınıf olan `Calisan` sınıfından türetilmiştir.
- **Encapsulation (Kapsülleme):** Masa sınıfındaki `__durum` ve menü ürünündeki `__fiyat` özellikleri gizlenerek dışarıdan doğrudan müdahale engellenmiş, property/setter metodları ile kontrollü erişim sağlanmıştır.
- **Polymorphism (Çok Biçimlilik):** `Calisan` sınıfındaki `calisan_bilgisi()` metodu, `Garson` sınıfı içerisinde üzerine yazılarak (override) farklı bir biçimde çalışması sağlanmıştır. Ayrıca sınıflarda `__str__` metotları ezilmiştir.
- **Abstraction (Soyutlama):** `abc` modülü kullanılarak `Calisan` isimli abstract class oluşturulmuş, soyut metotlar (abstract method) sayesinde şablon bir yapı kurulmuştur.

## Proje Özellikleri
- Masa ekleme ve listeleme (Durum kontrolü: Boş/Dolu)
- Menüye ürün ekleme ve ürünleri listeleme
- Masaya sipariş girme ve ara hesap görüntüleme
- Hesap kapatma ve masayı boşaltma
- Günlük satış raporu oluşturma
- Dosyaya kayıt (Verilerin `restoran_veri.json` formatında yedeklenmesi)
- Dosyadan veri yükleme (Kapanıp açılmalarda eski verilere erişim)

## Kurulum
Projeyi çalıştırmak için bilgisayarınızda Python kurulu olmalıdır. Google Colab üzerinde kod hücresine yapıştırılarak da doğrudan çalıştırılabilir.


