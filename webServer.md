

# Node.js ile nasıl Web Server oluştururuz?

Node.js, Javascript kullanarak back-end tarafında uygulamalar yazabileceğiniz bir Javascript runtime platformudur. Bugün Node.js nasıl web server oluşturabilirizin yanıtına bakacağız. 

Bir web sayfasını ziyaret ettiğinizde, internete bağlı başka bir bilgisayara istekte bulunmuş olursunuz ve o da size görüntülemek istedğiniz web sayfasını yanıt olarak gösterir. İstek gönderdiğiniz o bilgisayar web sunucusudur. Node.js ile web server iki farklı şekilde oluşturulabilir. Birincisi core modül olan yani node.js içerisinde yer alan HTTP yöntemi, ikincisi ise node.js için web server oluşturmayı kolaylaştıran bir framework olan Express.

## HTTP ile web server oluşturma:

Öncelikle bilgisayarımızda node.js kurulu olduğundan emin oluyoruz. Daha sona .js uzantılı bir dosya oluşturup http metodunu tanıtıyoruz.

` const http = require(‘http’);`

Sonraki adım olarak createServer metodu ile server oluşturmak için gerekli olan request ve response parametrelerini içeren bir callback fonksiyonu oluşturmalıyız.

 `const server = http.createServer(function (request, response) { });`

 Şimdi de sunucunun port tanımlamasını listen metodu kullanarak oluşturalım. Burada yin callback fonksiyonu kullanıyoruz ve İlk değişkeni port değişkeni olarak veriyoruz.

  `const port = 3000;
  server.listen(port, () => {
  console.log(Sunucu port ${port} de başlatıldı.);
}); `

Bu aşamada terminal kullanarak console.log’da yazdırdıklarımız görebiliriz.

` node dosyaAdi `

Ancak http://localhost:3000/ adresine isteği gönderdik ancak dönecek yanıta dair hiçbir şey belirtmedik. Şimdi yanıtı oluşturalım. Bu noktada dikkat edilmesi gereken gönderilen yanıtı sonlandıran res.end(); metodunu yazmayı unutmamak.

`const server = http.createServer((req, res)=> {
  console.log('Bir istek gönderildi.');
  res.write('MERHABA'); 
  res.end();
  });`

Artık http://localhost:3000 adresine gidip baktığımızda MERHABA yazısını görmüş olacağız.

Sonuç olarak HTTP ile server oluştururken;

require ile HTTP tanımlası yaparız.
createServer metodunu kullanarak istek ve yanıt döngüsünü tamamlar.
listen metodu ile port’u belirtip server oluşturmuş oluruz.

```
    const http = require(‘http’);
  
    const server = http.createServer((req, res)=> {
    
    console.log('Bir istek gönderildi.');
    res.write('MERHABA'); 
    res.end();
    
    });

    const port = 3000;

    server.listen(port, () => {
   
    console.log(Sunucu port ${port} de başlatıldı.);
   
   }); 
```

## Express ile web server oluşturma:

Express server oluştururken öncelikle packet.json oluşturup ardından npm’den express paketini indirmeliyiz.

 npm init
 npm i express

İndirmeler tamamlandıktan sonra index.js dosyası oluşturup express paketini tanıtalım ve express fonksiyonunu app değişkenine atıyoruz. Daha sonra get request oluşturarak http://localhost:3000 adresinde “Hello Word” yazısını görebiliyor oluyoruz. 

  ```const express = require('express')
     const app = express();

     app.get('/', (req, res) => {
     res.send('Hello World!');
      });

     const port = 3000;

    server.listen(port, () => {
    console.log(Sunucu port ${port} de başlatıldı.);
    });
