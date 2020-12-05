---
layout: post
title: Perspektif D�n�s�m�
slug: perspective-transform
author: Bahri ABACI
categories:
- Lineer Cebir
- N�merik Y�ntemler
thumbnail: /assets/post_resources/perspective_transform/thumbnail.png
---

Perspektif nesnenin bulundugu konuma bagli olarak, g�zlemcinin g�z�nde biraktigi etkiyi (g�r�nt�y�) 2 boyutlu bir d�zlemde canlandirmak i�in gelistirilmis bir iz d�s�m teknigidir. R�nesans d�neminde�Masaccio' nun resimlerinde kullanmaya basladigi teknik g�n�m�zde ger�ek�i �izimler olusturmak i�in olmazsa olmazlardandir. Ancak olayi g�r�nt� isleme a�isindan ele aldigimizda **perspektif** genellikle islerimizi zorlastiran bir etkiye sahiptir. Ama� nesne tanima veya siniflandirma oldugunda nesnenin hangi a�idan g�r�nt�lendiginin bir �nemi olmamalidir.  

<!--more-->
  
�rnegin standart bir karakter tanima uygulamasina g�r�nt� olarak verilen "*cescript*, "_cescript_" veya ?di??s?? g�r�nt�leri ayni kelime olmalarina ragmen bilgisayar tarafindan her seferinde farkli olarak okunacaktir. Iste **perspektif** d�n�s�m� bu noktada devreye girerek verilen g�r�nt� �zerindeki �l�ekleme, yayma, d�nme ve kayma gibi etkileri kaldirabilmemizi saglar. 

Perspektif d�zeltmede ama� kisinin veya nesnenin konum degistirmesi sonucu olusacak etkiyi betimleyebilmektir. Bu islem sayesinde g�r�nt� olustuktan sonra dahi belirli kisitlar i�erisinde resme baktigimiz a�iyi degistirebiliriz. Algoritma karakter tanima uygulamalrinda (Cam Scanner gibi) �ekilmis bir g�r�nt�y� belirli kaliplar i�erisine oturmada, plaka tanima, y�z tanima gibi uygulamalarda normalizasyon sirasinda siklikla kullanilmaktadir.  

Asagida verilen matriste <img src="assets/post_resources/math//332cc365a4987aacce0ead01b8bdcc0b.svg?invert_in_darkmode" align=middle width=9.39498779999999pt height=14.15524440000002pt/>,<img src="assets/post_resources/math//deceeaf6940a8c7a5a02373728002b0f.svg?invert_in_darkmode" align=middle width=8.649225749999989pt height=14.15524440000002pt/> herhangi bir koordinat degeri olmak �zere, <img src="assets/post_resources/math//aca94dc4280088e4b15ee4be41751fd0.svg?invert_in_darkmode" align=middle width=13.18495034999999pt height=24.7161288pt/> ve <img src="assets/post_resources/math//15f93b25ba881e5829e8fc647b680fb2.svg?invert_in_darkmode" align=middle width=12.43916849999999pt height=24.7161288pt/> bu iki degerin d�n�s�m sonrasi degerlerini g�stermektedir. Matris g�sterimindeki a degerlerinin her birinin �zel bir anlami vardir.�

<p align="center"><img src="assets/post_resources/math//116b0389e27dac5fc484a7354ab5c839.svg?invert_in_darkmode" align=middle width=203.7274866pt height=59.1786591pt/></p>

Simdi basitlik olmasi i�in bazi <img src="assets/post_resources/math//44bc9d542a92714cac84e01cbbb7fd61.svg?invert_in_darkmode" align=middle width=8.68915409999999pt height=14.15524440000002pt/> degerlerini <img src="assets/post_resources/math//29632a9bf827ce0200454dd32fc3be82.svg?invert_in_darkmode" align=middle width=8.219209349999991pt height=21.18721440000001pt/> kabul ederek elde edecegimiz <img src="assets/post_resources/math//aca94dc4280088e4b15ee4be41751fd0.svg?invert_in_darkmode" align=middle width=13.18495034999999pt height=24.7161288pt/> ve <img src="assets/post_resources/math//15f93b25ba881e5829e8fc647b680fb2.svg?invert_in_darkmode" align=middle width=12.43916849999999pt height=24.7161288pt/> degerlerini yorumlamaya �alisalim. Anlasilmasi en kolay durum ile incelememize baslayabiliriz: <img src="assets/post_resources/math//877ec8605e9a149fbdbacdc3b261d611.svg?invert_in_darkmode" align=middle width=275.4219286499999pt height=21.18721440000001pt/> ve <img src="assets/post_resources/math//f7f346faafc0b450ee416bf944606c99.svg?invert_in_darkmode" align=middle width=141.82056899999998pt height=21.18721440000001pt/>. Bu durumda <img src="assets/post_resources/math//1827f0f9f6d999034c150ef680d47bda.svg?invert_in_darkmode" align=middle width=45.31948079999999pt height=24.7161288pt/> ve�<img src="assets/post_resources/math//3ed059a1da67c3d11a55c21ce4e73e0a.svg?invert_in_darkmode" align=middle width=43.82793689999998pt height=24.7161288pt/>�olacaktir. Yani yeni olusan g�r�nt�deki her bir nokta oldugu yerde kalacaktir. (Aynalama)

