---
title: Vim'de Eski Türkçe Yazmak
tags: ["vim", "Göktürkçe", "Old Turkic", "Eski Türkçe"]
lang: tr
layout: post
---
Vim yeni başlayanlar için korkutucu görünse de, özünde pek çok yararlı özellik barındıran, "*ufacık fıçıcık, içi dolu turşucuk*" türünden şirin mi şirin bir metin düzenleyici. Alışma süresi biraz sancılı geçse de alıştıktan sonra `vim` dışında başka bir metin düzenleyicisini artık açmadığınızı ayrımlıyorsunuz. Vim'in özelliklerine ve kullanımına bu yazıda değinmeyeceğim doğal olarak, bunun için internette istemediğiniz kadar kaynak mevcut. Bu yazıda değinmek istediğim Vim'in "düğme eşlem" (*keymap*) özelliği ve bu özellik ile nasıl herhangi bir eklentiye veya klavye dizilimine gereksinim duymadan Eski Türkçe (Göktürkçe) yazabileceğimiz.

Düğme eşlem özelliği kısaca belirli düğme dizgileri kullanıldığında belirli karakterleri ekrana yazdırmayı sağlayan bir özellik. Özellikle standart Latin dışı karakterleri sık kullanıyorsanız bu özellik baya işinize yarayacaktır. Bu özelliği bugün çağdaş masaüstü ve taşınabilir işletim dizgelerinde, özellikle sohbet uygulamalarında belirli kalıpları kısaltmak için kullanıyoruz. Vim, öntanımlı olarak baya bir geniş karakter/alfabeler aralığı için şablonlar içeriyor. Bu şablonlar arasında Eski Türkçe hem Orhun hem de Yenisey damgaları ile bulunuyor. Gelin bu özelliği nasıl kullanacağımızı öğrenelim.

Vim'i çalıştırmak için uçbirim öykünücünüzü açıp `vim` yazın. Eğer Windows kullanıyorsanız [bu adresten](https://www.vim.org) grafik arabirim içeren sürümünü kurabilirsiniz. Vim açıldıktan sonra doğrudan komut kipinde başlar.

Orhun kipine geçmek için komut kipindeyken:

`:set keymap=oldturkic-orkhon` yazıp <Enter>'a basın.

Yenisey kipine geçmek için komut kipindeyken:

`:set keymap=oldturkic-yenisei` yazıp <Enter>'a basın.

> ÖNEMLİ: Eğer uçbirim öykünücünüz sağdan sola yazımı desteklemiyorsa girdiğiniz karakterler soldan sağa dizilecektir. Endişelenmeyin, bu yalnızca uçbirimdeki görünümü etkiler, eğer aynı dosyayı başka bir uygulama ile açarsanız sağdan sola yazımın uygulandığını göreceksiniz. Bildiğim kadarıyla şu an yalnızca GNOME 3.34 uçbirimi (VTE) ve macOS uçbirimi doğal sağdan sola görüntülemeyi destekliyor.

Bu komutları girdikten sonra vim komut satırı girdiğiniz komutları aynı biçimde gösterecektir. Ekleme kipine geçmek için `i` düğmesine basın. Uygulamanın alt kısmında `-- INSERT (oto) --` yazdığını göreceksiniz. Ayraçlar içindeki `oto` Eski Türkçe (Old Turkic) kipinde olduğumuzu gösterir. Artık Eski Türkçe yazmaya başlayabiliriz.

Klavyenizin düğmelerine bastığınızda yine Latin karakterlerin ekranda belirmeye başladığını göreceksiniz. Hmm. Bir şeyler yanlış gidiyor diye düşünmeyin, Eski Türkçe damgalar birden fazla ses içerdiği için damgaları yazabilmek için birden fazla düğme girdisi kullanmamız gerekecek. Nasıl yazabileceğimize bakalım:

