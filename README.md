<p align="center"><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/logo.svg"/></a><br/><a href="https://xxai.art"><img src="https://cdn.jsdelivr.net/gh/xxai-art/doc/xxai.svg"/></a></p><p align="center"><a href="https://github.com/xxai-art/doc#readme"><img alt="I18N" src="https://cdn.jsdelivr.net/gh/wactax/img/t.svg"/></a>　<a href="https://groups.google.com/u/0/g/xxai-art"><img alt="Google Groups" src="https://cdn.jsdelivr.net/gh/wactax/img/g-groups.svg"/></a></p>

Ana ba da shawarar shigar da nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) farko, sannan `direnv allow` bayan shigar da directory ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) za a kashe ta atomatik bayan shigar da directory).

Ma'anar ita ce: Fassarar Sinanci zuwa Jafananci, Koriya, Turanci, fassarar Turanci zuwa duk sauran harsuna. Idan kuna son tallafawa Sinanci da Ingilishi kawai, kuna iya rubuta `zh: en` .

Ma'anar ita ce: Fassarar Sinanci zuwa Jafananci, Koriya, Turanci, fassarar Turanci zuwa duk sauran harsuna. Idan kuna son tallafawa Sinanci da Ingilishi kawai, kuna iya rubuta `zh: en` .

* [lambar gaban-karshen](https://github.com/xxai-art/web)
* [Fakitin harshe don rukunin yanar gizon gaba ɗaya](https://github.com/xxai-art/web/tree/main/i18n)
* [Fakitin harshe don tsarin shiga](https://github.com/wacpkg/user/tree/main/ui.i18n)
* [Takardun Harsuna da yawa na Yanar Gizo](https://github.com/xxai-doc)

Harshen shirye-shiryen gaba-gaba shine [@w5/coffee_plus](http://npmjs.com/@w5/coffee_plus) , wanda ke ƙara wasu fasalulluka dangane da rubutun rubutun kofi, duba [./coffee_plus.md](./coffee_plus.md) .

## Ƙasashen waje na gidajen yanar gizo da takardu

Gina akan ayyuka 3 masu zuwa

* [@w5/mdt](https://www.npmjs.com/package/@w5/mdt)

  Ƙaƙwalwar ita ce `.mdt` , za ku iya amfani da tsarin daidaitawa mai kama da `<+ ./coffee_plus/import.js>` don komawa zuwa fayilolin waje, da kuma samar da alamar alama tare da suffix `.md` .

* [@w5/trmd](https://www.npmjs.com/package/@w5/trmd)

  Fassarar Markdown ba za ta fassara lambobi da hanyoyin haɗin gwiwa ba, kuma za ta adana jumlolin da aka fassara. Idan an canza fassarar amma ba a gyara ainihin rubutun ba, sake aiwatar da shi ba zai sake rubuta canjin fassarar ba.

* [@w5/i18n](https://www.npmjs.com/package/@w5/i18n)

  Fayilolin harshe don fassarar `yaml` da aka samar da gidajen yanar gizo.

### Umurnin Fassara Takardun Aiki Aiki

Duba wurin ajiyar lamba [xxai-art/doc](https://github.com/xxai-art/doc)

Ana ba da shawarar shigar da nodejs, [direnv](https://direnv.net) , [bun](https://github.com/oven-sh/bun) farko, sannan `direnv allow` bayan shigar da directory ( [.envrc](https://github.com/xxai-art/doc/blob/main/.envrc) za a kashe ta atomatik bayan shigar da directory).

Don guje wa babban tushen lambar da aka fassara zuwa ɗaruruwan harsuna, na ƙirƙiri tushen lambar tushe daban don kowane harshe kuma na ƙirƙiri ƙungiya don adana tushen lambar.

Saita canjin yanayi `GITHUB_ACCESS_TOKEN` sannan gudanar da [create.github.coffee](https://github.com/xxai-art/doc/blob/main/create.github.coffee) zai ƙirƙiri ma'ajiyar lambar ta atomatik.

Tabbas, zaku iya sanya shi a cikin tushen lambar.

Maganar rubutun fassarar [run.sh](https://github.com/xxai-art/doc/blob/main/run.sh)

An fassara lambar rubutun kamar haka:

[bunx](https://bun.sh/docs/cli/bunx) shine maye gurbin npx, wanda ya fi sauri. Tabbas, idan ba a shigar da bun ba, zaku iya amfani da `npx` maimakon.

`bunx mdt zh` renders `.mdt` a cikin zh directory as `.md` , duba 2 nasaba fayiloli a kasa

* [kofi_plus.mdt](https://github.com/xxai-doc/zh/blob/main/coffee_plus.mdt)
* [kofi_plus.md](https://github.com/xxai-doc/zh/blob/main/coffee_plus.md)

`bunx i18n` shine ainihin lambar don fassarar (idan kawai an shigar da `nodejs` , amma `bun` da `direnv` ba a sanya su ba, kuna iya gudu `npx i18n` don fassarawa).

Za a yi la'akari da [i18n.yml](https://github.com/xxai-art/doc/blob/main/i18n.yml) , daidaitawar `i18n.yml` a cikin wannan takarda shine kamar haka:

```
en:
zh: ja ko en
```

Ma'anar ita ce: Fassarar Sinanci zuwa Jafananci, Koriya, Turanci, fassarar Turanci zuwa duk sauran harsuna. Idan kuna son tallafawa Sinanci da Ingilishi kawai, kuna iya rubuta `zh: en` .

Na ƙarshe shine [gen.README.coffee](https://github.com/xxai-art/doc/blob/main/gen.README.coffee) , wanda ke fitar da abun ciki tsakanin babban take da farkon taken kowane harshe `README.md` don samar da shigarwa `README.md` . Lambar tana da sauqi qwarai, zaku iya kallon ta da kanku.

Ana amfani da Google API don fassarar kyauta. Idan ba za ku iya shiga Google ba, da fatan za a saita ku saita wakili, kamar:

```
export https_proxy=http://127.0.0.1:7890 http_proxy=http://127.0.0.1:7890 all_proxy=socks5://127.0.0.1:7890
```

Rubutun fassarar zai haifar da ma'ajin da aka fassara a cikin `.i18n` directory, da fatan za a duba shi tare da `git status` kuma ƙara shi zuwa wurin ajiyar lambar don guje wa maimaita fassarar.

Da fatan za a gudanar da `bunx i18n` duk lokacin da kuka canza fassarar don sabunta cache.

Idan an canza ainihin rubutun da fassarar lokaci guda, cache ɗin zai rikice, don haka idan kuna son gyarawa, zaku iya gyara ɗaya kawai, sannan ku kunna `bunx i18n` don sabunta cache ɗin.