### �teleme

Diger basit bir durum ise <img src="assets/post_resources/math//837fe56d8e6abdc9484475eac2b44b30.svg?invert_in_darkmode" align=middle width=186.3543561pt height=21.18721440000001pt/> ve <img src="assets/post_resources/math//f7f346faafc0b450ee416bf944606c99.svg?invert_in_darkmode" align=middle width=141.82056899999998pt height=21.18721440000001pt/> durumudur. Bu durumda yeni koordinat degerleri <img src="assets/post_resources/math//636a506e70fd2a3cd0324c972e312385.svg?invert_in_darkmode" align=middle width=85.71335685pt height=24.7161288pt/>, <img src="assets/post_resources/math//ee70a03ce2c3b49a55f025394ed2c96a.svg?invert_in_darkmode" align=middle width=87.20492054999998pt height=24.7161288pt/>�seklinde olacaktir. Yani yeni g�r�nt�deki herbir nokta�<img src="assets/post_resources/math//281037dda0073f9e3c169b6c53660212.svg?invert_in_darkmode" align=middle width=21.79424774999999pt height=14.15524440000002pt/>�kadar saga ve�<img src="assets/post_resources/math//01dde2af628b8534c6f880cfe04b740e.svg?invert_in_darkmode" align=middle width=21.79424774999999pt height=14.15524440000002pt/>�kadar asagiya kayacaktir.

### �l�ekleme

�l�ekleme islemi i�in�<img src="assets/post_resources/math//877ec8605e9a149fbdbacdc3b261d611.svg?invert_in_darkmode" align=middle width=275.4219286499999pt height=21.18721440000001pt/> ve <img src="assets/post_resources/math//8be983d78dbd26828f448d4c5b8d88b0.svg?invert_in_darkmode" align=middle width=52.75297334999999pt height=21.18721440000001pt/>�se�ilerek su durum elde edilir: <img src="assets/post_resources/math//a3845b0912c8bdbfd7ca6384a5d70f07.svg?invert_in_darkmode" align=middle width=66.44409255pt height=24.7161288pt/>�, <img src="assets/post_resources/math//a623d8df97c4f071a4877e711cf9b970.svg?invert_in_darkmode" align=middle width=67.93563809999998pt height=24.7161288pt/>. Ifadenin daha anlasilir olmasi i�in �<img src="assets/post_resources/math//21de9ef1ca1aa691456f97af1e78aa35.svg?invert_in_darkmode" align=middle width=112.81187444999998pt height=21.18721440000001pt/>�se�elim, bu durumda yeni olusan resimde <img src="assets/post_resources/math//deceeaf6940a8c7a5a02373728002b0f.svg?invert_in_darkmode" align=middle width=8.649225749999989pt height=14.15524440000002pt/> degerleri degismezken, <img src="assets/post_resources/math//50ef356199ecf9cd0b56dc55b19928ac.svg?invert_in_darkmode" align=middle width=47.75103794999999pt height=21.18721440000001pt/> daki bir nokta <img src="assets/post_resources/math//0965b5f2cc5612aacb2f4815ba3d0641.svg?invert_in_darkmode" align=middle width=52.362911699999984pt height=24.7161288pt/> ye, <img src="assets/post_resources/math//5083878ed0e20f1f455265a986774344.svg?invert_in_darkmode" align=middle width=47.75103794999999pt height=21.18721440000001pt/> deki bir nokta <img src="assets/post_resources/math//f31018f6e4a982602fe024fc08657e03.svg?invert_in_darkmode" align=middle width=52.362911699999984pt height=24.7161288pt/> a ... seklinde her bir <img src="assets/post_resources/math//332cc365a4987aacce0ead01b8bdcc0b.svg?invert_in_darkmode" align=middle width=9.39498779999999pt height=14.15524440000002pt/> noktasi <img src="assets/post_resources/math//76c5792347bb90ef71cfbace628572cf.svg?invert_in_darkmode" align=middle width=8.219209349999991pt height=21.18721440000001pt/> katina gitmekte yani resim <img src="assets/post_resources/math//332cc365a4987aacce0ead01b8bdcc0b.svg?invert_in_darkmode" align=middle width=9.39498779999999pt height=14.15524440000002pt/> ekseninde iki kat �l�eklenmektedir.

### D�nd�rme

