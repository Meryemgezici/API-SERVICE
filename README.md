# API-SERVICE 
## Proje ve Kodun Açıklaması 
Öncelikle API servisi URL’i: https://seffaflik.epias.com.tr/transparency/service/market/intra-day-trade-history?endDate=2022-01-26&startDate=2022-01-26 bu url'yi kullanarak endDate ve startDate parametrelerine içinde bulunduğum gün  2022 01 26 formatında 
değiştirdim.Daha sonra get kullanarak verileri sunucudan çektim.


•API’den gelen veriyi csv formatına çevirdim.

•Projeyi iki şekilde çözdüm 1.çözüm conract değerlerine göre gruplandım ve ortalamasını aldım.Daha sonra bu grupladığım
conract değerlerinin sadece PH ile başlayanlar için price ve quantity değerlerini kullanarak, her bir conract için
Toplam İşlem Miktarı , Toplam İşlem Tutarı ve Ağırlıklı Ortalama Fiyat değerlerini elde ettim.2.çözümde ise onract değerlerine göre gruplamadan aynı işlemleri yaptım.

Toplam İşlem Tutarı = İlgili conract’a ait sınıfların ( price*quantity)/10 değerlerinin toplamı;

Toplam İşlem Miktarı = İlgili conract’a ait sınıfların quantity/10 değerlerinin toplamı;

Ağırlıklı Ortalama Fiyat Toplam İşlem Tutarı/Toplam İşlem Miktarı formülü ile hesaplanacaktır.



• Her bir conract değeri, PH YYAAGGSS formatındadır.Conract değerinde PH ’dan sonra gelen 2
karakterler sırasıyla yıl,ay,gün ve saati temsil ediyor.Gruplama yaptığım conract için, bu tarih
bilgisini conract değerinin içinden uygun DateTime formatına parse ettim.
