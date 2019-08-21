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

## Day-07

Bugün fazla kod yazmadım, günümü kullanacağım teknolojiler üstüne araştırma yaparak geçirdim. Axios, fetch, gesture handler, event emitter, intent launcher gibi konulara baktım. Bunun dışında projeye `Clean Code` ve `Advanced Usage` dokümanları yazdım.

`Expo` kütüphanelerini projede kullanmak için `unimodlues` adlı bir kütüphaneyi projeye entegre ettim. AndroidIntentLauncher kütüphanesini kullanılır duruma getirdim bunun yardımı ile çünkü kişi kamera izni vermediğinde sonradan tıklayıp izin vermesi gereken sayfayı açacak bir buton yaratmam gerekiyordu.

Django'da `migration` kavramını görmüştüm ancak neden yapıldığını bilmiyordum, Django'ya özgü bir şey sanıyordum, PHP ile de yapılabildiğini öğrendim. Kısaca migration yöntemi ile `database`'imize kolon ekleme, silme ve değiştirme yapabiliyoruz, ileride sürüm yönetimi kullanırken migration ile database'i manuel değiştirmek yerine otomatik şekillendirebiliyoruz.

Proje, müşteriye sunulmak isteniyor bu yüzden en basit haliyle bitirmem için 1 hafta süre verildi. Yapacağım şeyler kesin olarak kararlaştırıldı ve bir `guideline` oluşturduk. Proje için şuanda bir API hazırlanıyor, API hazırlanana kadar aynı anda uygulama geliştirebilmem için `hardcoded` bir API verildi.

Proje tam gaz ileri sürüyor.

## Day-08

Bir hafta içinde projeyi bitirmem gerektiği için haftasonu ve bugün proje üstüne geliştirmeler yaptım. Statik veri yapısını sonunda dinamik hale getirdim, bunun anlamı; Artık QR kodunu gösterince bir API'ye POST atıyoruz ve gelen cevaba göre uygulama şekilleniyor. QR kodu bastırmış kişi Kokpit hesabından QR içindeki verileri değiştirebilir demek. WebView komponentine `Javascript DOM Manpülasyonu` ile belirlediğim bir elemente buton gömdüm. Web sayfası içindeki buton tıklamasını algılayabiliyorum, uygulama üstünden istediğim sayfaya götürebiliyorum kullanıcıyı. Bundan sonra uygulama üstünden WebView'a girince eğer gösterdiğim id değerine sahip bir element varsa kod otomatik `inject` ediliyor.

Kullanıcı uygulamayı kapatıp açtığında verileri kaybolmasın diye `redux-persist` ve `async storage` kütüphanelerini entegre ettim, saklamak istediğim verileri de konfigüre ettim.

Asana üstündeki tüm öncelikli işler bitti. Önemli gördüğüm yeni `task`'lar oluşturdum ve yüksek öncelikli işler başlığı altına madde madde yazdım.

Uygulama için bir icon, splash screen ve logo bulmam gerekiyordu, raw materyalleri eposta ile aldım, gerekli düzenlemeleri yapıp bu materyalleri uygulamaya yedirmem gerekiyor.

Tüm bunlar dışında şirkette ki Tolga abi sohbet sırasında `Webpack`'in JavaScript vs CSS'de sadece kullandığımız parçaları sayfaya include edebildiğini öğrendim. Webpack nedir duymuştum ancak ben sadece kodu `minify` ve `bundle` ettiğini sanıyordum, meğersem kullanılmayan kodları çıkarma gibi bir işlevi de varmış. Peki bu bzie ne sağlar? jQuery, Bootstrap gibi framework'ler sayfamızı çok ağır hale getirebilir, kullanıcı deneyimi amaçlı sayfanın hızlı yüklenmesini isteriz. Sayfamızı Webpack'ten geçirirsek kullanmadığımız fonksiyonlar ve stiller sayfadan siliniyor.

## Day-09

Bugün `svg` uzantılı dosyaların react native içine nasıl çağrıldığını ve .svg dosyalarının pdf içinde tutulabildiklerini öğrendim. Photoshop programının tek tıkla .svg çıktı verebildiğini de öğrendim.

