# Internship Diary

[ETOM Technology](http://etom.com.tr/) şirketinde yaptığım yazılım stajı, geçen günler ve yaptığım işler.

## Day-00

Staja ön hazırlık olarak şirkette benden sorumlu olan Özcan bey'in yönlendirmesi üzerine `Vue.js`, `Electron` ve `Vue Native` temelleri öğrenmeye başladım. Bunun üstüne `Vuex` yapısına baktım. Teorik olarak bir çok şey gördüm ve öğrendim.

## Day-01

Bugün ilk staj günümdü. İlk projemi aldım. Proje `kokpit.io` sistemi için kısmi bir mobil uygulama geliştirmek. Projeye `Vue Native` ile başladım ancak sonrasında `React-Native`'e geçtim. Bunun sebebi `Vue Native`'in olgunlaşmamış olması. 

Projemde `QR kod` okuma ve `URL encoding` gibi konular var.

Bugün ayrıca Github hesabım için bir `ssh key` aldım ve fork yapmadan pull request nasıl atılır -kısmen- öğrendim. Eğer proje sahibi bize branch açma yetkisi vermemişse direct pull request atamıyoruz, `fork-> pull request-> merge` sonrasında repoyu kaldırabiliriz, sorun olmaz.

## Day-02

Bugün `react-native-windows` adında bir proje olduğunu öğrendim. Bu proje ile `electron`'da uygulama geliştirmek yerine `react native` kullanarak windows için uygulama geliştirebiliyoruz. Bu yeni bir proje, 3 yıl kadar önce windows böyle bir şeyi yeniden denemiş şimdi aynı projeyi sıfırdan daha performanslı bir şekilde üretmişler.

Neden `electron` yerine `react-native-windows` kullanayım? Çünkü hem android, hem ios hemde windows için uygulama geliştirebiliyorum bu şekilde. Çok yeni olduğu için hakkında bilgi edinmek zor, konuyu anlamak için [şu ropörtaj](https://www.youtube.com/watch?v=Ga8oW0VUo2M) izlenebilir. Kısaca orjinal react native ile arasında minor farklar var, mobil için yazdığımız uygulamayı windows'a kolayca implemente edebiliyoruz.

Bunlar dışında üstüne çalıştığım projeye `redux` kurdum ve klasör yapısını düzenledim. `React-Native` pratiği yaptım.

## Day-03

Bugün üstüne çalıştığım uygulama üstünde major bir değişiklik yaparak QR kodu okuma kütüphanesini değiştirdim çünkü eski kütüphanenin algılama süresi yavaştı. Ayrıca QR kodu okuma sayfasına flash ışık açma-kapama komponenti ekledim. React-Native içinde aldığım bir çok build hatasının nedenini çözdüm ve geliştirme ortamım tam olarak kurulmuş oldu.

Yaptığım projeye kodun kalitesini korumak için `Editor Config`, `EsLint`, `Prettier`, `Husky` ve `Lint-Staged` ekledim ve ayarlarını yaptım. Bunun dışında projeye ait `markdown` formatında dokümanlar yazdım.

## Day-04

Bugün üstüne çalıştığım uygulama için 3 komponenetin tasarımını ve 3 sayfayı düzenledim. Proje'nin kod kalitesini yükseltmek amaçlı bazı algoritmaları değiştirdim. `Deep Linking` konusu üstüne araştırma yaptım ve uygulamaya ihtiyacım yönünde ekledim. `Deep Linking` mobil programcılıkta tarayıcı yada diğer uygulamalar üstünden hedeflenen bir uygulamanın istenen bir sayfasını vs. açma işine deniyor. Uygulama için bir sayfanın `header` bölgesine `dropdown menu` gerekiyordu, bunu modal ile değiştirmeye karar verdim. QR kodu okuyunca titreştirme özelliği ekledim.

React-Native biliyordum öncesinde ama unuttuğum yerler vardı, unuttuğum konuları proje ihtiyacı doğrultusudna tek tek yeniden öğrendim. Uygulama hızlı gelişiyor ve insanların problemlerine gerçekten yardım edecek özellikler geliştiriyorum.

Flash ışık açma-kapama komponentine QR kodu görünce otomatik ışık açma özelliği eklemek için araştırma yaptım, bu özellik kesin değil, eğer kullandığım komponenet izin verirse ekleyebileceğim bir şey.

## Day-05

Ofiste kimse olmaması yüzünden ve hafta sonu sebebiyle 4 gün evde boş zamanımda uygulamayı geliştirdim. Sonucunda bugün uygulamanın %90'ı bitti ve iş yerindeki insanlara gösterdim. Üstüne bazı kararlar aldık ve uygulama için yeni bir yol çizdik, bazı özellikler değiştiği için uygulama %50 bitti diyebilirim. Herneyse, bugün firmanın `git` servisine kaydoldum ve hesabım açıldı. Bunun dışında `asana` servisi ile bir `todo list` hazırlayıp öncelikleri sıraladık. Uygulama beklediğimden daha geniş bir seviyeye çekildi ve yeni özellikler hakkında konuştuk. Hazırladığım uygulama tüm `kokpit` servisini kapsıyor artık. Kokpit'i uygulamaya entegre etmek için `InBrowser` adında bir reack-native kütüphanesi kullanmayı planlıyorum.

Çoklu dil desteği eklenecek, bunun üstüne araştırma yapmam gerekiyor. `Deep Linking` mevzusundan vaz geçildi, uygulamanın `standalone` şekilde çalışması isteniyor. QR kod içindeki static veri yerine artık sunucudan veri çekme şeklinde olacak, yani artık QR kod içinde sadece id bilgisi barınıyor olacak.

Bu bir kaç gün içinde bir çok özellik ekledim, yanında bir çok şey de öğrendim; 

- Liste manipülasyonu
- Jsx rerender force
- Child Komponentten Parent komponenetin update ettirilmesi

gibi..

## Day-06

Bugün projeye `WebView` komponenti ekledim ve bu komponentin `props` ve `method`'larını öğrendim. WebView içine javascript kodu gömebiliyoruz, atılan isteklerin linklerini yakalayabiliyoruz, web sitesi ve react native uygulaması arasında iletişim kurabiliyoruz. Normalde `InBrowser` komponenetini kullanacaktım ancak github yıldızı düşük olduğu için offical olarak desteklenen komponeneti kullanmaya karar verdim.

Projeye `çoklu dil desteği` ekledim. Hatta bunun yanında ibranice ve arapça dillerinde olan `RTL` özellikli diller için uyum ekledim. Uygulamayı ingilizce ve türkçe olarak dil desteği de ekledim en sonunda.

Bugün `i18n`'in `internationalization` anlamına geldiğini öğrendim, 18 aradaki 18 harfi temsil ediyor.

Yürüttüğüm proje için kokpit sistemine özel bir API hazırlanıyor, API hazırladıktan sonra static QR kod okuma yapısını dinamik hale getiremem gerekiyor.

Yazdığım uygulama toplamda `1927` satır ve `27` dosyaya ulaştı. Projenin klasör yapısını güzel tuttuğum için ve temiz kod yazdığım için proje hızlı ilerliyor.