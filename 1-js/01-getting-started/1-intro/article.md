# JavaScript-e giriş

JavaScript-i beýle aýratyn edýän zat nämedigini göreliň, biz onuň bilen näme edip bileris we ol başga haysy tehnologiýalar bilen gowy işleýär.

## JavaScript näme?

*JavaScript* ilkibaşda  "web sahypalary interaktiw" etmek üçin döredilipdi.

Bu dilde programmalara *skriptler (kod bölejikleri)* diýilýär. Skriptler HTML bilen birikdirilýär we web sahypa ýüklenen-den soň awtomatiki usulda işläp başlaýar.

Skriptler arassa tekst görnüşinde berilýär we şol durşuna-da işledilýär. Olary işletmek üçin aýratyn taýýarlyk ýa-da kompliýasiýa gerek dal.

Bu nukdaýnazardan, JavaScript [Java](https://en.wikipedia.org/wiki/Java_(programming_language)) dilinden düýbünden tapawutlanýar.

```smart header="Why is it called <u>Java</u>Script?"
JavaScript ilkinji döredilende onuň ady: "LiveScript" boldy. Şol wagtlar Java dili has meşhurlyga eýe bolupdy, şeýlelikde JavaScript  Java-nyň "jigisi" bolar diýen düşünje bilen onuň adyna meňzeş at dakmak kararyna geldiler.

Emma JavaScript kämilleşdigiçe, [ECMAScript](http://en.wikipedia.org/wiki/ECMAScript) diýilýän standartizasiýa guramasy bilen bilelikde düýbünden Java-dan garaşsyz dil boldy we häzir Java bilen adyndan başga hiç hili baglanyşygy ýok.
```

Häzirki günlerde, JavaScript diňe brauzer-de däl, eýsem serwer tarapda ýa-da bolmasa islendik enjamda [ JavaScript motory (the JavaScript engine)](https://en.wikipedia.org/wiki/JavaScript_engine) diýlip atlandyrylýan motoryň kömegi bilen işläp bilýar.

Brauzer-iň içine  "JavaScript virtual machine" diýen wirtual maşyn oturdylandyr.

Her wirtual maşynyň özune mahsus "kod atlary" bardyr. Mysal üçin:

- [V8](https://en.wikipedia.org/wiki/V8_(JavaScript_engine)) --  Chrome we Opera üçin.
- [SpiderMonkey](https://en.wikipedia.org/wiki/SpiderMonkey) -- Firefox üçin.
- ...Başga-da  IE(Internet Explorer) üçin "Chakra",  Microsoft Edge üçin "ChakraCore",  Safari üçin "Nitro" we "SquirrelFish" we ş.m.

Ýokardaky atlary we adalgalary ýadyňyzda saklaň, sebabi olar internetdäki makalalarda ulanylýar. Olary biz hem ulanarys. Meselem, eger "X aýratynlyk V8 tarapyndan goldanylýar" diýilse, onda diýmek şol aýratynlyk Chrome we Opera brauzerlerinde işleýär diýmekdir.

```smart header="How do engines work?"

Motorlar çylşyrymlydyr. Emma düýp esaslary aňsat.

1. Motor (eger bir brauzer-e oturdylan bolsa (gömulen bolsa)) skriptleri  okarýar ("parses").
2. Soňra ony maşyn diline öwürýär ("compiles").
3. we maşyn diline öwürlen kod çalt işleýär.

Motor ýokardaky ädimleriň (prosesiň) dowamynda her ädimi optimizasiýa edýar. Hatda düzülen skriptiň işleýşine seredýär, içinden geçýän maglumatlary seljerýär we şol maglumatlaryň esasynda maşyn koduny hasam optimallaşdyrýar.
```

## Brauzer-de JavaScript nämeler edip bilýär ?

Häzirki zaman JavaScript "howpsuz" programmirleme dildir. Ol pes-derejeli (low-level) operasiýalary ýerine ýetirmeýär, ýagny kompýuteriň ýadyna ýa-da prosessora (CPU) girip bilmeýär, sebabi ol ilkibaşda şu operasiýalara zerurlyk duýmaýan brauzer-ler üçin niýetlenipdi.

JavaScript-iň ukyplary onuň işleýän sferasyna baglydyr. Meselem, [Node.js](https://wikipedia.org/wiki/Node.js) faýllary okaýan/ýazýan, tor isleglerini ýerine ýetirýän, we ş.m. ýaly funksiýalary goldaýar.

Brauzer-de JavaScript web sahypalary dolandyrmak, ulanyjy bilen interaksiýa (täsirleşmek) we brauzer-e degişli ähli zatlary edip biler.

Meselem, JavaScript brauzer-de şu aşakdakylary edip biler:

- Sahypa täze HTML goşmak, bar bolan mazmuny üýtgetmek, stili (şekili) üýtgetmek.
- Ulanyjy hereketlerine jogap bermek, syçanjygyň hereketlerini ýerine ýetirmek, kursoryň herektlerini, klawişa basylanda emele gelýän wakalary ýerine ýetirmek.
- Tor-yň üsti bilen uzakdaky serwere maglumatlary ugratmak, faýllary indirmek(download) we ýüklemek (upload)  ([AJAX](https://en.wikipedia.org/wiki/Ajax_(programming)) we [COMET](https://en.wikipedia.org/wiki/Comet_(programming)) diýip atlandyrylýan tehnologiýalar bilen).
- Cookie-leri almak we ýerleşdirmek, sahypany zyýarat edýänlere sorag bermek, habarlary (maglumatlary) görkezmek.
- Müşderi tarapynda (client-side) maglumatlary saklamak ("local storage").

## JavaScript brauzer-de nameler edip bilmeýär ?

JavaScript-iň brauzerdäki ukyplary, ulanyjynyň howpsuzlygy üçin çäklidir. Esasy maksat, erbet web sahypasynyň şahsy maglumatlara girmeginiň ýa-da ulanyjynyň maglumatlaryna zyýan ýetirmeginiň öňüni almakdyr.

Şeýle çäklendirmelere şular girýär:

- JavaScript web sahypada gaty disk-däki (hard disk) faýllary ýazyp/okap/pozup, olary göçürip alyp (kopýalap) ýa-da programmalary işledip bilmeýar. Onuň Operasion Sistema-nyň (OS) funksiýalaryna gös-göni girmäge rugsady ýokdur.

    Häzirki zaman brauzerleri faýllar bilen işlemäge mümkinçilik berýär, emma giriş çäklidir we diňe ulanyjy faýly brauzeriň penjiresine "taşlamak" ýa-da  `<input>` teg-i arkaly saýlamak ýaly käbir hereketleri eden ýagdaýynda üpjün edilýär.

    Kamera/mikrofon we beýleki gurluşlary ulanmagyň ýollary bar, emma munuň üçin ulanyjynyň aç-açan rugsady talap edilýär. Şonuň üçin JavaScript bilen işleýan web sahypa  kamerany gizlinlikde işledip, daş-töweregi synlap we maglumatlary [NSA](https://en.wikipedia.org/wiki/National_Security_Agency)-a ugradyp bilmez.
- Dürli-dürli penjireleriň/tablaryň biri-biri bilen baglanyşygy ýokdur (biri beýlekisini tanamaýar). Käwagt şeýle edýärler, meselem bir sahypa beýelikini JavaScript ulanyp açjak bolanda. Emma şeýle ýagdaýda hem JavaScript-iň beýleki tab-a girmage rugsady ýokdur, eger-de başga saýtdan (domain-den, protocol-dan ýa-da port-dan) gelýän bolsa.


    Muňa "Birmeňzeş gelip çykyş syýasaty"("Same Origin Policy") diýilýär. Munuň üstünde işlemek üçin * iki sahypa * maglumat alyşmak üçin biri-biri bilen ylalaşmaly we olary dolandyrýan ýörite JavaScript kody bolmaly. Munuň üstünde soňra durup geçeris.

    Bu çäklendirme ulanyjynyň howpsuzlygy üçindir. Ulanyjynyň açan `http://anysite.com` sahypasy `http://gmail.com` URL bilen başga tab-a girip bilmez we ol ýerden maglumat ogurlap bilmez.
- JavaScript açan sahypaňyz-da aňsatlyk bilen serwer bilen bilelikde maglumat alyş-çalyş edip biler. Emma başga saýt/domain bilen maglumat alyş-çalyş edip bilmegi kän bir mümkin däl. Mümkin bolsa-da, oňa uzakdaky serwerden aç-açan ylalaşyk (HTTP header-de anlatmaly) zerurdyr. Ýene bir gezek gaýtalaýaryn, bu ulanyjynyň howpsuzlygy üçindir.

![](limitations.svg)

Eger-de JavaScript brauzer-iň daşynda (meselem serwerde) ulanylsa, şeýle çäklendirmeler ýokdur. Häzirki zaman brauzerler giňeldilýän rugsatlary sorap bilýän  plugin we extension-lere hem rugsat berýär.

## JavaScript-i näme zat özboluşly edýär?

JavaScript-i özboluşly edýän iň azyndan *üç* sany zady aýtmak bolar:

```compare
+ HTML/CSS bilen bilelikde dolulygyna işläp bilmegi.
+ Ýonekeý zatlary ýonekeýje edip bilmegi.
+ Tanymal ähli brauzer-ler tarapyndan goldanylýar we olarda deslapky (default) görnuşinde işleýändir.
```
JavaScript bu üç zady birleşdirýän ýeke-täk brauzer tehnologiýasydyr.

Ine JavaScript-i özboluşly edýän zat. Şonuň üçin brauzer interfeýslerini doretmek ulanylýänlygy üçin giňden ýaýrandyr.

Ýokarda belläp geçişimiz ýaly, JavaScript serwerleri döretmekde, mobil programmalary düzmekde, kompýuter programmalary we ş.m. ýerlerde ulanylýändyr.

## JavaScript-iň "üstündäki" diller

JavaScript-iň sintaksisi hemme kişiniň zerurlyklaryny doly laýyk gelenok. Her kim her hili aýratynlyklary isleýärler.

Ýagdaý şeýle, sebäbi her kişiniň proýektleri we zerurlyklary dürli-dürlidir.

Soňky döwürde brauzer-de işledilmezinden ozal JavaScript kodyna *transpiled* (öwrülen => converted) edilýän birnaçe dil emele geldi

Häzirki zaman gurallar transplasiýany has tiz we aýdyn edip, programmistleriň başga dilde kod ýazmaklaryna mümkinçilik döretdiler.

Şeýle dilleriň sanawy:

- [CoffeeScript](http://coffeescript.org/) JavaScript üçin "syntactic sugar" (sintaktik şeker)-dir . Bize has gysga kod ýazmaga, arassa we takyk kod ýazmaga mümkinçilik berýär. Edil Ruby programmistleri ýaly.
- [TypeScript](http://www.typescriptlang.org/) çylşyrymly sistemalaryň ösüşini we goldawyny ýonekeýleşdirmek üçin "berk maglumat kysymlaryny" ýazmaga gönükdirilendir. TypeScript Microsoft tarapyndan döredilendir. 
- [Flow](http://flow.org/) - munda hem "berk maglumat kysymlary"-ny goşup bilýärsiňiz, emma üýtgeşik usulda. Bu Facebook tarapyndan döredildi.
- [Dart](https://www.dartlang.org/) brazuer ýok ýerlerinde (mobil programmalar ýaly) işýleýän, ýöne JavaScript-e convert edip bolýan özbaşdak motory (engine) bolan garaşsyz bir dildir. Bu Google tarapyndan döredildi.
- [Brython](https://brython.info/) JavaScript-siz arassa Python kody bilen programma ýazmaga mümkinçilik berýän, JavaScript kodyna öwürýän Python transplýasiýasydyr.

Ýene-de köp bar. Of course, even if we use one of transpiled languages, we should also know JavaScript to really understand what we're doing.

## Gysgaça

- JavaScript ilkibaşda diňe brauzer-de işleýän dil hökmünde döredilipdi, emma ol häzir başga birnäçe gurşawlarda işleýär.
- Häzirki wagtda JavaScript, HTML / CSS bilen doly integrasiýa bilen iň giňden kabul edilen brauzer dili hökmünde özboluşly orny eýeleýär.
- JavaScript-e "tranpirlenen" we käbir aýratynlyklary berýän köp dil bar. JavaScript-i özleşdirenden soň, iň bolmanda gysgaça olara göz aýlamak maslahat berilýär.
