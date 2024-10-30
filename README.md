# IndexNow Plugin Pro Seznam.cz

IndexNow Plugin Pro Seznam.cz umožňuje automaticky posílat URL nových, nebo upravených článků ve Wordpressu přímo do IndexNow na search.seznam.cz. Nepotřebujete web nijak ověřovat, ani registrovat.
Jakmile plugin nainstalujete a aktivujete, tak automaticky vytvoří API klíč a ověřovací soubor v kořenovém adresáři webu.
Plugin detekuje vytvoření, aktualizaci a smazání stránek a příspěvků ve Wordpressu a automaticky je na pozadí pošle do search.seznam.cz. To pomůže stránku ihned crawlovat vyhledávačem Seznam.cz a stránku případně indexovat, nebo deindexovat. Plugin využívá URL endpointu `https://search.seznam.cz/indexnow`. Tyto URL už dále mohou a nemusí být sdíleny s jinými vyhledávači sdílejícími protokol IndexNow.
Tento plugin vznikl jako tzv. fork (vychází z kódu jiného pluginu) z pluginu IndexNow od týmu Bing Webmaster, který naleznete na `https://wordpress.org/plugins/indexnow/` v rámci GPLv2.
Kód tohoto pluginu naleznete na GitHubu `https://github.com/neologyc/IndexNowForSearchSeznamCZ`.

Některé funkcionality:

- Možnost vypnout (defaultně zapnuto) automatické odesílání Url
- Možnost manuálního vložení jedné a více URL do IndexNow
- Tabulka se seznamem posledních 100 odeslaných URL a stavem odeslání
- Možnost znovu poslat URL, která nebyla odeslána kvůli chyby
- Možnost exportu seznamu odeslaných (i s chybou) URL pro další analýzy

Originální plugin jsem upravil takto:

- změnil jsem endpoint IndexNow na `https://search.seznam.cz/indexnow`, aby se vaše nové/upravené/smazané URL dostaly rovnou do Seznamu a co nejrychleji se zaindexovaly
- změnil jsem počet posledních odeslaných URL z 20 na 100
- drobně jsem upravil název pluginu, jeho náhledový obrázek a pár dalších drobností, aby bylo jasné, že URL odesílá jen do Seznam.cz
- částečný překlad do češtiny

## Instalace pluginu

Je to jednoduché:

- Přihlas se do administrace WP a klikni na `Pluginy > Přidat nový`.
- Najdi plugin `IndexNow Plugin` a klikni na tlačítko `Nainstalovat`.
- Po úspěšné instalaci plugin aktivuj, aby se plugin zapnul. Stačí kliknout na `Aktivuj`.
- Jdi do stránky s nastavením `Nástroje > IndexNow Pro Seznam.cz` a klikni na `Let's Get Started!`

## FAQ - Často kladené dotazy

- Jak změním API klíč?

Nový API klíč se vytvoří po deaktivaci a opětovné aktivaci pluginu. Automaticky.

- Jak smažu data pluginu v databázi Wordpressu?

Stačí plugin deaktivovat a data v databázi Wordpressu budou automaticky smazány. Při další aktivaci pluginu budete začínat s čistým listem.


- Jak rychle Seznambot stránku projde?

Podle mých testů SeznamBot projde stránku do pár sekund od odeslání pomocí IndexNow. To je prakticky stejně rychlé jako používání API v Seznam Webmaster Tools.

- URL se odeslala, ale zatím ji nevidím v indexu?
Než se stránka dostane do indexu Seznamu může trvat déle (hodiny, ale spíše dny). Zároveň může být stránka buď neindexovatelná (nastavením v meta robots), nebo pro Seznam nezajímavá (málo obsahu, chyby, atp.) a proto ji nezaindexuje.


### 1.0.0

- První verze