D�nd�rme islemi <img src="assets/post_resources/math//0371512dc45143d9e1c404a9aac28c5d.svg?invert_in_darkmode" align=middle width=111.56036429999999pt height=14.15524440000002pt/> degerlerinin �zel sekilde se�ilmesi ile yapilir. Bu se�im d�nd�rme a�isi <img src="assets/post_resources/math//27e556cf3caa0673ac49a8f0de3c73ca.svg?invert_in_darkmode" align=middle width=8.17352744999999pt height=22.831056599999986pt/> ya bagli olarak su sekilde ifade edilir: <img src="assets/post_resources/math//5a523ed0c3d8e2c4b00176ae12f47df2.svg?invert_in_darkmode" align=middle width=87.50189909999999pt height=24.65753399999998pt/> , <img src="assets/post_resources/math//237860db13346345ca138e2429b175f9.svg?invert_in_darkmode" align=middle width=101.20052745pt height=24.65753399999998pt/> , <img src="assets/post_resources/math//9f810af2d4a309a5d1eb28febdb6bb04.svg?invert_in_darkmode" align=middle width=85.67543489999998pt height=24.65753399999998pt/> , <img src="assets/post_resources/math//c83b52cf6bfc1c913511251b353a937e.svg?invert_in_darkmode" align=middle width=87.50189909999999pt height=24.65753399999998pt/>. Inceleme yapabilmemiz i�in yine basit olarak <img src="assets/post_resources/math//27e556cf3caa0673ac49a8f0de3c73ca.svg?invert_in_darkmode" align=middle width=8.17352744999999pt height=22.831056599999986pt/> degerini <img src="assets/post_resources/math//1c6512d0c8f909ef59643cb9bd8021b0.svg?invert_in_darkmode" align=middle width=24.657628049999992pt height=21.18721440000001pt/>, <img src="assets/post_resources/math//741a37c7e2b478fa19d0be5c818d9e93.svg?invert_in_darkmode" align=middle width=142.519113pt height=21.18721440000001pt/> ve <img src="assets/post_resources/math//1b0c414c468e7279b488dfd65f7c7182.svg?invert_in_darkmode" align=middle width=52.75299644999999pt height=21.18721440000001pt/> se�elim. <img src="assets/post_resources/math//acf1b8bbd82c00c81f1359cf90d0fc36.svg?invert_in_darkmode" align=middle width=102.37448759999998pt height=24.65753399999998pt/> ve <img src="assets/post_resources/math//952f0b0644ff0f5a1911ba5470b97bd9.svg?invert_in_darkmode" align=middle width=87.76258919999998pt height=24.65753399999998pt/> oldugu g�z �n�nde bulundurularak d�n�s�m sonrasi degerlerimiz <img src="assets/post_resources/math//0a4d1394e21415da1bc92260cbff13be.svg?invert_in_darkmode" align=middle width=58.104914999999984pt height=24.7161288pt/>, <img src="assets/post_resources/math//c2439bda9ce0de50c3898d8420b14bb5.svg?invert_in_darkmode" align=middle width=56.61337109999999pt height=24.7161288pt/> seklinde olacaktir. Yani yeni g�r�nt�de <img src="assets/post_resources/math//deceeaf6940a8c7a5a02373728002b0f.svg?invert_in_darkmode" align=middle width=8.649225749999989pt height=14.15524440000002pt/> noktalari <img src="assets/post_resources/math//019f81ae3f4c433d4f5bbc5ff002d38e.svg?invert_in_darkmode" align=middle width=21.43465829999999pt height=19.1781018pt/>, <img src="assets/post_resources/math//332cc365a4987aacce0ead01b8bdcc0b.svg?invert_in_darkmode" align=middle width=9.39498779999999pt height=14.15524440000002pt/> noktasi <img src="assets/post_resources/math//4eb1b9787b23954d9a6d0a46d13c6971.svg?invert_in_darkmode" align=middle width=22.180421999999993pt height=19.1781018pt/> noktasina tasinacak ve g�r�nt� orijine g�re simetrisi alinmis yani <img src="assets/post_resources/math//1c6512d0c8f909ef59643cb9bd8021b0.svg?invert_in_darkmode" align=middle width=24.657628049999992pt height=21.18721440000001pt/> derece d�nd�r�lm�s olacaktir.

