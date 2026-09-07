# 🧭 System Description Specification (SDS)

## Númer teymis og höfundar
Hópur 7, Edil Inga Kristjánsdóttir og Gabríel Orri Karlsson

## Heiti kerfis
Vaktin

## Hvað er kerfið?
Vaktin: Sveigjanlegt vaktaplan og afleysingakerfi

Hvað er kerfið?
Vaktin er stafræn lausn sem einfaldar alla umsjón með vaktaplónum, vaktaskiptum og afleysingum. Kerfið leysir óskilvirk samskipti í óformlegum skilaboðahópum með því að bjóða upp á miðlægan vettvang þar sem starfsfólk getur auðveldlega sett vaktir í skipti eða oskað eftir afleysingu og samstarfsfólk getur tekið að sér lausar vaktir. Kerfið sjálfvirkjar samþykkisferli vaktstjóra, heldur utan um réttindi starfsmanna og tryggir fulla yfirsýn yfir mannahald í rauntíma.

Fyrir hvern er kerfið?

- Starfsfólk í vaktavinnu: Fengið auðveldari leið til að stýra eigin vinnutíma, skipta á vöktum og taka að sér aukavaktir með örfáum smellum í símanum.

- Vakt- og rekstrarstjórar: Sparar tíma við að manna eyður á vaktaplaninu, heldur utan um samþykki á vaktaskiptum og komast hjá skörunum eða yfirvinnu.

- Fyrirtæki í vaktavinnugeiranum: Upphaflega hannað fyrir veitingastaði og verslanir þar sem mannahald breytist hratt, en uppbyggt þannig að það nýtist öllum fyrirtækjum með vaktakerfi (t.d. hótelum, heilbrigðisstofnunum og öryggisþjónustu).

## TilgangurMeginmarkmiðið er að eyða óreiðu í vaktaskiptum og koma á skilvirku, sjálfvirkara ferli sem sparar tíma hjá stjórnendum og eykur sveigjanleika hjá starfsfólki.

Vandamálin sem kerfið leysir

- Spjallhópaóreiða: Vaktaskipti fara oft fram í órekjanlegum skilaboðahópum (Messenger/WhatsApp), þar sem óskir gleymast eða valda ruglingi.

- Tímafrek umsýsla vaktstjóra: Stjórnendur eyða miklum tíma í að handskrá breytingar, samþykkja skipti í gegnum ólíka csamkiptaleiðir og leita að afleysingafólki þegar forföll verða með stuttum fyrirvara.

- Óskýr ábyrgð: Óvissa myndast um hver ber í raun ábyrgð á vaktinni ef skiptin hafa ekki verið skráð eða samþykkt með opinberum hætti.

Væntanlegur árangur

- Einfaldari ferlar: Starfsfólk getur óskað eftir skiptum eða tekið að sér lausar vaktir með nokkrum smellum í símanum.

- Full komin yfirsýn: Vaktstjórar sjá mönnunarstöðuna í rauntíma, fá viðvaranir um eyður á vaktaplaninu og geta samþykkt breytingar á einum stað.

- Styttur viðbragðstími: Lausar vaktir vegna veikinda eða forfalla mönnast mun hraðar með sjálfvirkum tilkynningum á tiltækt starfsfólk.

- Mikið tímasparnaður og fækkun mistaka: Dregur úr líkum á tvíbókunum, mönnunarskorti og yfirvinnualagskostnaði.

## Afmörkun (Scope)
**Innan scope:**
- Umsjón með vaktaskiptum: Notendur geta lagt út vaktir í skipti, valið óskir um skiptivaktir og tekið að sér lausar vaktir hjá samstarfsfólki.

- Samþykkisferli vaktstjóra: Vaktstjórar fá tilkynningar um vaktaskipti og geta samþykkt eða hafnað þeim á einum stað með einum smelli.

- Sjálfvirkar tilkynningar (Push Notifications): Rauntímatilkynningar sendar í síma þegar nýjar vaktir losna, þegar beiðni er samþykkt eða þegar breytingar verða á vaktaplani.

- Yfirsýn og mönnunarstaða: Vaktstjórar sjá lifandi stöðu á mönnun (e. coverage) og fá viðvaranir ef eyður eru á planinu eða ef forföll verða.

- Sveigjanlegar reglur (Stillingar): Möguleiki fyrir vaktstjóra að setja grunnreglur (t.d. lágmarkshvíld á milli vakta eða kröfur um ákveðna þjálfun/réttindi fyrir sérstakar vaktir).

- Persónulegt vaktaplan: Starfsfólk sér sína eigin dagskrá, framundan vaktir og sögu um skipti í persónulegu yfirliti.

**Utan scope:**
- Aðal-vaktaplangerð frá grunni: Kerfið er ekki ætlað til að búa til flókin upphafleg vaktaplön eða sjálfvirka gervigreindarhönnun á heildarvaktaplani (móttekur/flytur potþétt inn tilbúið plan).

- Launavinnslu- og stjórnunarkerfi: Kerfið reiknar ekki út lokalaun, skatta eða orlof, heldur sér aðeins um að halda utan um hver vinnur hvaða vakt.

- Viðverustimplun (Clock-in / Clock-out): Ekkert GPS- eða vélrænt mætingarkerfi á vinnustað (t.d. stika við dyrnar); kerfið snýst um skipulag og afleysingar, ekki rauntíma mætingareftirlit.

- Samskipta- eða spjallkerfi (In-app Chat): Engir frjálsir textaspjallþræðir milli starfsmanna til að koma í veg fyrir óreiðu; öll samskipti fara fram í gegnum stöðluð skiptiferli og hnappa.

## Samhengi kerfis (context) 
Í þessum hluta er gerð grein fyrir umhverfi kerfisins **Vaktin**, ytri kerfum sem það á í samskiptum við, hagsmunaaðilum og þeim ramma sem kerfið starfar innan.

---

**1. Samhengismynd (System Context Diagram)**

Eftirfarandi mynd sýnir mörk kerfisins (*System Boundary*) og hvernig ytri aðilar, kerfi og reglur tengjast því:

```text
               +----------------------------------+
               |     Lög & Kjarasamningar         |
               | (t.d. lágmarkshvíld, yfirvinna)  |
               +----------------------------------+
                                |
                                v
+-------------------+   +---------------+   +--------------------+
|  Starfsfólk       |--->|               |<---|  Vakt- &         |
|  (App notendur)   |   |    VAKTIN     |    |  Rekstrarstjórar  |
+-------------------+   |               |    +--------------------+
                        |  (System in   |
+-------------------+   |    Scope)     |    +--------------------+
| Ytra Vaktaplan    |--->|               |--->| Tilkynninga-       |
| (t.d. Excel/CSV)  |   +---------------+    | þjónusta (Push/SMS)|
+-------------------+            |           +--------------------+
                                 v
                        +-----------------+
                        |  Launakerfi     |
                        | (Útflutningur)  |
                        +-----------------+
```
- **Fólk og hagsmunaaðilar:** Hverjir hafa samskipti við kerfið eða hafa áhrif á það?
- **Ytri kerfi og þjónustur:** Hvaða önnur kerfi eða þjónustur hefur kerfið samskipti við?
- **Önnur atriði í umhverfinu:** Eru t.d. ferli, reglur eða skjöl sem hafa áhrif á kerfið?
- **Mörk kerfisins:** Hvað tilheyrir kerfinu og hvað tilheyrir samhengi þess?

## Tenging við SRS
- Sjá nánari kröfuskipan í [SRS](SRS/SRS.md) (viðskiptakröfur, fídusar, notendakröfur o.s.frv.).