Üstüne çalıştığım uygulama için icon ve logo hazırladım, gelecek gün `splash screen` hazırlamayı planlıyorum. Bunlar dışında gerekli API'lar hazır olmadığı için uygulama içinde bazı bug ve mantık hatalarını düzelttim sadece. Kullanıcının bilgileri. API'ye post atabilmek için `sessionid` denen bir değere sahip olmam gerekiyor, bu değeri kullanıcı webview ile giriş yaptıktan sonra cookie bilgisini çekerek elde ediyorum. Sessionid ile kullanıcı post atabileceği için kokpit'e kolayca auth işlemleri için API yazılabilir, elimdeki işi bitirince bu konuyu açıp ileride uygulamanın login olma kısmını implemente edebilirim.

Uygulamayı `linter`'a sokup 144 tane linter hatası çözdüm. Projenin klasör yapısını ufak ta olsa değiştirdim. Önceden kulay kullanım amaçlı parçaladığım bir kaç dosyayı tek çatı altında birleştirdim çünkü ayrı kullanmak işimi kolaylaştırmak yerine zorlaştırıyordu.

Ufak mantık hataları dışında bir şey kalmadı, API hazırlanmasını bekliyorum.

## Day-10

Bugün `splash screen` tasarladım ve android'e entegre ettim. Splash screen tasarlamak kolay olur sanıyorum çünkü daha önceleri `expo` kullanırken 3dklık bir işti, react-native'de bu işi 2 saate çıktı, tüm ekranlara uyacak çözünürlükte resim hazırlamak derken 2.30 saate kadar çıktı. Bugün splash screen için native kod yazmak zorunda kaldım, `color.xml`, `string.xml`. `style.xml` gibi dosyalarla android bileşenlerine değişken nasıl yüklenir görmüş oldum. Android de `activity` yapısını gördüm.

`react-native-cookies` bağımlılığını projeden kaldırdım çünkü kütüphanenin `maintainer`'ı yok. Geliştirilmesi bırakılmış ve derlerken ufak ta olsa bir kaç uyarı mesajı veriyor. Bu kütüphane yerine Webview'a cookie döndüren bir javascript kodu yazdım ve dönen sonucu işleyip obje haline getirecek bir fonksiyon yazdım.

Bunun dışında webview üstündeki kokpit login ekranında kullanıcı giriş yaparken normalde dil seçiyor ve ona göre giriş yapıyor. Çoklu dil desteğini login ekranındaki dil seçim yapısına entegre ettim. Artık kişi login olurken seçtiği dil ile uygulamayı kullanabiliyor.

Projeyi react-native `0.59.4`'tan `0.60.4`'a geçirmeye çalıştım. Projede kullandığım bazı kütüphaneler AndroidX desteklemediği için derelme hataları geldi, `jetifier` adında bir programı projeye entegre ederek hataalrdan kurtuldum ancak proje derlense bile telefonda açılmıyordu. Bu sebeple eski sürüme geri döndüm.

## Day-11

Bugün ilk defa git sunucusuna commit attım. Splash screen sonrası oluşan status bar sorunu vardı, onu çözdüm. Lint-staged aracını yanlış konfigüre etmişim, onu düzelttim. Webview içinde site dışından bir linke tıklandığında telefondaki tarayıcıdan açtırma özelliği ekledim.

Android Lolipop kurup uygulamanın teoride desteklediği en düşük sürümü emülatörde denedim ve sorun olmadı, güzel çalışıyor. Koleksiyon özelliği için uygulamada bir altyapı vardı, bu özellik pratikte pek kullanılmayacağı için altyapısını kaldırdım.

Bugün ayrıca `lottie` adı verilen bir kütüphaneyi entegre ettim, bu kütüphanein amacı `adobe after effects` ile tasarlanan animasyonları uygulamaya yerleştirebilmek. Hata aldığım için kurulumu kaldırmak zorunda kaldım.

## Day-12

Bugün Kokpit API'ına `POST` isteği atabilmek için `Postman` adında bir yazılımı kullanmaya başladım. POST atarken `body` kısmına data, `header` kısmınada `auth` bilgileri konduğunu öğrendim. API dokümantasyonu yazabilmek için `Swagger` adında bir dokümente aracı kullanıldığını öğrendim. Bugün ilk defa `release` aldım ve uygulamayı `production mode`'unda test ettim, release alırken karşıma çıkan sorunları çözdüm. İnternet yavaşlığında kullanıcı deneyimini arttırmak için loading ekranları tasarladım ve uygulamanın gerekli gördüğüm yerlerine koydum.