Daha karmasik durumlar i�in ilk olarak <img src="assets/post_resources/math//630884b7e089613e3e7476288a35a259.svg?invert_in_darkmode" align=middle width=51.71628659999998pt height=14.15524440000002pt/> degerlerinin sifirdan farkli oldugu durumlar incelenebilir. Bu durumda <img src="assets/post_resources/math//aca94dc4280088e4b15ee4be41751fd0.svg?invert_in_darkmode" align=middle width=13.18495034999999pt height=24.7161288pt/> degerinde <img src="assets/post_resources/math//deceeaf6940a8c7a5a02373728002b0f.svg?invert_in_darkmode" align=middle width=8.649225749999989pt height=14.15524440000002pt/>, <img src="assets/post_resources/math//15f93b25ba881e5829e8fc647b680fb2.svg?invert_in_darkmode" align=middle width=12.43916849999999pt height=24.7161288pt/> degerinde ise <img src="assets/post_resources/math//332cc365a4987aacce0ead01b8bdcc0b.svg?invert_in_darkmode" align=middle width=9.39498779999999pt height=14.15524440000002pt/> ekseninin etkisi g�r�necektir. Daha karmasik bir durum ise **perspektif d�zeltmenin** temeli olan <img src="assets/post_resources/math//1713634c9489d71cc69f9e9e20ddecf3.svg?invert_in_darkmode" align=middle width=51.71628659999998pt height=14.15524440000002pt/> degerlerini sifirdan farkli se�mektir. Bu durum g�r�nt�deki uzaklik etkisini <img src="assets/post_resources/math//aca94dc4280088e4b15ee4be41751fd0.svg?invert_in_darkmode" align=middle width=13.18495034999999pt height=24.7161288pt/> ve <img src="assets/post_resources/math//15f93b25ba881e5829e8fc647b680fb2.svg?invert_in_darkmode" align=middle width=12.43916849999999pt height=24.7161288pt/> degerlerine yayarak g�zde �� boyut etkisini yaratan b�k�m� d�zeltmeyi saglar.

Bu yazimda basit �rneklerle baslik halinde de verdigim �� d�n�s�m� (�teleme-�l�ekleme-D�nd�rme) �rneklerle incelemeye �alisacagim. D�n�s�m i�in yazilan kodu inceleyerek baslayalim.  
  
```c
//a11 = T[0]; a12 = T[3]; a13 = T[6];
//a21 = T[1]; a22 = T[4]; a23 = T[7]; 
//a31 = T[2]; a32 = T[5]; a33 = T[8];

//x' = (x*a11 + y*a12 + a13) / z';
//y' = (x*a21 + y*a22 + a23) / z';
//z' = (x*a31 + y*a32 + a33);

uint8_t *in_data  = data(uint8_t, in);
uint8_t *out_data = data(uint8_t, out);

// Affine
float *a = data(float, T);

int d, w, h;
for(h=0; h < height(out); h++) 
{
    for(w=0; w < width(out); w++) 
    {
        double zp = w*a[6] + h*a[7] + a[8];

        // if the z zero, continue
        if(equal(zp, 0, 0.00001)) { continue; }

        int x = (w*a[0] + h*a[1] + a[2]) / zp;
        int y = (w*a[3] + h*a[4] + a[5]) / zp;

        // check whether the x,y is outside the image
        if( (x < 0) || (y < 0) || (x > width(out)-1) || (y > height(out)-1) ) { continue; }

        for(d=0; d < channels(in); d++)
        {
            out_data[channels(out)*(x+y*width(out)) + d] = in_data[ channels(in)*(w+width(in)*h) + d];
        }
    }
}
```

**Peki bu kadar mi?**

Degil tabi ki :) Su ana kadar okudugunuz yazi i�erisinde dikkatinizi bir noktanin �zellikle �ekmesini istemistim. �l�ekleme kisminda verdigim �rnekte katsayinin iki se�ilmesi durumunda resimdeki her bir noktanin iki katina gittigini s�ylemistim. Ayni �rnekte durumu yeni olusan resim a�isindan ele alirsak, <img src="assets/post_resources/math//a8cfa0bfd812d6072a0650f07da67403.svg?invert_in_darkmode" align=middle width=112.85341319999999pt height=21.18721440000001pt/> gibi noktalar hi�bir <img src="assets/post_resources/math//0acac2a2d5d05a8394e21a70a71041b4.svg?invert_in_darkmode" align=middle width=25.350096749999988pt height=14.15524440000002pt/> �ifti i�in bir degere sahip olamayacaktir. Bu y�zden olusan resimde siyah noktalar (bu �rnek i�in yatay �izgiler) olusacaktir. Bunu engellemek i�in s�yle bir y�ntem izleyebiliriz.�

<p align="center"><img src="assets/post_resources/math//da6647763ec18b2638106fc05da1b052.svg?invert_in_darkmode" align=middle width=220.717167pt height=59.1786591pt/></p>
  
