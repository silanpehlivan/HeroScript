# HeroScript Mini Programlama Dili Tasarım Raporu

## 1. Giriş

Programlama dilleri, insan düşüncesini makine komutlarına dönüştüren yazılım geliştirme sürecinin temel taşlarıdır. Her dil, belirli bir mantık çerçevesinde kendine özgü sözdizimi (syntax), semantik (anlam) ve hedef kullanım alanı ile yapılandırılır. Özellikle yazılım dünyasına yeni adım atanlar için bu soyut kuralları kavramak, temel algoritma mantığını somutlaştırmak ve pratik yaparak tecrübe kazanmak kritik bir öneme sahiptir.

Bu çalışma kapsamında, oyun geliştirme dikeyinde uzmanlaşmış HeroScript adında özgün bir mini programlama dili tasarlanmıştır. HeroScript; özellikle RPG (Rol Yapma) ve macera türü oyunlarda karşılaşılan karmaşık NPC (Oyuncu Olmayan Karakter) davranışlarını yönetmek, dinamik görev (quest) mantıklarını kurgulamak ve temel oyun mekaniklerini (hasar hesaplama, envanter yönetimi vb.) kontrol etmek amacıyla özel olarak optimize edilmiştir.

HeroScript’in tasarım felsefesi, genel amaçlı dillerin (C++, Java gibi) karmaşıklığından kaçınarak, belirli bir problem alanına (Domain-Specific) odaklanıp bu alanda maksimum verimlilik sağlamaktır. Dil; "her şeyi yapan" devasa bir sistem olmak yerine, oyun mantığını en yalın ve anlaşılır şekilde ifade eden fonksiyonel bir araç olarak kurgulanmıştır.

Bu raporun ilerleyen bölümlerinde, HeroScript dilinin varlık nedeni, sözdizimsel kuralları, desteklediği özelleşmiş veri tipleri ve temel komut seti ayrıntılı olarak ele alınacaktır. Ayrıca, teorik bilgilerin pratiğe dökülmesini sağlamak amacıyla, oyun senaryolarını temel alan çeşitli örnek programlar sunularak dilin işlevselliği kanıtlanacaktır.

## 2. Dilin Adı

Bu proje kapsamında geliştirilen mini programlama dilinin ismi HeroScript olarak belirlenmiştir. İsim seçimi süreci, sadece estetik bir tercih olmanın ötesinde, dilin işlevselliği ve hedef kitlesiyle kuracağı psikolojik bağı temel alan stratejik bir karardır.

### 2.1. Semantik Analiz (Hero + Script)

İsim, iki temel bileşenin birleşmesinden oluşmaktadır:

- **Hero (Kahraman):** Dilin temel odak noktasını simgeler. RPG ve macera dünyasının merkezinde yer alan "kahraman" figürü, kullanıcının yazdığı kodların neyi kontrol ettiğini doğrudan somutlaştırır. Kullanıcı kod yazarken bir değişkeni değil, aslında bir kahramanın kaderini veya yeteneklerini yönettiği hissine kapılır.
- **Script (Betik):** Bu terim, dilin yapısını tanımlar. Karmaşık alt seviye dillerin aksine, HeroScript'in kolayca yorumlanabilir, hızlı yazılabilir ve belirli bir uygulama (oyun motoru) üzerinde çalışan bir "betik dili" olduğunu vurgular.

### 2.2. İsim Tasarımındaki Temel İlkeler

HeroScript isminin tercih edilmesinde şu üç temel ilke rol oynamıştır:

1. **Kavramsal Uyum:** İsim, dilin "oyun geliştirme" amacını hiçbir ek açıklamaya gerek duymadan kullanıcıya aktarır. Bu, öğrenme sürecindeki bilişsel yükü azaltan önemli bir unsurdur.
2. **Fonetik ve Akılda Kalıcılık:** Çift heceli ve ritmik yapısı sayesinde dilin ismi kolayca telaffuz edilebilir ve teknik literatürde hızla yer edinebilir. Kısa ve öz olması, modern yazılım ekosistemindeki (JavaScript, TypeScript vb.) isimlendirme standartlarıyla paralellik gösterir.
3. **Eğitimsel Erişilebilirlik:** Yeni başlayan öğrenciler için karmaşık ve soyut isimler (örneğin; "X-102" veya "Algol-Alpha") korkutucu olabilir. HeroScript ismi ise daha oyunsu (gamified) ve davetkar bir algı yaratarak, öğrencilerin programlama diline karşı olan çekincesini kırar.

