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

    Modern browsers allow it to work with files, but the access is limited and only provided if the user does certain actions, like "dropping" a file into a browser window or selecting it via an `<input>` tag.

    There are ways to interact with camera/microphone and other devices, but they require a user's explicit permission. So a JavaScript-enabled page may not sneakily enable a web-camera, observe the surroundings and send the information to the [NSA](https://en.wikipedia.org/wiki/National_Security_Agency).
- Different tabs/windows generally do not know about each other. Sometimes they do, for example when one window uses JavaScript to open the other one. But even in this case, JavaScript from one page may not access the other if they come from different sites (from a different domain, protocol or port).

    This is called the "Same Origin Policy". To work around that, *both pages* must agree for data exchange and contain a special JavaScript code that handles it. We'll cover that in the tutorial.

    This limitation is, again, for the user's safety. A page from `http://anysite.com` which a user has opened must not be able to access another browser tab with the URL `http://gmail.com` and steal information from there.
- JavaScript can easily communicate over the net to the server where the current page came from. But its ability to receive data from other sites/domains is crippled. Though possible, it requires explicit agreement (expressed in HTTP headers) from the remote side. Once again, that's a safety limitation.

![](limitations.svg)

Such limits do not exist if JavaScript is used outside of the browser, for example on a server. Modern browsers also allow plugin/extensions which may ask for extended permissions.

## What makes JavaScript unique?

There are at least *three* great things about JavaScript:

```compare
+ Full integration with HTML/CSS.
+ Simple things are done simply.
+ Support by all major browsers and enabled by default.
```
JavaScript is the only browser technology that combines these three things.

That's what makes JavaScript unique. That's why it's the most widespread tool for creating browser interfaces.

That said, JavaScript also allows to create servers, mobile applications, etc.

## Languages "over" JavaScript

The syntax of JavaScript does not suit everyone's needs. Different people want different features.

That's to be expected, because projects and requirements are different for everyone.

So recently a plethora of new languages appeared, which are *transpiled* (converted) to JavaScript before they run in the browser.

Modern tools make the transpilation very fast and transparent, actually allowing developers to code in another language and auto-converting it "under the hood".

Examples of such languages:

- [CoffeeScript](http://coffeescript.org/) is a "syntactic sugar" for JavaScript. It introduces shorter syntax, allowing us to write clearer and more precise code. Usually, Ruby devs like it.
- [TypeScript](http://www.typescriptlang.org/) is concentrated on adding "strict data typing" to simplify the development and support of complex systems. It is developed by Microsoft.
- [Flow](http://flow.org/) also adds data typing, but in a different way. Developed by Facebook.
- [Dart](https://www.dartlang.org/) is a standalone language that has its own engine that runs in non-browser environments (like mobile apps), but also can be transpiled to JavaScript. Developed by Google.
- [Brython](https://brython.info/) is a Python transpiler to JavaScript that allow to write application in pure Python without JavaScript.

There are more. Of course, even if we use one of transpiled languages, we should also know JavaScript to really understand what we're doing.

## Summary

- JavaScript was initially created as a browser-only language, but is now used in many other environments as well.
- Today, JavaScript has a unique position as the most widely-adopted browser language with full integration with HTML/CSS.
- There are many languages that get "transpiled" to JavaScript and provide certain features. It is recommended to take a look at them, at least briefly, after mastering JavaScript.
