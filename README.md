# Apache Kafka

Apache Kafka, gerçek zamanlı veri akışı (event streaming) için kullanılan dağıtık bir mesajlaşma sistemidir.  
Büyük ölçekli ve yüksek hızlı veri iletimini güvenli ve performanslı şekilde sağlar.

---

## Apache Kafka Nedir?

Apache Kafka, producer ve consumer mantığıyla çalışan, verileri topic’ler üzerinden ileten açık kaynaklı bir platformdur.  
Özellikle gerçek zamanlı sistemlerde, mikroservis mimarilerinde ve log toplama işlemlerinde kullanılır.

---

## Kafka Ne Zaman Kullanılır?

- Gerçek zamanlı veri akışı gerektiğinde  
- Mikroservisler arası iletişimde  
- Log ve event toplama sistemlerinde  
- Büyük veri (Big Data) pipeline’larında  
- Bildirim ve mesajlaşma sistemlerinde  

---

## Kafka’nın Temel Bileşenleri

### Producer
Veriyi Kafka’ya gönderen uygulamadır.

### Consumer
Kafka’dan veriyi okuyan uygulamadır.

### Broker
Kafka sunucusudur. Veriler broker’lar üzerinde saklanır.

### Topic
Verilerin gönderildiği mantıksal kanaldır.

### Partition
Topic’lerin parçalara bölünmüş halidir. Performans ve paralellik sağlar.

### Zookeeper / KRaft
Kafka cluster yönetimi için kullanılır. Yeni sürümlerde KRaft tercih edilir.

---

## Kafka Nasıl Çalışır?

1. Producer mesajı Kafka’ya gönderir  
2. Mesaj ilgili topic’e yazılır  
3. Broker mesajı diskte saklar  
4. Consumer mesajı topic’ten okur  

---

## Kafka’nın Avantajları

- Yüksek performanslıdır  
- Yatay olarak ölçeklenebilir  
- Veri kaybına karşı dayanıklıdır  
- Gerçek zamanlı veri işleyebilir  

---

## Kafka’nın Dezavantajları

- Kurulumu ve yönetimi karmaşıktır  
- Öğrenme süresi uzundur  
- Sistem kaynaklarını fazla tüketebilir  

---

## Basit Kafka Mimarisi

Producer → Topic → Broker → Consumer

---

## Kullanım Alanları

- Finans sistemleri  
- E-ticaret uygulamaları  
- Log izleme sistemleri  
- IoT projeleri  
- Veri analizi platformları  

---

## Sonuç

Apache Kafka, büyük ve gerçek zamanlı veri işleyen sistemler için güçlü ve ölçeklenebilir bir çözümdür.  
Doğru senaryoda kullanıldığında sistem performansını ciddi şekilde artırır.