Y�ntem ilk kisimda anlatilan y�ntem ile ayni g�r�nmesine karsilik, bu sefer �ikti g�r�nt�s� �zerindeki bir noktanin <img src="assets/post_resources/math//bf4645e786baf289adfe68fe608d3e69.svg?invert_in_darkmode" align=middle width=47.35926029999999pt height=24.7161288pt/> girdi g�r�nt�s� �zerinde nereden geldigini aradigimizdan <img src="assets/post_resources/math//7392a8cd69b275fa1798ef94c839d2e0.svg?invert_in_darkmode" align=middle width=38.135511149999985pt height=24.65753399999998pt/> �ikti g�r�nt�s� �zerinde hi� bir bos nokta kalmayacaktir. Kod �zerinde yapacagimiz en �nemli degisim a katsayilari yerine ia katsayilarini bulma kisminda olacaktir. Matrissel sekilde g�sterilen <img src="assets/post_resources/math//6e6ef46c567f70e3c5145d9b202f6f77.svg?invert_in_darkmode" align=middle width=14.352379799999989pt height=21.68300969999999pt/> katsayilari <img src="assets/post_resources/math//44bc9d542a92714cac84e01cbbb7fd61.svg?invert_in_darkmode" align=middle width=8.68915409999999pt height=14.15524440000002pt/> katsayilarindan olusan matrisin tersine ait elemanlardir. Matris tersi bulma islemini baska bir yazimda anlatmayi planladigimdan bu kismi ge�erek yeni y�nteme ait kodlari paylasiyorum.  
  
```c
//ia11 = T[0]; a12 = T[3]; a13 = T[6];
//ia21 = T[1]; a22 = T[4]; a23 = T[7]; 
//ia31 = T[2]; a32 = T[5]; a33 = T[8];

//x' = (x*ia11 + y*ia12 + ia13) / z';
//y' = (x*ia21 + y*ia22 + ia23) / z';
//z' = (x*ia31 + y*ia32 + ia33);

uint8_t *in_data  = data(uint8_t, in);
uint8_t *out_data = data(uint8_t, out);

// Affine
float *ia = data(float, iT);

int shidx, d, w, h;
for(h=0; h < height(out); h++)
{
    shidx = h*width(out);

    for(w=0; w < width(out); w++)
    {
        double zp = w*ia[6] + h*ia[7] + ia[8];

        // if the z zero, continue
        if(equal(zp, 0, 0.00001)) { continue; }

        int x = (w*ia[0] + h*ia[1] + ia[2]) / zp;
        int y = (w*ia[3] + h*ia[4] + ia[5]) / zp;

        // check whether the x,y is outside the image
        if( (x < 0) || (y < 0) || (x > width(in)-1) || (y > height(in)-1) ) { continue; }

        for(d=0; d < channels(in); d++)
        {
            out_data[channels(out)*(w+shidx) + d] = in_data[ channels(in)*(x+width(in)*y) + d];
        }
    }
}
```
  
Dikkat edilecek olursa kodlamadaki tek degisimin T matrisi yerine iT olmadigi g�r�l�r. Bahsettigim �zere bu degisim sonrasinda for d�ng�lerimizi �ikis g�r�nt�s� �zerindeki koordinatlarda d�nd�recegimizden `x` ve `y` (yani x' ve y') degerleri giris g�r�nt�s�nde yerine yazilacaktir. Artik basitten karmasiga dogru �rneklerimize ge�ebiliriz.

|Orjinal Imge| 45� D�nd�rme | 90� D�nd�rme | 45� D�nd�rme ve Yariya �l�ekleme|
|:----------:|:-----------------:|:----------------------:|:-----------:|
![affine d�n�s�m� �rnek][affine] | ![affine d�n�s�m� �rnek][affine1] | ![affine d�n�s�m� �rnek][affine2] | ![affine d�n�s�m� �rnek][affine3]
| `rot2tform(128, 128, 0, 1.0)` | `rot2tform(128, 128, 45, 1.0)` | `rot2tform(128, 128, 90, 1.0)` | `rot2tform(128, 128, 45, 0.5)` |
| <p align="center"><img src="assets/post_resources/math//2a9b9a3e0bf8f86a368b63a6e6fe1f61.svg?invert_in_darkmode" align=middle width=151.61542275pt height=59.1786591pt/></p> | <p align="center"><img src="assets/post_resources/math//9b363e3f712e370e1fe32aff788f7663.svg?invert_in_darkmode" align=middle width=185.4054807pt height=59.1786591pt/></p> | <p align="center"><img src="assets/post_resources/math//2524147ff89f40dcb2c3f0ae5187f996.svg?invert_in_darkmode" align=middle width=180.83925584999997pt height=59.1786591pt/></p> | <p align="center"><img src="assets/post_resources/math//93ced4bcedd036bb3f583e00634daca6.svg?invert_in_darkmode" align=middle width=193.62468345pt height=59.1786591pt/></p> |

Yukarida farkli d�n�s�m parametreleri i�in elde edilen sonu�lar verilmistir. Sonu�lar �retilirken imlab k�t�phanesinde yer alan ve bir merkez noktasi etrafinda d�nme ve �l�ekleme yapabilmek i�in gereken d�n�s�m matrisini hesaplayan `rot2tform` fonksiyonu kullanilmistir. Bu fonksiyonun �rettigi d�n�s�m matrisleri de tabloda ilgili s�tunlarin altinda verilmistir. 

