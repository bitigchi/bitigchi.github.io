---
title: "Yeni Eski Türkçe Klavye Dizilimi"
tags: ["Göktürkçe", "Eski Türkçe", "Old Turkic", "klavye"]
lang: tr
layout: post
author: emir
---
Dil ile ilgilenmeye başladığım ilk zamanlar Eski Türkçenin, daha bilinen adıyla Göktürkçenin sayısal ortamda ilk kullanılabilir olduğu zamanlara denk geliyor, 2009 yılı civarı. Göktürk damgaları o zaman [Unicode](https://unicode.org)'a yeni eklenmişti ve destekleyen platformlarda doğal olarak yazımının önü açılmıştı. Daha önceleri yapılan Göktürk yazıtipleri mevcuttu elbet, ancak tüm bu yazıtipleri Latin harflerinin atalı olduğu kod konumlarında Latin harflerinin şeklini değiştirerek çalışıyordu. Dolayısıyla o yazıtipinin yüklü olmadığı bilgisayarlarda görüntülenmesine olanak yoktu. Damgaların Unicode'a girmesiyle artık çoğu bilgisayarda bir zorluk olmaksızın damgaları görüntüleyebilecektik; artık bu bir zaman sorunuydu.

Bu heyecanla bendeniz hemen Linux, macOS ve Windows için birer klavye düzeni hazırlayıp ağa koydum. Bu klavye düzeni üzerinde herhangi bir bilimsel veya özverili çalışma yapılmamış, yalnızca Orhun yazıtlarındaki damgaları içeren aleladele bir çalışma idi. Ne derece kullanıldı, birinin işine yaradı mı, yaradıysa da ne derece yaradı herhangi bir fikrim yok. Ancak genel kullanım için yetersiz olduğu kesindi.

Orkun damgalarının bulunduğu Unicode kod alanında toplam 73 damga bulunuyor. Damgalar Unicode'a eklenirken yalnızca Orhun vadisi yazıtları değil, Yenisey vadisinde bulunan yazıtlardaki damgalar da bu ölçüne eklendi. Yenisey bölgesindeki yazıtlar genelde tarih olarak Orhun vadisindeki yazıtlardan daha önceye dayanıyor, damgaların evrimi ve coğrafyanın değişik olmasından dolayı aynı sesi veren damgaların mevcut olan iki biçimi de Unicode'a eklenmiş. Bu damgaların kolay bir şekilde yazılamaması beni rahatsız ediyordu ve bu nedenle yeni bir klavye düzeni yapmaya karar verdim. Aşağıda detaylarını göreceğiniz klavye düzeninde sayısal olarak ölçünlenmiş bütün 73 damgayı da yazmak olanaklı.

![Görsel 1: Dizilimin genel görünümü](/assets/images/nov2019/layout.png)

Öncelikle belirtmeliyim ki, bu dizilim Eski Türkçe ve Eski Türkçe söz varlığı temel alınarak hazırlanmıştır. Dolayısıyla Türkiye Türkçesi ve çağdaş metinlerin yazımı için beklediğiniz kadar uygun olmayabilir.

İndirmek için:
* [macOS](/oldTurkic/mac_old_turkic.zip)
* [Linux](/oldTurkic/linux_old_turkic.zip)
* [Windows](/oldTurkic/win_old_turkic.zip)

Ayrıntılı yönergeler her bir `.zip` dosyasının içinde mevcut. Herhangi bir hata veya soru için lütfen bana ulaşın.

Eğer damgaları görüntüleyemiyorsanız, güncel bir işletim sistemi kullandığınızdan ve bilgisayarınızda bir Eski Türkçe yazıtipinin yüklü olduğundan emin olun. Win 8.1 ve macOS 10.11 sonrası Eski Türkçe yazıtipleri ile yüklü gelmektedir. Linux dağıtımları için yine yukarıdaki bağlantıdan istediğiniz bir yazıtipini indirebilirsiniz. Paket yöneticinizde büyük olasılıkla Noto yazıtipleri olacaktır, bu yazıtiplerinde de Eski Türkçe desteği mevcut.

Şimdi ayrıntılara gelelim

Eski klavye diziliminde damgaların kalın ve ince halleri için Shift ve Caps Lock değiştiricileri kullanılıyordu. Bu standart bir klavyeye tüm Orkun damgalarının sığmasını sağlarken, numaralar ve noktalama için de yeterince boşluk bırakıyordu. Ancak bu dizilime Yenisey karakterlerini de koymaya kalkınca yer sıkıntısı ve düğme değiştiricileri kullanmak baya zordu. Bu yüzden yeni dizilimde damgaların hem ince hem de kalın durumları aynı dizilimde yer alıyor.

Türkçe F klavye dizilimi üzerine okuduysanız, bu dizilimin zamanında Türkçenin söz varlığı çözümlendikten sonra en çok görülen seslerin en kolay ulaşılabilir yerlere konumlandırıldığını biliyorsunuzdur. Bu yeni dizilimde ben de benzer bir yöntem gütmeye çalıştım. Elimde zamanında sayısal ortama geçirdiğim yazıt metinlerini karakter sıklığı bakımında analiz ettiğimde Türkçe F dizilimine yakın sonuçlar elde ettiğimi gördüm, bu da benim işimi baya kolaylaştırdı. Dolayısıyla bu yeni dizilimin Türkçe F diziliminden esinlendiğini söylemek yanlış olmaz. Önemli bir ayrımdan söz etmek gerekirse, Orkun-Yenisey yazısında 𐰀 (a-e) damgası genelde sözcük sonu dışında pek yazılmadığından serçe parmağın basacağı yere gitmek zorunda kaldı. Bunun dışında her iki dizilimi yanyana alıp baktığınızda pek çok sesin aynı düğmeye denk geldiğini göreceksiniz.

Bu yeni dizilimin bir önemli ayrımı da numara sırasında. Orkun-Yenisey yazısı pek çok iki sesli damga barındırdığından, bunları da klavyede erişilebilir bir yere koymak önemliydi. Orkun-Yenisey yazısında bildiğimiz anlamda rakamlar olmadığından, rakamları Alt (Gr) düğmesi ile ulaşılabilir yapıp rakamların yerine bu çoklu sesli damgaları yerleştirdim. Boş kalan yerleri de Yenisey damgaları doldurdu.

Bu dizilimde Yenisey damgalarına ulaşmak için Shift düğmesini kullanabilirsiniz. Örneğin Orkun yazısında 𐱃 ile gösterilen /at/ damgasının Yenisey sürümü Shift düğmesine basıldığında 𐱄 olarak karşımıza çıkıyor. Alt (Gr) düğmesi ile ulaşılabilen tek damga 𐰬 (Yenisey ang) damgası. Bu sesin Orkun karşılığı olmadığından Orkun eng (𐰭) ve Yenisey eng (𐰮) damgaları ile aynı düğmeden ulaşılabilir.

Çok kullanılan noktalama imlerine yine Shift ile ulaşabilirsiniz. Daha fazla ime gereksiniminiz varsa Alt (Gr) düğmesi bugün yaygınca kullanılan tüm noktalama imlerini ve bazı eklemeleri de içeriyor. Ayrıca macOS ve Linux üzerinde Alt (Gr) + Shift ikilemesi standart yerleşim noktalama karakterlerini verecektir.

Tüm damgaların yerleşimini gösteren bir PDF dosyasını dizilimlerle birlikte bulabilirsiniz. Eğer sorularınız olursa [İletişim](/contact.html) bölümünden bana yazmaya çekinmeyin.

Yeni ağ günlüğümün ilk girisini de böyle güzel bir olaya yazmak nasip oldu. Umarım ileride daha güzel şeyler yazabilirim.

Sağlıcakla kalın.
