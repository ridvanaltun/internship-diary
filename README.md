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