HeroScript ismi, dilin hem teknik kapasitesini hem de eğlenceli dünyasını aynı potada eriten, profesyonel ama bir o kadar da kullanıcı dostu bir marka kimliğini temsil etmektedir.

## 3. Kullanım Amacı

HeroScript, modern yazılım dünyasının karmaşık sözdizimi kuralları altında ezilmeden, öğrencilere temel algoritma mantığını aşılamak amacıyla geliştirilmiş özel amaçlı bir eğitim dilidir. Dilin varlık sebebi, teknik bir araç olmanın ötesinde, mantıksal düşünme becerilerini geliştiren bir köprü görevi görmektir.

### 3.1. Algoritmik Düşünce ve Problem Çözme

HeroScript'in temel vizyonu, öğrencinin bir problemi atomik parçalara ayırabilmesini ve bu parçaları adım adım (step-by-step) bir çözüm setine dönüştürmesini sağlamaktır.

- **İşlem Sırası Takibi:** Kodun yukarıdan aşağıya doğru akan yapısı, öğrencinin bilgisayarın çalışma mantığını ve komut önceliğini kavramasına yardımcı olur.
- **Hata Farkındalığı:** Basitleştirilmiş hata mesajları ve net kurallar sayesinde öğrenci, mantıksal hataları (logical errors) ve yazım hatalarını (syntax errors) hızlıca ayırt etme becerisi kazanır.

### 3.2. Başlangıç Seviyesi Müfredat Uyumluluğu

HeroScript, temel bilgisayar bilimi eğitiminde yer alan kritik konseptleri kapsayacak şekilde optimize edilmiştir:

- **Değişken Yönetimi:** Bellek kullanımını ve veri depolama mantığını öğretir.
- **Akış Kontrolü:** Karar yapılarını (IF-ELSE) ve tekrarlı işlemlerin (WHILE) işleyişini somutlaştırır.
- **Veri Yapıları:** Bag (liste) kullanımı ile veri gruplama ve indeksleme kavramlarını sunar.

### 3.3. Oyunlaştırma (Gamification) ve İlgi Uyandırma

Eğitimi daha cazip hale getirmek için HeroScript, soyut matematiksel ifadeleri oyun ekosistemiyle harmanlar:

- **Somutlaştırma:** Bir döngü sadece bir matematiksel artış değil, bir NPC’nin (oyuncu olmayan karakter) kaç adım yürüyeceğini belirleyen bir komuttur.
- **Motivasyon:** Öğrenciler "Sayı toplama" gibi kuru işlemler yerine "Envanterdeki hasarı hesaplama" veya "Karakterin hayatta kalma durumunu sorgulama" gibi görevler üzerinde çalışarak daha yüksek öğrenme motivasyonu sergilerler.
- **Yaratıcılık:** Oyun içi mekanikler, öğrencinin kendi "kurallarını" tasarlamasına ve algoritmanın sonucunu görsel bir hikaye içerisinde görmesine imkan tanır.

HeroScript, öğrencilerin programlama dünyasına dair çekincelerini ortadan kaldıran, onlara algoritma kurmanın temel mantığını eğlenceli ve etkileşimli bir simülasyon üzerinden öğreten ideal bir pedagojik araçtır.

## 4. HeroScript'in Genel Yapısı

HeroScript, tasarlanma aşamasında "okunabilirlik" ve "takip edilebilirlik" ilkelerini merkeze alan emirsel (imperative) bir programlama yapısına sahiptir. Dilin mimarisi, öğrencinin zihnindeki algoritma akışıyla bilgisayarın işlem sırasını senkronize etmek üzerine kurulmuştur.

### 4.1. Sekansiyel Akış Mimarisi

HeroScript, komutların yukarıdan aşağıya (top-down) doğru bir sıra dahilinde işlendiği doğrusal bir çalışma modelini benimser.

- **Doğrusal Mantık:** Her komut, bir önceki komutun başarıyla tamamlanmasının ardından devreye girer. Bu yapı, özellikle karmaşık dallanma (branching) mantığına henüz hakim olmayan başlangıç seviyesindeki kullanıcıların kodun "izini sürmesini" (tracing) kolaylaştırır.
- **Tahmin Edilebilirlik:** Program akışında sürprizlere yer verilmez; veri girişi, işlenmesi ve çıktının üretilmesi net bir sıra dahilinde gerçekleşir.