`CodePush` adında bir teknolojinin varlığını öğrendim, normalde bir uygulamayı güncellediğimizde IOS için günlerce Android için saatlerce beklemek zorunda kalıyoruz. React-Native ve Cordova ile `hybrid` yapıları sayesinde bu sorunu aşmak mümkün. Yaptığımız tüm değişiklikler anında uygulamanın yüklü olduğu telefonlara `CodePush` sunucusu üstünden yüklenebiliyor.

Bunun dışında uygulamanın ikonuna `badge` eklemek için araştırma yaptım. IOS ta bu iş standart ancak Android'de şirketler kendilerine has `launcher` çıkardıkları için sabit bir çözüm ve native bir destek yok, yine de Android'de bu işi yapan 3. parti kütüphaneler var. Uygulama ikonuna badge eklesek bile her telefonda bu badge gözükmeyecek çünkü react-native için 3. parti kütüphaneler popüler değil.

Bugün HTTP kodlarını kediler üstünden anlatan [bu hoş siteyi](https://http.cat/) buldum.

## Day-13

Bugün PDF uzantılı bir dosyadan vektörel bir grafik çıkardım, bu işi yaparken `inkspace` adlı bir yazılım kullandım. Amacım çıkardığım vektörel resimleri app içinde kullanmaktı ama hatalar yüzünden başarılı olamadım. `Async` işler için bir loading komponenti hazırladım ve appteki `fetch` kullandığım yerlere yerleştirdim. Bugün yazdığım app incelendi ve maddeler şekilde yapılması gereken ve değiştirilmesi gereken şeyler listelendi, aynı gün içinde istenilen şeyleri yerine getirdim.

Notification için araştırmalar devam ediyor, Kokpit'in hali hazırda bir notification sistemi olduğu için `best practice` yerine Kokpit'e özel bir notification sistemi düşünülüyor. Notification sisteminin temelde nasıl çalıştığını öğrendim ve altyapıyı nasıl kurmam gerekeceği hakkında bir fikir sahibi oldum.

App'in navigator yapısı tamamen değiştirildi. NavigationService adında ektra bir bölüm vardı o yapıyı kaldırdım ve kodu basitleştirdim.

## Day-14

Bugün pek kod yazmadım, `docker` nedir ne diğildir, nasıl kullanılır bunları öğrendim. Bunun sebebi kapalı sistemler için uygulamaya `notification server` entegre etmekti. Normalde notification server için Firebase, Google, Apple, Amazon vs. şirketlerin `cloud messaging` servisleri kullanılıyor.

Belli başlı notification servisleri:

- `FCM` -> Firebase Cloud Messaging
- `GCM` -> Google Cloud Messaging
- `APNS` -> Apple Push Notification Service


`docker-compose` adlı bir aracı kullanmayı öğrendim. Docker ile `nginx`, `php-fpm` ve `php`  birlikte bir konteynır olarak ayağa kaldırdım. İlk docker tecrübem bu oldu. `Apache` ie `nginx` arasındaki farkları öğrendim. `Dockerfile` yapısını ve neden kullanıldığını öğrendim. Bunun dışında `docker-compose.yml` dosyalarındaki `volume` yapısını öğrendim ve tüm öğrendiğim şeyleri not aldım.

Tüm bunları öğrenmemin sebebi `notification server` ayağa kaldırmak olsada sonradan bundan vazgeçildi. Bunun 3 sebebi var;

- Kokpit'in kendine has bir bildirim sistemi var.
- Kapalı sistemler ile çalışmamız gerekiyor.
- Client için yazılmış bir kütüphane local bildirimlere izin veriyor.

QR kod için gerekli olan API hala bitmedi, halen `dummy data` kullanıyorum.

## Day-15

Bugün `git branch` sistemini öğrendim. Aslında konuyu yarım yamalak biliyordum ancak bugün kafama tam oturdu. Özetle, `branch` açınca aslında bulunduğumuz branchin kopyasını oluşturmuş oluyoruz ve `checkout` parametresi ile farklı bir branch'e geçiş yapınca bilgisayarımızda bulunan klasör ve dosyalar git sayesinde aktif branch te ne varsa ona dönüştürülüyor. Bu şekilde `master` branch'ine versiyon adı içeren bir branch açıp onun üstüne `feature` branchi açıp geliştirme yapabiliriz. Git programı `diff` üstünden dosya değişikliğini takip ederek işlem yaptığı için branch açınca dosyamız neredeyse hiç büyümüyor.

Bugün bana geliştirdiğim uygulamanın `manager` uygulaması olduğunu, bu uygulamayı satın alan şirketteki yönetici insanların kullanacağı söylendi. Şimdi ise aynı temelleri paylaşan ve bazı minor ve major değişiklikleri olan `customer` uygulaması geliştirmem isteniyor. Bu sebeple git branch sistemini öğrendim. Uygulamaya customer ve manager olmak üzere 2 branch açtım, master branchi içinde sadece dokümantasyon tutmayı planlıyorum. Uygulama normalde master branch'indeydi ancak şimdi aynı temeli paylaşan 2 farklı uygulamayı tek bir git deposunda tutuyorum artık.

Bugün `sublime text 3` editöründen `atom` editörüne geçiş yaptım. Atom için pluginler kurup geliştirme ortamımı hazırladım. Sublime kadar hızlı bir editör olmasada çok daha gelişkin bir plugin desteği var.

## Day-16

Bugün tek bir problem için 4-5 saat uğraştım. Karşıma çıkan problem sadece hatanın hangi bileşende olduğunu söylüyordu, hiç bir bilgi vermiyordu bu sebeple tüm kodu debug etmek zorunda kaldım. Sonun hata çözüldü ama basit bir şey için saatlerim gitti.

Her neyse, bugün asana üstünde tanımlanmış ve uzun süredir bekleyen görevi yerine getirdim. `crashlytics`, `fabric.io` ve `apphub` konularını araştırdım. Yazdığım uygulama hangi hataları hangi sistemlerde veriyor vs. takip etmek gerekiyor bu sebeple yazılmış servislere bakındım.

`socket` bazlı Kokpit'e özel bir `push notification server` diagramı çıkardım ve şirketteki yetkili bir elemanla paylaştım. Bunun üstüne kullanacağımız teknolojiyi konuştuk.

Uygulama biteli çok oldu ancak API hala hazırlanıyor. `customer` adında geliştirdiğim ikinci mobil uygulaması ha bitti ha bitecek, bu yeni uygulama için de yeni bir API hazırlanacak. Bir kaç gün öncesinde ETOM'a ait Kokpit'ten farklı bir mobil uygulaması fikri üstüne konuşmuştuk, muhtemelen her şey bitince o projeye başlıcam.

## Day-17

Kokpit Mobile için doküman çıkarmayı planladık. Öncelikle uygulamayı tanımlayan bir doküman yazılacak. Daha sonra teknik doküman çıkartılıp gerekli teknolojiler belirlenecek en sonunda `iş planı` hazırlanıp tarihler belirlenecek.

Uygulamayı geliştirmeye başladığım günden beri dinamik bir şekilde değişiyor. Bazı zamanlar major değişimler isteniyor. Bu sebeple uygulamayı dokümante etmek şart oldu.

Bugün `kokpit customer` uygulamasını ayağa kaldırana kadar çıkan hataları çözdüm. Bu uygulamada başlar başlamaz bitti ancak bu uygulama için de iş planı gerekiyor. API hazırlanana kadar boş durmamak için geliştirdim ve bugün geliştirmesini bıraktım, eğer ETOM'dan istek gelirse verdikleri doküman doğrultusunda geliştirmeye devam edicem.

`customer` uygulaması için `kiosk mode` denen bir şeyi entegre etmem gerekiyor. Kullanıcı sadece uygulama ile etkileşime girebilmeli, hiç bir şekilde uygulamayı kapatamamalı hatta telefon açılırken uygulama otomatik olarak başlamalı. Bu işi çözmek için internette araştırmalar yaptım ve native kod yazmam gerektiğini öğrendim. İş planı ve teknik doküman çıkarılmadığı için `kiosk mode` entegre etme işine ara verdim.

Bugün kodu daha okunabilir kılmak için düzelttim. Üstüne daha fazla kod yazamıyorum çünkü bana bu yönde istek gelmesi gerekiyor.

Herneyse, atom editörünü aktif kullanmaya başladım ve bir sürü paket yükledim. Çok garip bir şekilde sublime'da olmayan bir çok özellik atom için yazılmış.

## Day-18

Bugün `token` işi süpriz bir şekilde tamamlandı. WebView elementine `fetch` fonksiyonu içeren bir javascript kodu gömerek `token` elde edebiliyorum. Artık token elde edebildiğim için kullanıcı adı şifre olmadan `API`'ya istekler atabiliyorum. İleride eklemeyi planladığımız bildirim sistemi içinde bu token kullanılacak.

`JWT` denen `auth` stratejisini araştırıp öğrendim. Projede kullanmak için araştırmıştım ancak token işi zaten çözüldü. `Levenshtein Distance` adında bir algoritmanın varlığını öğrendim ve bununla ilgili olarak `elasticsearch` nedir ne değildir nerelerde kullanılır öğrendim.

Beş gündür üstüne parça parça uğraştığım `lottie` entegrasyonunu bugün başardım. Artık `Adobe After Effects` ile hazırlanmış animasyonları mobil uygulamada kullanmak üzere `export` alabiliyoruz. Bu işlem için `Adobe AE`'ye `Bodymovin` adında bir eklenti yüklememiz gerekiyor, export alma işlemi çok basit.

`Firebase`'i entegre ettim ve artık `Firebase API`'larını uygulama içinde kullanabilir hale geldim. Bunun üstüne `Crashlytics` servisini entegre ettim ve artık uygulama çökünce çökme raporları Firebase üstündeki crashlytics paneline geliyor. Bu şekilde artık sık sık gelen hataları görüp uygulama içinde gereken düzeltmeleri sağlayabiliriz.

`Firebase` entegrasyonu için `react-native` paketini `0.59.10` dan `0.64`'e yükseltmek zorunda kaldım. Önceden de denemiştim bunu ancak başarılı olamamıştım. Bazı major değişiklikler olduğu için kod patladı ancak tane tane tüm sorunları çözerek entegre ettim ve native kodu okuma yeteneğim gelişti diyebilirim, artık gözüme daha az korkunç geliyor. Bu yükseltme işi sayesinde `lottie`'yi entegre edebildim zaten. 

## Day-19

`Crashlytics Beta` adlı bir servise başvuru yaptım, bu servis `Firebase Alpha` programında ve başvuru yapıyoruz kullanabilmek için, eğer başvurumuzu kabül ederlerse kullanabiliyoruz. Bugün başvuru yaptım ve yanıt bekliyorum. Bu servis ile test işlemleri kolaylaşıyor, şöyle ki uygulamanın yeni sürümünü anında test kullanıcılarına gönderebiliyorum, marketten indirmelerine yada manuel yollarla apk indirmelerine gerek kalmıyor.

Kokpit'ten `token` almam gerekiyordu çünkü token'ı kullanarak işlem yapabiliyorum, sorun şu ki `postman` kullanarak token alamıyordum çünkü kullanıcının önceden giriş yapmış olması gerekiyordu ve `postman` tarayıcıdan bağımsız olarak yürüyor. Benim düşümcem, normalde login sistemi için API yazılması ve webview üstünden giriş iptal edimesi. Native yollarla giriş yapmak ve token almak. Bu yol zahmetli olduğu için `workaround` kullanmıştık. Her neyse, tarayıcıdan çalıştığımızda token alabiliyorduk ancak `POST` işlemi yaparken sıkıntı çekiyorduk çünkü bu işi yapacak -siteye özel post atma- bir araç yok. Neyse ki bu problemi `chrome dev tools` içindeki konsola `fetch` fonksiyonu yazarak çözebildik.

Dün liste şeklinde verilen şeyleri yapmaya başladım, yeni bir şey pek öğrenmedim. 

## Day-20

Bugün lokasyon özelliği eklemeye çalıştım. React Native'in bize `geolocation` adında sunduğu bir kütüphane var ancak bu kütüphaneyi resmi kaynak önermiyor çünkü tüm kullanıcılar uygulama geliştirebilsin diye farklı bir şekilde geliştirilmiş. Örneğin Çin'deki kullanıcıların telefonunda `Google Play Store` yok, normalde geolocation için google play servisi üstünden çalışıyoruz ancak dediğim gibi bu sefer telefonunda Play Store olmayan'lar bundan yararlanamaz. Ayrıca eski bir Play Stroe varsa elimizde yine bundan yararlanamıyoruz bu sebeple farklı bir şekilde geliştirilmiş uygulama ve yavaş olduğu söyleniyor.

`Geolocation` nedir ne değildir bugün bunu öğrenme fırsatım oldu. Normalde uydu verileri ile konum tespiti yaparken bu teknikle internete bağlı diğer cihazların verileri, IP adresi bazlı vs. ile arkada dönen bir hesapla konumumuz tespit edilebiliyor.

`Fine Location` diye bir şey öğrendim, normalde her uygulama 100% doğrulukta yer tespine ihtiyaç duymuyor, sadece bulunduğumuz ilçe yetebiliyor mesela uygulama için. Konumumuzu eğer uygulamayı yazan kişi izin vermişse bulanık gösterebiliyoruz. Eğe yüksek derecede doğruluk istiyorsak `Fine Location` denen izinle lokasyon izni alıyoruz.

Bügün yine rutin olarak listemdeki özellikleri geliştirdim. Proje temelleri oturduğu için ve istekler spesifik hale geldiği için öğrenmekten çok algoritma geliştirmeye ve proje yapısını yeni özelliklere uygun hale getirmeye ayırıyorum zamanımı.

## Day-21

Bugün elimdeki tüm işleri bitirdim, sadece bildirim sistemi kaldı ki onun API'ı 1 saat içinde yazıldı. Günün son dakikalarında kritik bir bug çıktı, onu yarın çözücem. Bildirim sistemi üstünde test amaçlı kod yazmıştım o yüzden kısa bir süre içinde implemente etmeyi planlıyorum. 

Elimdeki liste bitince muhtemelen yeni bir projeye başlıcam.

## Day-22

Bugün dünden kalan kritik bir hatayı çözdüm. Bunun üstüne kod yazamadım çünkü Android Release alırken hata alıyordum ve hatayı debug etmem ve çözmem gerekti. `CI` aracı kullansaydım böyle bir hatayı erken tespit edip gerektiği zaman müdahele edebilirdim ancak `CI` entegrasyonu olmadığı için git üstünden test branch'i açarak eski commitlere gitmem gerekti. Tüm günümü bu hataya ayırdığım için `CI` entegrasyonu yapmaya karar verdim ve temellerini öğrenmeye başladım. Şirkette `GitLab` kullanıyoruz ve GitLab'a gömülü olarak `GitLab CI/CD Runner` aracı geliyor. Yani `travis`, `jenkins` gibi ekstra bir servis kullanmamıza gerek yok tek bir çatı altında hem git deposu hem CI aracımız var. GitLab'ın CI aracını öğrenmeye başladım ve yakında projeye entegre edeceğim.

`FontAwesome 4` ile `FontAwesome 5` arasındaki farkı öğrendim. 4. versiyonda `fa` kullanıyoruz, 5. versiyonda ikon tipine göre yani solid etiketli bir ikonsa `fas` vs. şeklinde kullanılıyor.

Bugünkü planım bildirim sistemini bitirmekti ama çıkan hata yüzünden kod yazmaya fırsat bulamadım.

Bugün ayrıca `Atom`'un yavaşlığından bıkıp `VSCode`'a geçtim.

## Day-23

Android'de çıkan hatayı erkenden çözdüm. Htanın sebebi bundle dosyasını derleme esnasında oluşturmaması. Bu sebeple runtime error alıyorduk. Çözüm için bir `NPM script` yazdım ve derleme yaparken ilk adım olarak artık farklı bir komutla bundle oluşturup ardından derleme işine geçiyor.

`VSCode`'a alıştım. Sol tarafta dikey bir menü olması garibime gidiyor sadece. Sublime Text, VSCode yanıdna `Zen Mode`'u açılmış gibi bir havası var. Sublime Text ile yazı yazmak halen daha zevkli. İleride VSCode'u Sublime Text kadar yalın bir şekle sokmak istiyorum. Sadece ihtiyacım olduğunda sol dikey menü önümde olmalı mesela.

Bildirim sistemini implemente etmeye çalışırken android hakkında çok şey öğrendim. Normalde bildirim sistemi kurarken hali hazırda bu işi yapan bir servis kullanılır `FCM` vs. Biz API yazıp bunun üstünden halletmek istiyoruz çünkü Kokpit'in kendine has bazı `case`'leri var. Benim arka planda sürekli olarak gelen yeni bildirimleri takip etmem ve gelince `local` olarak bildirim oluşturmam gerekiyor. Uygulama arka plana atıldığında yada kapatıldığında yine de çalışması gerekiyor, yani bu durumda Android için `service` ve IOS için `Background Task` yazmam gerekiyor.

IOS pil tüketimini kısmak için bize en az 15dk da bir arka planda kod çalıştırmamıza izin veriyor ve maksimum 30 saniye boyunca kod çalıştırabiliyoruz. Ayrıca IOS arka planda task çalıştırma konusunda tam bir kara kutu. Diğer geliştiricilerin tahminine göre arka planda bir `machine learning` algoritması var. IOS, arka planda çalışmasını istediğimiz kodu ne zaman çalıştıracağını kullanıcının uygulamayı kullanma alışkanlığına göre kendi belirliyor. Yani biz minimum 15dk ayarlasak bile mesela uygulamayı ilk defa test amaçlı olsa bile telefona yüklediğimizde arka planda çalışmasını istediğimiz kod bir sonraki güne kadar çalıştırılmayabilir.

Android için böyle bir durum yok ancak arka planda kod çalıştırma implementasyonu zor. Öncelikle yazdığımız uygulama ile Android servisinin iletişim kurabiliyor olması lazım, buna köprü kurmak deniyor ve React-Native bu iş için `HeadlessJS` adında bir şey üretmiş. Android'de native kod yazan biri değilseniz implemente etmek çok zorlaşıyor zira ne resmi doküman nede diğer kaynaklar bu teknolojiyi dokümente etmemiş. Bugün 5 saatimi bunu implemente ederek harcadım ama başarısız oldum. Bu sebeple yöntemimi değiştirmeye karar verdim, `react-native-background-fetch` adında bir kütüphaneye geçtim, belki ileride `HeadlessJS` ile tekrar şansımı denerim.

`Gitlab CI/CD Runner`'ı implemente ettim ancak her commit sonrası uzun bir pending kısmına giriyor ve en sonudna fail veriyor, bunun sebebi de android'i derleyebilmek için çok fazla kaynağa ihticımız olması. Kendi bilgisayarımda deploy amaçlı build almak sitediğim zaman ortalama 11-12dk sürüyor mesela. Problemi çözmek için manuel olarak GitLab server yöneticisinin projeye kaynak ayırması gerekiyor ki işlem hızlı yapılabilsin ve timeout'a düşüp fail vermesin.

Geri tuşuna basınca WebScreen üstünde eğer geri gidebiliyorsak geri giden, gidemiyorsak uygulamadan çıkan bir yapı koydum çünkü kullanıcılar geri tuşuna basınca uygulamadan istemeden de olsa yanlışlıkla çıkıyordu. Kullanıcı deneyimi bu şekilde artmış oldu.

Yarın background task işlemini bitirmeyi planlıyorum.

## Day-24

Background Task işlemi bitti ancak içine API'ı yerleştiremedim çünkü API'da bazı hatalar vardı ve gün sonunda çözülebildi. Bildirim sistemini 5 gün sonrasına kadar bir bitirme sürem var, 5 gün sonrasında ufak yerleri düzeltip sonraki günde test ve `Google Play Store`'a yüklemeyi düşünüyoruz.

GitLab CI/CD entegrasyonu bugün yapıldı. Tüm sistemi bugün anladım. Projemiz için bir `task runner` oluşturmamız gerekiyor, bir token üstünden GitLab'a bunu bağlıyoruz. Tüm CI operasyonu task runner kurduğumuz sunucu üstünden gerçekleşiyor. Birden fazla task runner sunucusu kurup CI işlemini hızlandırmamız mümkün. Bunun için tabi paralel çalışabilecek job'lar yazmamız gerekiyor. Örneğin üstüne çalıştığım projede Android ve IOS için paralel bir şekilde derleme ve deploy işlemi gerçekleşebilir. 30dk sunucuyu meşgul etmek yerine 15dk-15dk ayrı sunucularda paralel bir şekilde işlemleri yaptırabiliriz.

Eskiden -2005 civarı- Apple, `macOS Server` adında bir ürün çıkarmış -Windows Server gibi- ama başarısız olmuş. IOS uygulamasını derleyebilmem için macOS bir bilgisayara ihtiyacım var bu sebeple araştırma yaptım.

CI için hazırladığım konfigüreasyon dosyasında bir çok mantık hatası vardı, projeye task runner atayınca hataları görme şansım oldu çünkü pending modundan çıkıp hazırladığım konfigürasyon dosyası çalıştırıldı ve adım adım izledim ne olup ne bitiyor diye. Bulduğum çoğu hatayı düzelttim ancak daha bitiremedim.

Bugün `Google Cloud` üstündeki açabileceğimiz disk yapılarını gördüm, `Coldline`, `Region`, `Multi-Region` vs. Bunun üstüne `arthifacts server` adında derlediğimiz veya bir işlem sonucu ortaya çıkan uygulamaları sürümüne göre arşivleyen servisler olduğunu öğrendim.

Uygulamyı daha önce tablet üstünde denemiştik, tablet üstünde denerken bir kaç stil hatası çıktı, bugün ufak tefek bazı stil hatalarını çözdüm ancak o da bitmedi. Bildirim sistemi bitince stil hatalarını bitirip Google Play için hazır hale getirmek istiyorum.

Bugün fetch sonrası ezbere çalıştırdığım `response.json()` komutunun aslında ne olduğunu öğrendim. Normalde response alırken response nesnesi içinde json adında bir fonksiyon var, yani dönen cevabın içindeki fonksiyonu çalıştırıyoruz ve bize body üstünden iletilen json verisini döndürüyor. response içinde fonksiyon göndermesi çok garibime gitti açıkçası.

Günün sonlarında `Git Stash` denen naneyi öğrendim. Normalde çalıştığım branch üstünde commit'lenmemiş dosyalar varsa başka branch üstüne geçemiyoruz. Hatta push yapamıyoruz. Bu durumda değişiklik yapılmış dosyaları bir stash içine alıp diğer işlemlerimizi yapabiliyoruz. Sonrasında stash içindeki değişiklikleri uygula diyerek geri döndürüyoruz. `Stash`'in türkçe karşılığı zaten saklamak.

## Day-25, 26 & 27

Bildirim sistem bitti. `Google Play Console` hesabı açtık ve uygulamayı incelenmek üzere gönderdik, incelme işi bitince Play Store'da yayınlanacak. Yayınlama işini ben üstlendim ve android için uygulama yayınlarken ne yapılır öğrenmiş oldum. Uygulamada ufak stil hataları dışında bir şey kalmadı. `MVP` sürümü çıkardık artık müşteriye sunulabilir. Bundan sonra geri bildirimlerle ekstra özellikler eklenecek.

Tüç işlerim bittiği için asana'da duran bir özelliği geliştirmeye başladım. Manuel ürün ekleme özelliği, qr kod okunamaz bir haldeyse ürün kodunu elle girerek ürün ekleyebilmeyi sağlayacak. Bu özelliğin temelini yazdım kalan kısmını yarın bitirmeyi düşünüyorum.

Uygulamayı sürüm adı vermeyi öğrendim.

- Prototype
- POC (proof of concept)
- MVC (minimum viable product)
- Alpha
- Beta
- Launch 

İlk başta bir prototip çıkartılıyor, UX tasarımı vs her şey burada belirleniyor. POC ile testler yapılıyor ve hangi teknolojiler seçilecek bu özellik olur mu olmaz mı diye yazmaya başlıyoruz, elimizdeki veriler hardcoded olmalı API beklememize gerek yok. Sonrasında tüm olmasa da olur özellikleri eleyip (push notification vs) MVC sürümü çıkartıyoruz, bu sürümde elimizdeki datalar API ve hardcoded olmak üzere iki şekilde de olabilir. Sonrasında alpha sürümünde temel şeyleri geliştiriyoruz, bu sürüm halen kullanıcıya sunulacak yapıda değil, ekip içi uygulamayı test edip geri dönüşlerle geliştirme yapılıyor. Beta'ya geçince daha az `breaking change` yapacağımız için hedef kullanıcı kitlesine beta sürümü altında dağıtabiiyoruz, hedef kullanıcılardan aldığımız dönüşlerle uygulamayı şekillendiriyoruz. Beta sürümün bir yararı, erken hata tespiti, ullanıcıalrın uygulamaları crash oldukça elimize gelen hata raporları ile ileride çok büyük dert olacak sorunları burada çözebiliyoruz. En sonunda hedeflerdiğimiz prototipe ulaşınca launch sürümü çıkıyor ve uygulamanın sürümü 1.0.0 artık.

Bundan sonra şirket içinde yapacağım uygulamalara bu şekilde geliştirmeye özen göstericem. Hatta ve hatta bu semantik versiyonlama hakkında bana yardımcı olabilecek araçları araştırmaya başladım. Yakında projeye dahil edip otomatik sürüm numarası verme gibi şeyler eklemeyi düşünüyorum.

Proje rayına oturduğu için öğrendiğim pek bir şey yok, artık major değişiklikler yerine minor ve patch yazıyorum genellikle. Bu sebeple anlatacak bir şey çıkmıyor.