Türkçe Latin Abecesi (TLA), OET (Orhun Eski Türkçe), YET (Yenisey Eski Türkçe)

TLA: Bu ses biter mi?

OET: 𐰉𐰆 𐰾𐰾 𐰋𐰃𐱅𐰀𐰼 𐰢𐰃?

YET: 𐰊𐰆 𐰾𐰅𐰾 𐰌𐰄𐱆𐰁𐰼 𐰢𐰄?

"Bu" sözcüğüne bakalım:

* Orhun yazımı: 𐰉𐰆, içerdiği damgalar ab ve o damgaları. Dolayısıyla "Bu" sözcüğünü yazmak için önce Orhun kipindeyken `ab` ve `O` veya `U` yazmamız gerekiyor (Eski Türkçede o ve u sesi aynı damga ile gösterilir).
* Yenisey yazımı: 𐰊𐰆, içerdiği damgalar ab ve o damgaları. Ancak o/u damgasının kendine özel bir Yenisey sürümü olmadığından yazmak için Orhun kipine geçiş yapmamız gerekiyor.

> Düğme eşlem şablonları arasında geçiş yapmak için komut kipinde aşağı ve yukarı ok düğmeleri ile son kullanılan komutlar arasında gezinebilirsiniz.

"Ses" sözcüğüne bakalım:

* Orhun yazımı: 𐰾𐰾, içerdiği tek damga es damgası. Yazmak için `es`/`aes` yazmamız yeterli.
* Yenisey yazımı: 𐰾𐰅𐰾, içerdiği damga es ve kapalı e damgası. Orhun yazımına ek olarak `e` yazmamız yeterli. Es damgasını Orhun kipindeyken yazıyoruz.

"Biter" sözcüğüne bakalım:

* Orhun yazımı: 𐰋𐰃𐱅𐰀𐰼, içerdiği damgalar eb, i, et, a/e ve er damgaları. Evet doğru tahmin ettiniz, `eb`, `I`, `et`, `A` ve `er` yazarak bu sözcüğe ulaşabiliriz. Sesli damgalar için büyük harf kullanmamız gerekiyor. Eski Türkçede a ve e sesi aynı damga ile gösterildiğinden /e/ sesi için `A` kısayolu kullanılmış.
* Yenisey yazımı: 𐰌𐰄𐱆𐰁𐰼, içerdiği damgalar eb, i, et, a/e ve er damgaları. Orhun yazısı ile aynı düğmeleri kullanıyoruz, yalnızca "er" damgası için yeniden Orhun kipine geçiş yapmamız gerekiyor, çünkü Yenisey ile Orhun kullanımı aynı.

"Mi" sözcüğüne bakalım:

* Orhun yazımı: 𐰢𐰃, içerdiği damgalar m ve i. M damgasının ayrı bir ince ve kalın sürümü olmadığından, demeli tek damga ile yazıldığından `m` veya `em` yazabilirsiniz. İ sesi için yine `I` yazıyoruz.
* Yenisey yazımı: 𐰢𐰄, içerdiği damgalar m ve i.

Örnekte bulunmuyar ancak ö ve ü içeren damgalar için yine Latin yazıçevrimini kullanıyoruz:

TLA: ö/ü, ök

OET: 𐰇, 𐰜

YET: 𐰈, 𐰝

Bu damgaları sırasıyla `oe` ve `oek` girerek çıkartabilirsiniz. Eklemem gereken bir şey daha var ki, bu özellik Vim'e eklenirken her damga için üç veya daha fazla dizgi tanımlanmış. Eğer bu dizgileri görmek isterseniz [bu adresten](https://github.com/vim/vim/tree/master/runtime/keymap) ilgili dosyaları inceleyebilirsiniz.

Orhun-Yenisey kipinden çıkmak ve normal Latin kipine geçmek için `:set keymap=` yazmanız yeterli. Sorularınız olursa ulaşmaktan çekinmeyin!