Son s�z olarak perspektif d�zeltmedeki katsayilarin otomatik bulunmasindan bahsedebiliriz. Bu yaziyi yazmamdaki esas neden **sudoku ��z�c�** i�in gerekli olan perspektif d�zeltmesinin nasil yapilacagini anlatmakti. [Bir �nceki yazimi]({% post_url 2013-12-02-sudoku-cozucu-uygulamasi %}) okuduysaniz, sudoku karesinin karsidan �ekilmedigi durumlarda ne olacagini merak etmis olabilirsiniz. B�yle bir durumla karsilasmamiz durumunda gerekli d�n�s�m katsayilarini otomatik olarak belirleyerek d�n�s�m yapmamiz gerekecektir.

## Perspektif D�n�s�m Katsayilarinin Elde Edilmesi

Parametrelerin otomatik olarak �ikarilmasi i�in bir ka� matris b�lmesi islemi gerekmektedir. B�ylece girdi olarak verilen bir g�r�nt� otomatik olarak kolaylikla hizalanabilmektedir.
Perspektif d�n�s�m�n�n bir matris �arpmasi ile yapildigini biliyoruz. D�n�s�m i�in kullandigimiz matrisi islemlerimiz i�in tekrar yazalim.

<p align="center"><img src="assets/post_resources/math//116b0389e27dac5fc484a7354ab5c839.svg?invert_in_darkmode" align=middle width=203.7274866pt height=59.1786591pt/></p>
  
Burada <img src="assets/post_resources/math//bf4645e786baf289adfe68fe608d3e69.svg?invert_in_darkmode" align=middle width=47.35926029999999pt height=24.7161288pt/> �iftlerinin <img src="assets/post_resources/math//7392a8cd69b275fa1798ef94c839d2e0.svg?invert_in_darkmode" align=middle width=38.135511149999985pt height=24.65753399999998pt/> �iftlerinin <img src="assets/post_resources/math//44bc9d542a92714cac84e01cbbb7fd61.svg?invert_in_darkmode" align=middle width=8.68915409999999pt height=14.15524440000002pt/> matrisi ile d�n�s�m sonrasi aldigi degerler oldugunu hatirlayalim. Amacimizin <img src="assets/post_resources/math//44bc9d542a92714cac84e01cbbb7fd61.svg?invert_in_darkmode" align=middle width=8.68915409999999pt height=14.15524440000002pt/> matrisini bulmak oldugunu tekrarlayarak islemlerimize baslayalim. Ilk olarak <img src="assets/post_resources/math//f93ce33e511096ed626b4719d50f17d2.svg?invert_in_darkmode" align=middle width=8.367621899999993pt height=14.15524440000002pt/> degerini <img src="assets/post_resources/math//d317dab3abbc6f671f1dcf553201e79f.svg?invert_in_darkmode" align=middle width=155.5383852pt height=19.1781018pt/> seklinde yazarak <img src="assets/post_resources/math//aca94dc4280088e4b15ee4be41751fd0.svg?invert_in_darkmode" align=middle width=13.18495034999999pt height=24.7161288pt/> ve <img src="assets/post_resources/math//15f93b25ba881e5829e8fc647b680fb2.svg?invert_in_darkmode" align=middle width=12.43916849999999pt height=24.7161288pt/> degerlerini a�ik sekilde yazmaya �alisalim.
  
<p align="center"><img src="assets/post_resources/math//9d20e6dd67c8a88cacd84a18fd4a4ec8.svg?invert_in_darkmode" align=middle width=336.47675655pt height=35.18196pt/></p>  
  
Simdi i�ler dislar �arpimi yaparak ifadeleri d�zenleyelim ve kolaylik olmasi adina <img src="assets/post_resources/math//cc66eabb96b1e6f09498d2c025cb6695.svg?invert_in_darkmode" align=middle width=52.75299644999999pt height=21.18721440000001pt/> alalim.  
  
<p align="center"><img src="assets/post_resources/math//7c92b263b1d338aed5fce8595d30cd8a.svg?invert_in_darkmode" align=middle width=292.6502436pt height=16.3763325pt/></p>ve <p align="center"><img src="assets/post_resources/math//e0e071a36631e2ecb5e37a6d7b7892c1.svg?invert_in_darkmode" align=middle width=290.41289804999997pt height=16.3763325pt/></p>  
  
Elde edilen ifadeyi solda <img src="assets/post_resources/math//79f484e408f95e8839929c2fffd02c82.svg?invert_in_darkmode" align=middle width=33.75191489999999pt height=24.7161288pt/>; sagda ise <img src="assets/post_resources/math//4fc63d27626433f23e36eca761bac52b.svg?invert_in_darkmode" align=middle width=12.47911664999999pt height=24.7161288pt/> l� terimler olacak sekilde d�zenlersek;  
  
