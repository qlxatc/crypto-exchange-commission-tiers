# En düşük komisyonlu kripto borsası: Maker/taker farkı, VIP kademeleri ve GT indirimiyle işlem maliyetini düşürme rehberi

"En düşük komisyonlu kripto borsası" arayan biri genelde tek bir sayı bekliyor: yüzde kaç? Ne yazık ki iş öyle bitmiyor. Aynı borsada aynı gün iki kişi aynı miktarda Bitcoin alıp farklı komisyon ödeyebiliyor, çünkü ödenen tutarı belirleyen şey ilan edilen orandan çok emrin nasıl gönderildiği ve ödemenin hangi varlıkla yapıldığı oluyor.

Bu yazıda işi iki katmana ayırıyorum: hangi kalemler gerçekten para çıkartıyor, ve Gate.com özelinde VIP kademeleri, GT indirimi ve vadeli işlem tarafı ne durumda. Amaç "şu borsa en ucuz" diye bağırmak değil; hangi profilde hangi kademenin anlamlı olduğunu rakamlarla göstermek.

## Komisyon tek kalem değil: maliyetin beş parçası

Bir alım satımda cebinizden çıkan şeyi şöyle ayırmak gerekiyor:

1. **İşlem komisyonu (maker/taker).** Limit emirle deftere likidite ekliyorsan maker oranı, piyasa emriyle mevcut likiditeyi tüketiyorsan taker oranı ödersin. Çoğu borsada maker oranı taker'ın yarısı kadar.
2. **Spread.** "Tek tuşla al" ekranları komisyonsuz görünüp uygulama anındaki fiyata gizli maliyet bindirebiliyor.
3. **TL yatırma/çekme.** Yerli borsaların çoğunda TL yatırma ve çekme ücretsiz; küresel borsalarda TL'yi içeri sokmanın yolu genelde başka.
4. **Kripto çekim ücreti.** Coine ve seçtiğiniz ağa göre değişiyor. Küçük tutarlarda transfer sayısı arttıkça bu kalem işlem komisyonunu bile geçebiliyor.
5. **Token indirimi.** BNB, OKB, KCS, GT gibi platform tokenlarıyla komisyon ödemek indirim getiriyor; ama tokenı tutmanın kendi riski var.

Küçük bir örnek: ayda 100.000 dolar hacim çeviren bir hesapta taker oranının %0,10 yerine %0,05 olması, aylık 50 dolar fark demek. Yılda 600 dolar. Tek başına yatırım kararı sebebi değil, ama aynı stratejiyi iki farklı platformda çalıştırıyorsanız görmezden gelinecek bir kalem de değil.

## Türkiye'de ilan edilen spot komisyon oranları

Aşağıdaki tablo, Türkçe kaynaklarda yayımlanan **ilan edilmiş giriş seviyesi** spot oranlarını bir araya getiriyor. Kaynak tarihlerini bilerek yazdım, çünkü bu alanda dolaşan tabloların ciddi bir kısmı eski verilerle çalışıyor.

| Borsa | Giriş seviyesi spot (maker / taker) | Not |
| --- | --- | --- |
| Midas Kripto (yerli) | %0,15 (tek oran, TRY 10 milyona kadar) | 02.10.2026 tarihli karşılaştırma; hacimle %0,12 / %0,10'a iniyor |
| Binance TR | %0,10 / %0,15 | TRY çiftlerinde taker %0,15 olarak da raporlanıyor |
| BtcTurk | %0,12 / %0,20 | Bazı kaynaklar TRY tarafında taker için %0,24 veriyor |
| Paribu | %0,12 / %0,28 | TRY 1 milyon altı hacim |
| OKX TR | %0,10 maker | Taker için iki farklı veri var: %0,15 ve TRY çiftlerinde %0,22 |
| Bybit TR | %0,10 / %0,10 | Yerli şirket; kaldıraçlı işlem sunmuyor |
| Binance (global) | %0,10 / %0,10 | BNB ile ödemede %0,075 |
| OKX (global) | %0,08 / %0,10 | Giriş kademesinde maker tarafında en düşüklerden |
| MEXC | %0 / %0,05 | Maker tarafı sıfır; taker %0,025'e kadar iniyor |
| KuCoin | %0,10 / %0,10 bandı | KCS indirimi ayrı |
| Gate.com | %0,10 / %0,10 | GT ile komisyon ödemesi açıkken %0,09 / %0,09 |
| Kraken Pro | %0,40 / %0,80 | 9 Temmuz 2026'daki düzenlemeyle yükseldi |

