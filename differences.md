# JavaScript ve TypeScript Arasındaki Farklar
Javascript front-end tarafında kullanılan statik web sitelerini dinamik hale getiren bir programlama dilidir. Zaman içerisinde geliştiriciler javascript’i back-end kullanmaya başladılar. Ancak javascript ile çalışmak bu alanda çeşitli nedenlerden dolayı zorlaştı ve javascript’in eksikliklerini tamamlayacak TypeScript ortaya çıkmıştır.

Typescript, amacı açısından javascript'ten farklı değildir, ancak büyük uygulamalar geliştirmek için kullanılır. Typescript'i javascript ile yazılan uygulamanızı daha düzenli ve yazılı hale getiren bazı ek özellikler olarak düşünebilirsiniz. Typescript javascript'e derlenir(trans compiled : kaynaktan kaynağa derleme). Tarayıcılar doğal olarak Typescript anlamazlar, ancak javascript'i anlarlar. Yani Typescript kodlarını çalıştırmak için önce javascript'e aktarılır.

Javascript en sevilen istemci tarafı betik dilidir. javascript doğrudan tarayıcıda çalıştırıldığından, küçük kod parçalarını çalıştırmak, yenilemek ve hatalarını ayıklamak daha kolaydır. Javascript, esnekliğin bir öncelik olduğu durumlarda harika bir seçimdir çünkü aynı kurallara bağlı kalmadan işlevsellik oluşturmanıza olanak tanır. Ancak, hıza öncelik verirken tek bir standarda getirmek istediğiniz büyük bir kod tabanıyla uğraşıyorsanız, Typescript en iyi seçeneğinizdir. Kodunuz büyüdükçe ve işlemesi daha karmaşık hale geldikçe, derleme süresi sırasında yakalanması daha iyi olan hata olasılığı artar.

Bazı yazılım diller  hatalı programların çalışmasına hiç izin vermezler. Koddaki hataları çalıştırmadan algılamaya statik kontrol denir. Neyin hata olduğunu ve neyin üzerinde çalışılan değer türlerine dayalı olmadığını belirlemek, statik tip denetimi olarak bilinir. Typescript böyle bir yapı sunar.

Typescript nesne yönelimli bir programlama dili yapısını takip eder ve interface, inheritance, class gibi özellikleri destekler. Typescript'te veri tipleri (numbers, string ve boolean) aracılığıyla statik yapı oluşturmak mümkündür. Bu, büyük projeler için kodlamanın daha verimli bir yolu olan debug daha iyi hale getirir.

Geliştiriciler tarafından oluşturulan uygulamalarda birçok doğrulama ve kontrol işlemleri mevcuttur, kullanıcılardan veri alırken veri tiplerini en başta belirlemek önemlidir. Javascript tip denetimi içermediği için typescript devreye girmektedir. Javascript, dinamik olarak yazılan bir dildir, yani yazılım, çalışma zamanına kadar tür farklılıklarını hata olarak kabul etmeyecektir. Bu genellikle birçok hataya neden oldu. Ancak Typescript, isteğe bağlı statik yapı sunduğu için, bir değişken türünü değiştirmez ve yalnızca belirli değerleri alabilir. Derleyici, erken hata tespiti ile sonuçlanan türle ilgili herhangi bir hata konusunda geliştiricileri uyarır.
Ayrıca Typescript, tüm javascript kodunu çalıştırabilir ve tüm kitaplıklarını destekler; bu nedenle javascript'in üst kümesi olarak adlandırılır.
 
###### Toparlamak gerekirse, 

-Typescript ve javascript'e baktığımızda pek çok benzerlik var. Her ikisi de etkileşimli web sayfaları oluşturmak için kullanılır.

-TypeScript, Nesne yönelimli bir programlama dili olarak bilinirken, javascript bir betik dilidir.

-TypeScript, derleme hatalarını her zaman yalnızca geliştirme sırasında gösterir. Bu nedenle çalışma zamanında hata alma şansı çok daha azdır, oysa javascript yorumlanmış bir dildir.

-Javascript doğrudan tarayıcıda çalıştırılır, bu nedenle küçük kod parçaları için kodu yenilemek ve hatalarını ayıklamak daha kolaydır. TypeScript durumunda, kodu çalıştırmak için uygun bir IDE'ye ve kurulumuna ihtiyacımız var.

-Typescript statik tür tanımları için uygun derleme kurulumu (npm paketi) gereklidir, javascript için buna ihtiyaç yoktur.

-Typescript, tıpkı java gibi sınıflar, nesneler ve arayüzler gibi özelliklerle tamamen nesne yönelimlidir. Önceden javascript değişkenleri ve nesneleri için veri türlerinden bahsetmemize gerek yoktu, bu da genel mantığın anlaşılmasını zorlaştırıyor çünkü ne tür verilerle uğraştığımızı bilmiyorduk. Typescript bu sorunu giderir ve geliştiricilere değişkenler ve nesneler için veri türlerini belirtmenin bir yolunu sunar.