<p align="center"><img src="assets/post_resources/math//a4a3f574882037f412428ee7cc3dbc87.svg?invert_in_darkmode" align=middle width=292.65023864999995pt height=16.3763325pt/></p>ve <p align="center"><img src="assets/post_resources/math//b8dabdd68d6928576e932108df8434c2.svg?invert_in_darkmode" align=middle width=290.41289474999996pt height=16.3763325pt/></p> 

elde edilir.  
  
Bu denklemleri matris formunda yazacak olursak (<img src="assets/post_resources/math//cbd1c0e87d9e8e261f4d30611b8664cf.svg?invert_in_darkmode" align=middle width=76.32017744999999pt height=22.465723500000017pt/>);  
  
<p align="center"><img src="assets/post_resources/math//80807870c5879d6e8a1f8188711bd6b4.svg?invert_in_darkmode" align=middle width=361.69162754999996pt height=177.5360268pt/></p> 

ifadesi elde edilir. Burada aranilan <img src="assets/post_resources/math//44bc9d542a92714cac84e01cbbb7fd61.svg?invert_in_darkmode" align=middle width=8.68915409999999pt height=14.15524440000002pt/> vekt�r� <img src="assets/post_resources/math//1f3fcdc4a9ba8727f5488470e53257f1.svg?invert_in_darkmode" align=middle width=141.50867445pt height=26.76175259999998pt/> matris b�lme islemi ile kolaylikla bulunabilir. Burada dikkat edilmesi gereken bir nokta elimizde sekiz bilinmeyen (<img src="assets/post_resources/math//44bc9d542a92714cac84e01cbbb7fd61.svg?invert_in_darkmode" align=middle width=8.68915409999999pt height=14.15524440000002pt/> vekt�r�n�n elemanlari) olamasina ragmen g�r�n�rde sadece iki denklemimiz olmasidir. Sekiz bilinmeyenli bir denklemin tek ��z�m�n�n olmasi i�in bagimsiz sekiz denklem gerektiginden bizimde �alismada tek bir <img src="assets/post_resources/math//7392a8cd69b275fa1798ef94c839d2e0.svg?invert_in_darkmode" align=middle width=38.135511149999985pt height=24.65753399999998pt/> noktasi yerine d�rt tane <img src="assets/post_resources/math//7392a8cd69b275fa1798ef94c839d2e0.svg?invert_in_darkmode" align=middle width=38.135511149999985pt height=24.65753399999998pt/> noktasi �zerinden d�n�s�m yapilarak <img src="assets/post_resources/math//44bc9d542a92714cac84e01cbbb7fd61.svg?invert_in_darkmode" align=middle width=8.68915409999999pt height=14.15524440000002pt/> matrisi bulunmustur.

Simdi gelelim kodlama kismina. Bir �nceki yazida matris tersini bulma kismindan bahsettigim i�in yapmamiz gerek tek islem `A` ve `B` matrislerini hazirlamak.

```c
float dst_data[] = 
{
    dst[0].x, dst[0].y, 1, 0, 0, 0, -src[0].x * dst[0].x, -src[0].x * dst[0].y,
    0, 0, 0, dst[0].x, dst[0].y, 1, -src[0].y * dst[0].x, -src[0].y * dst[0].y,

    dst[1].x, dst[1].y, 1, 0, 0, 0, -src[1].x * dst[1].x, -src[1].x * dst[1].y,
    0, 0, 0, dst[1].x, dst[1].y, 1, -src[1].y * dst[1].x, -src[1].y * dst[1].y,

    dst[2].x, dst[2].y, 1, 0, 0, 0, -src[2].x * dst[2].x, -src[2].x * dst[2].y,
    0, 0, 0, dst[2].x, dst[2].y, 1, -src[2].y * dst[2].x, -src[2].y * dst[2].y,

    dst[3].x, dst[3].y, 1, 0, 0, 0, -src[3].x * dst[3].x, -src[3].x * dst[3].y,
    0, 0, 0, dst[3].x, dst[3].y, 1, -src[3].y * dst[3].x, -src[3].y * dst[3].y,
};

float b_data[] = {src[0].x, src[0].y, src[1].x, src[1].y, src[2].x, src[2].y, src[3].x, src[3].y};

matrix_t *inA = matrix_create(float, 8, 8, 1, dst_data);
matrix_t *inB = matrix_create(float, 8, 1, 1, b_data);
```

Matrislerimizi olusturduktan sonra katsayilari bulmak i�in �nceki yazimizda kullandigimiz�`matris_divide` fonksiyonunu kullanacagiz, ardindan olusan <img src="assets/post_resources/math//005c128d6e551735fa5d938e44e7a613.svg?invert_in_darkmode" align=middle width=8.219209349999991pt height=21.18721440000001pt/> satirlik vekt�r� kullanarak <img src="assets/post_resources/math//46e42d6ebfb1f8b50fe3a47153d01cd2.svg?invert_in_darkmode" align=middle width=36.52961069999999pt height=21.18721440000001pt/> l�k a matrisimizi yeniden olusturacagiz.