Buradan çıkan sonuç net: küresel borsaların büyük kısmı %0,08–%0,10 bandında toplanıyor. Yani "en düşük" iddiası tek bir platforma ait değil; giriş kademesinde MEXC'nin maker tarafı sıfır, OKX maker tarafında %0,08, Binance BNB ile %0,075'e iniyor. Kraken ise bu tablonun en pahalı ucunda duruyor ve hâlâ dolaşan bazı karşılaştırmalar Kraken için eski oranları yazıyor.

Gate'i bu tabloya yerleştirirsek: giriş kademesinde %0,10 / %0,10, GT ile ödemede %0,09 / %0,09. Yani girişte "en düşük" değil; ama kademe yükseldikçe maker tarafı %0'a kadar inen bir yapı var ve asıl hikâye orada başlıyor.

## Gate.com komisyon yapısı: kademeler ve GT indirimi

Gate'in resmi komisyon sayfasındaki spot yapısı iki sütun üzerine kurulu: standart **VIP oranı** ve **GT ile ödeme oranı**. GT (platform tokenı) üzerinden komisyon ödemeyi açtığınızda, aynı kademede daha düşük oran ödüyorsunuz. VIP 0'da bu fark %0,1'den %0,09'a inmek demek; kademe yükseldikçe iki sütun arasındaki açıklık büyüyor.

Gate, 9 Nisan 2026'da spot ve vadeli komisyon yapısını yeniden düzenledi. Duyuruda yer alan tabloya göre VIP 0–VIP 3 oranları sabit kaldı, üst kademelerde GT indiriminin etkisi arttı.

Vadeli tarafta tablo farklı işliyor. Gate'in vadeli komisyon dokümanına göre ücret yalnızca pozisyon açılırken, kapanırken veya kısmi kapatılırken alınıyor; gerçekleşmeyen ya da iptal edilen emirlerde komisyon yok. Ücret pozisyon değeri üzerinden hesaplanıyor, yani kaldıraç oranı komisyon tutarını değiştirmiyor. VIP 0 için yayımlanan seviye maker %0,02 / taker %0,05 civarında; üst kademelerde taker tarafı %0,048'den aşağı iniyor.

### Tüm VIP kademeleri ve ilan edilen oranlar

Aşağıdaki tablo Gate'in resmi komisyon sayfasındaki VIP 0–VIP 16 aralığını, 30 günlük işlem hacmi eşikleriyle birlikte veriyor.

