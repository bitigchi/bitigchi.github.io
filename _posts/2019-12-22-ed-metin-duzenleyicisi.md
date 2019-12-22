---
title: ed (EDitor)- Unix Metin Düzenleyicisi
tags: ["ed", "unix", "vim"]
lang: tr
layout: post
author: emir
---
Günümüzde işletim sistemi olarak Windows kullanıcılarını saymazsak, büyük olasılıkla bir Unix klonu işletim sistemi kullanıyoruz. O parlak Mac'lerimiz, Linux işletim sistemi, BSD işletim sistemi türevleri... Aslında hepsinin kökeni 1969 yılında serüveni başlayan Unix işletim sisteminin bugünkü son hali. Böyle olunca Unix'in temel parçalarını bugün dahi bu işletim sistemlerinde bulmak olanaklı. Bunlardan biri de *ed* metin düzenleyicisi.

ed'i başlatmak için uçbirimde `ed` yazdıktan sonra Enter'a basın.

![ed](/assets/images/dec2019/ed1.png)

Artık ed'in içerisindesiniz. Bir şey olmadığını düşünmeyin, ed öntanımlı olarak herhangi bir komut istemi sunmaz, programın çalıştığını imlecin bir alt satıra geçmesinden anlarız. Çıkmak için tahmin edeceğiniz üzere `q` yazmanız yeterli. `Q` ise değişiklikleri yoksayıp çıkmamıza olanak veriyor.

![ed](/assets/images/dec2019/ed2.png)

Yok benim kafam karışıyor böyle, bana komut kipinde olduğumu anlatacak bir komut işleci gerekiyor diyorsanız `-p\X` değişkeni ile (X yerine istediğiniz bir karakteri kullanabilirsiniz) bir komut istemi tanımlayabilirsiniz.

![ed](/assets/images/dec2019/ed3.png)

Bu yazıyı okuyorsanız ve bu tür konular ilginizi çekiyorsa vi ve dolayısıyla vim'den de haberiniz vardır. Ancak yine de ed'in vi'nin atası olduğunu belirtmekte yarar var diye düşünüyorum. Bu ne anlama geliyor, bugün kullandığımız temel vim komutlarının yüzde doksanı ed'de çalışır. Dolayısıyla yazı yazmak için `i` (*insert*) veya `a` (*append*) ile ekleme kipine girip istediğimizi yazmaya başlayabiliriz.

![ed](/assets/images/dec2019/ed4.png)

Yazacağımızı yazdıktan sonra ed'e işimizin bittiğini ve komut kipine dönmek istediğimizi belirtmek için yeni bir satırda `.` yazdıktan sonra Enter'a basıyoruz.

![ed](/assets/images/dec2019/ed5.png)

Yazdığımız metni kaydetmek için, evet tahmin ettiğiniz üzere `w`'ye bastıktan sonra dosya adını girmemiz yeterli. Vim'de başına `:` koyuyorduk burada neden yok diye soracak olursanız, komutların başına `:` getirme ed'in bir sonraki sürümü olan ex'te geldi. Bugün de vim kullanırken `:` ile girdiğimiz kip **ex kipi** (komut kipi) olarak adlandırılır.

![ed](/assets/images/dec2019/ed6.png)

Dosyayı kaydettikten sonra ed bize dosyanın kaç bayt olduğunu sayı ile belirtir. Aynı dosyayı açmak için de komut satırında `ed [değişken] [dosya_adı]` dizisini girmemiz yeterli. ed satır bazlı çalışan bir düzenleyici olduğundan bize dosyanın kendisini göstermek yerine yalnızca boyutunu listeleyecektir. Tüm dosya içeriğini listelemek için `,p` yazın.

Yapabilecekleriniz tabii ki bununla sınırlı değil. 5. satıra gitmek mi istiyorsunuz? `5` yazın ve Enter'a basın. Son satırı mi görmek istiyorsunuz? `n` yazın ve Enter'a basın. Kaydıracın üzerinde olduğu satırı görmek için `p` yazın. Kaydıracın üzerinde olduğu satırı değiştirmek için `c` yazın ve metni yazıp `.` ile çıkın. Geri al? `u` hizmetinizde.

Bütün komutları yazmayacağım, vim bilenler birkaç denemeyle olayı çözebilirler.

![ed](/assets/images/dec2019/ed7.png)

Yine vim'en aşina olduğumuz üzere metin bulmak için `/` işlecini kullanmak yeterli. `$` son satıra gider, `^` ile bir önceki, `+` ile de bir sonraki satırı görüntüleyebilirsiniz. Bu işleçlere sayı ekleyerek istediğiniz kadar ileri ve geri gitmeniz olanaklı.

![ed](/assets/images/dec2019/ed8.png)

Bul ve değiştir işlemi de yine vim'den bildiğimiz gibi `%s/değiştirilecek/yeni/global` komutuyla yapılıyor. Bu şekilde düzenli ifadeler kullanarak metin üzerinde istediğiniz oynamaları yapabilirsiniz.

Neyse, çok oyalandık, beyitimizi bitirelim artık.

![ed](/assets/images/dec2019/ed9.png)

Bitmiş ve kaydedilmiş hali:

![ed](/assets/images/dec2019/ed10.png)

ed içerisindeyken kabuk komutlarını başına `!` ekleyerek çalıştırabiliyoruz. Yine vim'de en çok kullandığımız özelliklerden bir tanesi.

Her ne kadar günlük işlerimde ed'i pek kullanmayacak olsam da, işletim sistemini saymadan böyle tarihi bir eserin yine elimizin altında olduğunu bilmek ve kullanabilmek gerçekten hoş bir duygu. Bugün kullandığımız yazılımlar o kadar karmaşıklaştı ki, eskilerin böyle programlarla bugün kullandığımız işletim sistemlerini yazdıklarını düşününce kişi bir tuhaf oluyor.

ed hakkında daha fazla bilgi almak ve tüm komutlarını görmek için [bu sayfaya](https://www.tutorialspoint.com/unix_commands/ed.htm) göz gezdirebilirsiniz.