### 4.2. Program Sınırları ve Kapsülleme (Encapsulation)

HeroScript'te her bir kod dosyası, programın yaşam döngüsünü belirleyen iki anahtar komutla sarmalanmak zorundadır:

- **açış başla** (Giriş Segmenti): Derleyiciye programın başlangıç noktasını bildirir ve gerekli çalışma ortamını (environment) hazırlar.
- **açış bitir** (Çıkış Segmenti): Programın tüm işlemlerini tamamladığını simgeler ve sistem kaynaklarını serbest bırakır.

### 4.3. Bu Yapının Avantajları

Bu disiplinli sınır belirleme yöntemi, öğrenciye şu teknik kazanımları sağlar:

- **Görsel Netlik:** Kod okuyucu, programın hangi satırda aktifleştiğini ve hangi satırda sonlandığını hiçbir karmaşaya yer bırakmadan görebilir.
- **Hiyerarşik Disiplin:** Programın sınırlarını çizmek, öğrencinin kod yazarken bir başlangıç ve sonuç odaklı düşünmesine yardımcı olur.
- **Hata Yönetimi Kolaylığı:** Programın bu iki komut dışında kalan bölümlerde işlem yapmaması, "program dışı" (out of scope) hatalarının önüne geçilmesini sağlar.

HeroScript'in genel yapısı, karmaşık sentaks kuralları yerine, mantıksal bir çerçeve sunarak kullanıcının tamamen "algoritma üretmeye" odaklanmasına zemin hazırlar.

## 5. Veri Tipleri

HeroScript dilinde dört temel veri tipi bulunmaktadır:

### 5.1. Int (Tam Sayı)

Int veri tipi, tam sayıları temsil etmek için kullanılır. Oyun bağlamında, karakterin can puanı, hasar değeri, seviye gibi sayısal değerleri depolamak için kullanılmaktadır.

Örnek:
```heroscript
Int hp = 100
Int damage = 25
Int level = 5
```

### 5.2. Dialog (Metin)

Dialog veri tipi, metinsel verileri temsil etmek için kullanılır. Oyun içi konuşmalar, NPC diyalogları, oyun mesajları gibi metinsel bilgileri depolamak için kullanılmaktadır.

Örnek:
```heroscript
Dialog character_name = "Aragorn"
Dialog quest_message = "Görevini tamamla!"
Dialog greeting = "Hoş geldin kahraman!"
```

### 5.3. Status (Mantıksal)

Status veri tipi, mantıksal değerleri (doğru/yanlış) temsil etmek için kullanılır. Karakterin yaşayıp yaşamadığı, bir görevin tamamlanıp tamamlanmadığı gibi iki durumlu bilgileri depolamak için kullanılmaktadır.

Örnek:
```heroscript
Status is_alive = Alive
Status quest_complete = Dead
Status has_weapon = Alive
```

### 5.4. Bag (Liste/Dizi)

Bag veri tipi, birden fazla değeri bir arada depolamak için kullanılır. Oyun içinde envanter, eşya listesi, hasar kayıtları gibi koleksiyonları depolamak için kullanılmaktadır.

Örnek:
```heroscript
Bag inventory = [sword, shield, potion]
Bag damage_values = [15, 20, 18, 22]
Bag quest_rewards = [gold, experience, item]
```

## 6. Yazım Kuralları ve Sözdizimi

### 6.1. Büyük/Küçük Harf Duyarlılığı

HeroScript dilinde büyük ve küçük harfler farklı anlamlar taşımaktadır. Komutlar büyük harfle yazılmalıdır (SAY, IF, WHILE), değişken adları ise küçük harfle yazılmalıdır.

Doğru kullanım:
```heroscript
SAY "Merhaba"
Int player_hp = 100
```

### 6.2. Noktalı Virgül (;)

HeroScript'te her komutun sonunda noktalı virgül bulunmalıdır. Noktalı virgül, komutun bittiğini gösterir.

Doğru kullanım:
```heroscript
SAY "Oyun başladı";
Int hp = 100;
```

### 6.3. Kod Blokları

HeroScript'te kod blokları köşeli parantezler [ ] ile gösterilir. Bu seçim, oyun içi diyalog metinlerinden kod bloklarını ayırt etmeyi kolaylaştırmaktadır.

Örnek:
```heroscript
IF hp < 30 [
    SAY SAY "Kritik durumdasın!";
];
```