| VIP seviyesi | 30 günlük işlem hacmi eşiği (USD) | Maker / Taker (VIP oranı) | Maker / Taker (GT ile ödeme) | Kayıt |
| --- | --- | --- | --- | --- |
| VIP 0 | 0 | %0,100 / %0,100 | %0,090 / %0,090 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 1 | 60.000 | %0,099 / %0,099 | %0,089 / %0,089 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 2 | 120.000 | %0,098 / %0,098 | %0,088 / %0,088 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 3 | 240.000 | %0,097 / %0,097 | %0,087 / %0,087 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 4 | 500.000 | %0,095 / %0,096 | %0,086 / %0,086 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 5 | 1.000.000 | %0,090 / %0,095 | %0,081 / %0,085 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 6 | 3.000.000 | %0,085 / %0,090 | %0,076 / %0,081 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 7 | 8.000.000 | %0,080 / %0,085 | %0,070 / %0,076 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 8 | 20.000.000 | %0,075 / %0,080 | %0,060 / %0,072 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 9 | 50.000.000 | %0,070 / %0,075 | %0,050 / %0,068 | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 10 | 100.000.000 | %0 / %0,058 | — | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 11 | 120.000.000 | %0 / %0,045 | — | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 12 | 240.000.000 | %0 / %0,037 | — | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 13 | 440.000.000 | %0 / %0,030 | — | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 14 | 800.000.000 | %0 / %0,025 | — | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 15 | 1.600.000.000 | %0 / %0,022 | — | [ Hesap aç](https://bit.ly/GateVIP) |
| VIP 16 | 3.000.000.000 | %0 / %0,020 | — | [ Hesap aç](https://bit.ly/GateVIP) |

> GT ile ödeme sütunundaki oranlar VIP 0–VIP 9 kademeleri için resmi komisyon tablosunda ayrı sütun olarak yayımlanıyor. Oranlar güncellenebildiği için işlem öncesi kendi hesabınızdaki güncel tabloyu kontrol etmek en sağlıklısı.

Tablodan çıkan birkaç pratik sonuç:

- **VIP 10 ve üzeri maker tarafı %0.** Ama buraya çıkmak için 100 milyon dolarlık 30 günlük hacim gerekiyor; perakende kullanıcı için gerçekçi bir hedef değil.
- **Girişteki kazanç GT'de.** Hiçbir şey yapmadan %0,1 / %0,1 ödüyorsunuz; GT ile ödemeyi açtığınızda aynı kademede %0,09 / %0,09. Yani platform tokenını tutmaya istekli biri, daha ilk günden Binance'in BNB'siz oranının altında kalıyor.
- **VIP 5, çoğu aktif trader için gerçekçi ilk durak.** 30 günlük 1 milyon dolar hacim, 14 günlük ortalama 2.000 GT ya da 40.000 dolar hesap varlığı — üçünden **herhangi biri** yeterli. Orada GT ile taker %0,085'e iniyor.

## VIP kademesi nasıl yükseliyor?

Gate'in VIP açıklamalarına göre kademe üç ayrı yoldan birinden yükseliyor: 30 günlük toplam işlem hacmi, 14 günlük ortalama GT varlığı, ya da VIP yükseltme varlık değeri. Üçünü birden tutturmak gerekmiyor; hangisi yüksekse o geçerli.

Hacim hesabında ağırlıklandırma var. Gate'in yayımladığı bilgiye göre spot işlemler tam sayılıyor, vadeli işlemler %40, opsiyonlar %20, CFD işlemleri %10 ağırlıkla hesaba katılıyor. Yani vadeli ağırlıklı çalışan birinin aynı kademeye ulaşmak için spot tarafına kıyasla daha yüksek nominal hacim çevirmesi gerekiyor.

Bir de kademe koruma kuralı var: 30 günlük hacimle yükselen kullanıcılar 60 gün boyunca düşürülmüyor. Varlık veya GT üzerinden yükselenler için bu tampon yok. Yani "hacimle basıp bırakayım" mantığı bir süre işliyor, ama kalıcı bir strateji değil.

## Komisyonu düşürmenin pratik yolları

Bu maddelerin bir kısmı hiçbir ek maliyet gerektirmiyor ve etkisi ilk işlemde görünüyor:

1. **Limit emir kullanın.** Aynı hesapta aynı parite için maker/taker farkı ciddi. Paribu örneğinde %0,28 taker, limit emre geçtiğinizde %0,12'ye iniyor.
2. **GT / BNB / OKB gibi token indirimini hesaplayın.** İndirim gerçek, ama tokenın fiyat riski de sizin. Ayda birkaç işlem yapan biri için bu risk indirimden büyük olabilir.
3. **Piyasa emri yerine emir defterini kullanın.** Basitleştirilmiş "anında al" ekranları çoğu platformda komisyonu spread içine gizliyor. Kraken uygulamasında %1'e kadar çıkan oranların yanında emir defterinde %0,40 bandı var; aynı borsa, iki farklı maliyet.
4. **Transfer sayısını azaltın.** Kripto çekim ücreti sabit olduğu için işlemi böldükçe katlanıyor. Küçük bakiyeleri tek seferde taşımak daha mantıklı.
5. **Ağı kontrol edin.** Aynı coin farklı ağlarda farklı ücretlendiriliyor; USDT'yi TRC20 yerine ERC20 ile çekmek gibi bir tercih doğrudan cebinizden çıkıyor.
6. **Oranın KDV dahil olup olmadığını sorun.** Yerli borsalarda taban aynı değilse iki oranı yan yana koymak yanıltıcı oluyor.

## Yerli borsa mı, küresel borsa mı?

Türkiye'de karşılaştırmanın en can alıcı kısmı komisyon oranından önce para rayı. Yerli borsalarda TL yatırma ve çekme ücretsiz ve doğrudan banka havalesiyle çalışıyor; dört yerli/küresel-yerel platformda TL tarafının ücretsiz olduğu, Bitexen'in çekimde 3 TL + KDV aldığı 30.08.2026 tarihli bir karşılaştırmada görülüyor.

Küresel borsalarda denklem değişiyor. Gate için Türk karşılaştırma siteleri TL girişini P2P ve kart yöntemleriyle listeliyor; yani yerli borsalardaki gibi tek tuşla banka havalesi beklentiniz varsa bunu hesap açmadan önce kontrol etmek gerekiyor. Buna karşılık küresel borsaların ilan edilen işlem oranları, yerli borsaların TRY çiftlerindeki oranlarının altında kalabiliyor: Binance TR'nin TRY tarafındaki %0,15 taker oranına karşılık küresel Binance'te %0,10, OKX'te %0,08–%0,10 bandı var.

Kısaca:

- **Ayda birkaç kez TL ile alım yapıp tutan biri** için yerli borsaların ücretsiz TL rayı, işlem komisyonundaki 5–10 baz puanlık farktan daha değerli olabilir.
- **Yüksek hacimle, sık işlem yapan biri** için %0,08–%0,10 bandı ile yerli borsaların %0,15–%0,28 taker oranı arasındaki fark ciddi bir kalem.
- **Altcoin çeşitliliği arayan biri** için Gate'in listesi geniş; karşılaştırma sitelerinde Gate için 4.000'in üzerinde coin listeleniyor, bunu hesap açmadan önce platformda kendiniz de doğrulayabilirsiniz.

## Düzenleme tarafında iki sık tekrarlanan yanlış

Bu kısım komisyonla doğrudan ilgili değil, ama 2026'da yayımlanan Türkçe karşılaştırmaların ciddi bir kısmı şu iki noktada hatalı:

- **"Her kripto işleminden %0,03 vergi kesiliyor."** Mart 2026'da TBMM'ye sunulan taslakta böyle bir hüküm vardı, ancak 2 Nisan 2026'da kabul edilen ve 17 Nisan 2026'da Resmî Gazete'de yayımlanan 7577 sayılı Kanun'un son metninde bu vergi hükmü bulunmuyor. Yani haber değeri taşıyan bir tasarı, yürürlükte olan bir kural gibi aktarılıyor.
- **"SPK lisanslı borsa."** SPK'nın yayımladığı "faaliyette bulunanlar listesi" geçici bir liste; orada yer almak, ilgili mevzuat kapsamında yetkilendirilmiş olmak anlamına gelmiyor. Bu, Paribu, BtcTurk, Binance TR, Bybit TR, OKX TR ve Midas dahil herkes için geçerli.

Vergi ve lisans konusu kişiye göre değişiyor; oran karşılaştırması yaparken bu iki başlığı ayrı bir yerde doğrulamak gerekiyor.

## Hangi profil için ne mantıklı?

Rakamlar bir yere kadar konuşuyor, gerisi kullanım şekline kalıyor:

- **Ayda 10.000 dolar altı hacim, çoğunlukla piyasa emri:** Giriş kademesi oranı belirleyici. GT/BNB indirimi gibi küçük avantajlar bu ölçekte komik kalıyor; asıl mesele TL rayı ve spread.
- **Ayda 100.000–1.000.000 dolar hacim, limit emir ağırlıklı:** Maker oranı öne çıkıyor. Gate'te VIP 5'te maker %0,09, GT ile %0,081; MEXC'te maker %0. Emir defterine emir bırakma alışkanlığınız varsa iki platformu yan yana çalıştırmak mantıksız değil.
- **Taker ağırlıklı, sürekli içeri giren çıkan bir strateji:** Burada MEXC'nin %0,05 taker oranı Gate'in VIP 5 seviyesindeki %0,085'inden düşük. Gate'te üstünlük ancak yüksek kademelerde ve maker tarafında belirginleşiyor.
- **Küçük hacimle geniş altcoin listesi arayan biri:** Gate'in kademe yapısı girişte diğer büyüklerle aynı bandı veriyor, listede ise fark açılıyor.

Gate'e kayıt olup komisyon sayfasından kendi kademenizi görmek [👉 ücretsiz hesap açarak oranları kontrol etmenin](https://bit.ly/GateVIP) en hızlı yolu; GT indirimini açıp kapatarak aynı işlem için iki farklı oranı yan yana görebiliyorsunuz.

## Sık sorulanlar

**Gate'te komisyon ne kadar?**
VIP 0'da spot işlem oranı %0,10 / %0,10. GT ile komisyon ödemeyi açarsanız aynı kademede %0,09 / %0,09. Kademe yükseldikçe oran düşüyor, maker tarafı VIP 10'dan itibaren %0.

**GT indirimi ne kadar kazandırıyor?**
VIP 0'da 0,1'den 0,09'a inmek, yani kabaca %10 iyileşme demek. Üst kademelerde iki sütun arasındaki fark açılıyor. GT'yi ödeme aracı olarak kullanmak ile GT tutarak kademe atlamak ayrı iki mekanizma; ikisi birlikte çalışıyor.

**"En düşük komisyonlu" borsa hangisi?**
Tek bir cevabı yok. Giriş seviyesinde maker tarafında MEXC %0, OKX %0,08; taker tarafında MEXC %0,05 ile önde. Binance BNB ile %0,075'e iniyor. Gate girişte %0,09 / %0,09 bandında, yüksek hacimde ise maker tarafını %0'a kadar indiriyor. Kararı, sizin emir tipiniz ve hacminiz belirliyor.

**Komisyon dışında neye bakmak gerekiyor?**
TL yatırma/çekme ücreti, kripto çekim ücreti ve seçtiğiniz ağ, ve basitleştirilmiş alım ekranlarındaki spread. Bu dört kalem, ilan edilen oran farkını kısa sürede tersine çevirebiliyor.

**Oranlar sabit mi?**
Değil. Kraken Pro giriş kademesi 9 Temmuz 2026'da %0,40 / %0,80'e yükseldi; Gate 9 Nisan 2026'da spot ve vadeli yapıyı düzenledi. Üçüncü taraf karşılaştırmalarına değil, kaydettiğiniz gün resmi komisyon sayfasına bakmak gerekiyor.