```c
matrix_t *inv = matrix_create(float);
matrix_divide(inA, inB, inv);
```

Bu asamada istedigimiz noktalari istedigimiz yeni noktalara d�n�st�recek d�n�s�m�matrisini�elde etmis�bulunuyoruz. Elde edilen bu sonu� imlab k�t�phanesinde yer alan `pts2tform` fonksiyonu ile de ger�eklenebilir.

Bulunan degerler kullanilarak istenilen d�n�s�m�`imrotate` fonksiyonunu ile ger�eklestirilebilir. Her zamanki gibi bir �rnek uygulama ile yazimizi bitirelim. Birka� yazi �nce temelini attigimiz sudoku ��z�c� uygulamamiz i�in bulunan sudoku karesini hizalamaya �alisalim.

```c
// read the test image
matrix_t *test  = imread("../data/sudoku.bmp");
matrix_t *test_aligned = matrix_create(uint8_t, rows(test), cols(test), 3);

// find the key points
struct point_t source[4] = { {.x = 117, .y = 66}, {.x = 464, .y = 70}, {.x = 502, .y = 375}, {.x = 33, .y = 350} };
struct point_t destination[4] = { {.x = 0, .y = 0}, {.x = 511, .y = 0}, {.x = 511, .y = 511}, {.x = 0, .y = 511} };

// correct the image
matrix_t *transform = pts2tform(source, destination, 4);

// print the transform
printf("%5.3f %5.3f %5.3f\n", atf(transform, 0,0), atf(transform, 0,1), atf(transform, 0,2));
printf("%5.3f %5.3f %5.3f\n", atf(transform, 1,0), atf(transform, 1,1), atf(transform, 1,2));
printf("%5.3f %5.3f %5.3f\n", atf(transform, 2,0), atf(transform, 2,1), atf(transform, 2,2));

// do the transform
imtransform(test, transform, test_aligned);

// write the resulting image
imwrite(test_aligned, "../data/test_aligned.bmp");
```
  
Yazilan kod okunan sudoku resminin d�rt k�sesini girdi olarak aldiktan sonra sudoku karesini <img src="assets/post_resources/math//232b7825ad6b94218473890f57549b15.svg?invert_in_darkmode" align=middle width=69.40644809999999pt height=21.18721440000001pt/> lik bir karenin i�erisine hizalayacak d�n�s�m matrisini bulur ve d�n�s�m� ger�eklestirir. Kodumuzun girdi ve �iktilari su sekilde olacaktir.

|Girdi Imgesi|Hizalama I�in Se�ilen Noktalar|Hizalanmis Imge|
|:-------:|:----:|:----:|
![perspektif d�n�s�m� �rnek][sudoku1] | ![perspektif d�n�s�m� �rnek][sudoku2] | ![perspektif d�n�s�m� �rnek][sudoku3]

Baska bir uygulama olarak da rubik k�p �rnegine bakalim. Burada amacimiz verilen rubik k�pe yukaridan baksaydik nasil bir g�r�nt� elde ederdik sorusuna cevap bulmak.

|Girdi Imgesi|Hizalama I�in Se�ilen Noktalar|Hizalanmis Imge|
|:-------:|:----:|:----:|
![perspektif d�n�s�m� �rnek][rubik1] | ![perspektif d�n�s�m� �rnek][rubik2] | ![perspektif d�n�s�m� �rnek][rubik3]

G�r�ld�g� gibi algoritma sadece k�se noktalarini alarak otomatik �rettigi parametreler ile gayet basarili sonu�lar �retmektedir. Bu da bize kamera a�isindan bagimsiz g�r�nt� isleme uygulamalarinda b�y�k bir katki saglamaktadir.

Yazida yer alan analizlerin yapildigi kod par�alari, g�rseller ve kullanilan veri setlerine [perspective_transform](https://github.com/cescript/imlab_perspective_transform) GitHub sayfasi �zerinden erisilebilirsiniz.

**Referanslar**

[RESOURCES]: # (List of the resources used by the blog post)
[affine]: /assets/post_resources/perspective_transform/affine.png
[affine1]: /assets/post_resources/perspective_transform/affine1.png
[affine2]: /assets/post_resources/perspective_transform/affine2.png
[affine3]: /assets/post_resources/perspective_transform/affine3.png

[sudoku1]: /assets/post_resources/perspective_transform/sudoku1.png
[sudoku2]: /assets/post_resources/perspective_transform/sudoku2.png
[sudoku3]: /assets/post_resources/perspective_transform/sudoku3.png

[rubik1]: /assets/post_resources/perspective_transform/rubik1.png
[rubik2]: /assets/post_resources/perspective_transform/rubik2.png
[rubik3]: /assets/post_resources/perspective_transform/rubik3.png