### 6.4. Yorum Satırları

Kodun daha anlaşılır olması için yorum satırları yazılabilir. Yorum satırları // işareti ile başlar.

Örnek:
```heroscript
// Karakterin can puanını kontrol et
IF hp <= 0 [
    SAY SAY "Öldün!";
];
```

## 7. Örnek Kodlar

HeroScript dilinin kullanımını daha iyi anlamak için, beş farklı örnek program hazırlanmıştır.

### Örnek 1: Altın Toplama (Sayı Toplama)

```heroscript
açış başla

SAY "Sandıktan kaç altın çıktı?";
Int sandik_altini = INPUT;
Int cep_altini = 150;
Int toplam_altin = sandik_altini + cep_altini;
SAY "Yeni bakiyeniz: " + toplam_altin + " altın";

açış bitir
```

Açıklama: Bu program, kullanıcıdan bir sayı alır, bunu mevcut altın miktarına ekler ve sonucu ekrana yazdırır. Temel toplama işlemini göstermektedir.

### Örnek 2: Karakter Durumu Kontrolü (Koşul İfadeleri)

```heroscript
açış başla

SAY "Mevcut HP değerinizi girin:";
Int hp = INPUT;

IF hp >= 80 [
    SAY SAY "Durum: Çok sağlıklı, savaşmaya hazırsın!";
] ELSE IF hp >= 30 [
    SAY SAY "Durum: Yaralı, dikkatli ol!";
] ELSE [
    SAY SAY "Durum: Kritik, hemen iksir içmelisin!";
];

açış bitir
```

Açıklama: Bu program, karakterin can puanına göre durumunu belirler. Çok seviyeli koşul ifadeleri (IF-ELSE IF-ELSE) kullanılmıştır.

### Örnek 3: Kritik Vuruş Hesaplama (Modülüs Operatörü)

```heroscript
açış başla

SAY "Saldırmak için zar atın (1-20):";
Int zar = INPUT;
Int kalan = zar % 2;

IF kalan == 0 [
    SAY SAY "Çift geldi! Kritik vuruş yaptın!";
] ELSE [
    SAY SAY "Tek geldi! Normal vuruş yaptın.";
];

açış bitir
```

Açıklama: Bu program, zarın çift veya tek gelmesine göre farklı sonuçlar üretir. Modülüs operatörü (%) kullanılmıştır.

### Örnek 4: Kombo Hasarı Hesaplama (Döngü)

```heroscript
açış başla

SAY "Kombo yeteneği seviyesi:";
Int seviye = INPUT;
Int kombo_hasari = 1;

WHILE seviye > 0 [
    kombo_hasari = kombo_hasari * seviye;
    seviye = seviye - 1;
];

SAY "Toplam kombo hasarı: " + kombo_hasari;

açış bitir
```

Açıklama: Bu program, faktöriyel hesaplaması yaparak kombo hasarını belirler. WHILE döngüsü kullanılmıştır.

### Örnek 5: Hasar Ortalaması Hesaplama (Liste İşlemleri)

```heroscript
açış başla

Bag vurus_hasarlari = [12, 18, 25, 10, 30];
Int toplam_hasar = 0;
Int adet = COUNT(vurus_hasarlari);
Int i = 0;

WHILE i < adet [
    toplam_hasar = toplam_hasar + vurus_hasarlari[i];
    i = i + 1;
];

Int ortalama_hasar = toplam_hasar / adet;
SAY "Ortalama hasar: " + ortalama_hasar;

açış bitir
```

Açıklama: Bu program, bir liste içindeki değerlerin ortalamasını hesaplar. COUNT() fonksiyonu ve liste indeksleme kullanılmıştır.

## 8. Komutlar ve İşlemler

### 8.1. Temel Komutlar

- **SAY Komutu:** Ekrana mesaj yazdırmak için kullanılır.
  ```heroscript
  SAY "Merhaba dünya!";
  ```
- **INPUT Komutu:** Kullanıcıdan girdi almak için kullanılır.
  ```heroscript
  Int sayi = INPUT;
  ```
- **IF Komutu:** Koşullu işlem yapmak için kullanılır.
  ```heroscript
  IF hp < 50 [
      SAY SAY "Yaralısın!";
  ];
  ```
- **WHILE Komutu:** Döngü oluşturmak için kullanılır.
  ```heroscript
  WHILE i < 10 [
      // Döngü içeriği
  ];
  ```
