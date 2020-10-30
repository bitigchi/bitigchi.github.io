---
title: "Türkçe Vim"
tags: ["vim", "Türkçe", "yerelleştirme"]
lang: tr
layout: post
---
Bu giriyi yazmak için bayadır bekliyordum. Yazayım da aradan çıksın.

Vim artık Türkçe. Biraz daha spesifik yazacak olursak 8.1.2200 sürümünden itibaren Türkçe. Hemen şimdi denemek isterseniz Windows için gecelik kur paketlerini [bu adresten](https://github.com/vim/vim-win32-installer/releases), Linux için AppImage kalıplarını da [bu adresten](https://github.com/vim/vim-appimage/releases) indirebilirsiniz. macOS ve diğer BSD tayfası güncel Github deposunu klonladıktan sonra birkaç komut girerek kısa sürede derleyebilir. Derleme ve yapma yönergeleri [burada](https://github.com/vim/vim/blob/master/src/INSTALLmac.txt).

![Türkçe Vim](/assets/images/dec2019/vim.png)

Türkçe yerelleştirmeyi içeren bir Vim sürümü şu an için Debian Testing ve pek tabii ki Arch Linux depolarında mevcut, almak isteyen olursa bu depoları kullanabilir.

Vim'in tarihi ta 1970'li yıllara dayanıyor; aslında kendisi Unix bilgisayarlarda öntanımlı metin düzenleyicisi olarak gelen `vi`'nin bir klonu. 50 yıla yaklaşan bir tarihi olan bir yazılımın hâlâ Türkçe yerelleştirmesinin olmadığını gördüğümde kendimi bir tür borçlu hissettim. Uzun geceler ve yaklaşık 2600 satır diziden sonra artık kullanırken garip bir mutluluk hissetmiyorum desem yalan olur.

Aynı zamanda Vim artık Türkçe yazım denetimi de yapabiliyor. Yazım denetimini açmak için komut kipinde `:set spell spelllang=tr` yazmanız yeterli. Vim Türkçe yazım dosyasını indirmek için sizden izin isteyecektir. Ekrandaki yönergeleri izledikten sonra Vim'in yanlış yazılan veya henüz sözlükte olmayan sözcükleri imlediğini ayrımlayacaksınız. Genel Ağ'da bu özelliğin nice kullanılabileceği ile ilgili ayrıntılı yönergeler mevcut. Vim yazım denetimi için LibreOffice Türkçe yazım sözlüğünü kullanıyor, ancak Vim'in kendi biçimine dönüştürürken yaşanan bazı sorunlar nedeniyle doğru bildiğimiz bazı sözcükler yanlış diye imlenebilir, ileriki sürümlerde bu hatanın düzelmesini bekliyoruz.

Eğer kullandığınız metinlerde birden fazla dil mevcut ise `spelllang=tr,en,de` (evet, üç tane l) şeklinde birden fazla dil tanımlayabilirsiniz.

Son olarak, Vim öğrenmek istiyorsanız ancak öğrenme eğrisi gözünüzü korkutuyorsa, korkmayın. Uçbirimde `vimtutor` yazarak Vim öğreticisini çalıştırabilirsiniz (evet o da Türkçe). Vim temelini hızlıca öğrenmenizde size yararlı olacaktır.

Çevirilerde gözünüze takılan bir hata olursa lütfen bana bildirin. Vim aslında devasa bir program ve tahmin edemeyeceğiniz kadar çok özellik içeriyor.
