---
title: "Vim için Türkçe düğme eşlemler"
tags: ["f klavye", "vim", "Türkçe"]
lang: tr
layout: post
author: emir
---
Vim'in standart ABD-QWERTY klavyesi dışındaki klavyelerde kullanımının pek de kolay olmadığı bir gerçek, bu yüzden çoğu programcı Vim kullanırken ya standart QWERTY dizilimini kullanıyor ya da düğme eşlem betiklerinden yararlanıyor.

Düğme eşlem betikleri ile Vim komutlarını `NORMAL` kipte sanki standart QWERTY dizilimini kullanırmışçasına verirken `EKLE` kipinde de yeğlediğiniz herhangi bir klavye dizilimini kullanabilirsiniz. Ancak şimdiye dek Vim'in Türkçe düğme eşlem desteği bulunmuyordu.

Vim'i Türkçe Q klavye ile kullanmak gerçekten bir eziyet. Çoğu sembol SHIFT ve ALT-GR düğmeleri ile erişilebiliyor ve yerleşimleri de gayet uygunsuz. F klavyenin sembol yerleşimleri biraz daha uygun olsa da bu kez de Vim dolaşım düğmeleri (H, J, K, L) yan yana değil. Bir süre sonrasında etkili komut verme ve hızlı Türkçe yazma arasında bir seçim yapmak gerekebiliyor.

Vim'in güncel sürümü (8.2.1388 ve sonrası) artık Türkçe Q ve F dizilimleri için düğme eşlem betikleri içeriyor. Böylece sistem klavyenizi standart QWERTY'e geçirerek Vim komutlarınızı bu klavye üzerinden verebilir, `EKLE` kipinde de Türkçe klavyenizi kullanabilirsiniz.

Etkinleştirmek için:

- `:set keymap=turkish-f` veya `:set keymap=turkish-q` komutlarını kullanın.
- Bu ayarları kalıcı yapmak için `.vimrc` dosyanıza yukarıdaki komutları ekleyebilirsiniz.

Düğme eşlemi kapatmak için `EKLE` veya `KOMUT` kipindeyken 'CTRL-^' kısayolunu kullanabilirsiniz. Standart QWERTY diziliminde '^' sembolünün 6 düğmesinde olduğunu unutmayın.

Daha önceki bir [yazımda](https://bitigchi.github.io/2019/11/05/vimde-eski-turkce-yazma.html) Vim'in düğme eşlem özelliğini Eski Türkçe yazmak için de kullanabileceğinizden söz etmiştim. Çağdaş Türkçe ise biraz geç de olsa en sonunda geldi. Umarım birilerine yararlı olur.
