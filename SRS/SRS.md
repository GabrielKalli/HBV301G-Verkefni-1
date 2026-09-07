# 📄 Software Requirements Specification (SRS)

## 1. Inngangur
### 1.1 Tilgangur
**Vaktin** er stafrænt vaktaskipta- og afleysingakerfi sem leysir óreiðu í vaktavinnu með því að færa samskipti og samþykki úr óformlegum skilaboðahópum yfir á einn miðlægan vettvang.

### Tilgangur kerfisins
* **Sjálfvirknivæða vaktaskipti:** Gera starfsfólki kleift að skipta á vöktum og taka að sér afleysingar með auðveldum hætti í snjallsíma.
* **Létta álagi af vaktstjórum:** Fækka handvirkum skráningum og stytta tímann sem fer í að manna lausar vaktir vegna forfalla.
* **Tryggja regluvörslu:** Koma í veg fyrir tvíbókanir og tryggja að vaktaskipti stangist ekki á við kjarasamninga (t.d. lágmarkshvíldartíma).

### Hverju kerfið á að skila (Deliverables)
1. **Snjallsímaappa- / Vefviðmót fyrir starfsfólk:**
   * Persónulegt yfirlit yfir eigin vaktir.
   * Einfalt ferli til að leggja út vaktir í skipti eða taka að sér lausar vaktir.
   * Rauntímatilkynningar (push notifications) um nýjar eða lausar vaktir.
2. **Stjórnendaviðmót fyrir vakt- og rekstrarstjóra:**
   * Yfirlit yfir mönnunarstöðu vinnustaðarins í rauntíma.
   * Einn staður til að samþykkja eða hafna vaktaskiptum með einum smelli.
   * Stillingar á innri reglum (t.d. réttindum starfsmanna og hvíldartíma).
3. **Gagnatengingar og útflutningur:**
   * Innflutningur á tilbúnum vaktaplónum (Excel/CSV eða API).
   * Útflutningur á staðfestum vaktaskiptum yfir í launakerfi.

### 1.2 Umfang og mörk kerfisins

### 1. Innan marka kerfisins (In Scope)
* **Umsýsla vaktaskipta og afleysinga:** Ferli þar sem starfsfólk setur vaktir í skipti, sækir um lausar vaktir og tekur að sér afleysingar.
* **Samþykktarferli stjórnenda:** Viðmót fyrir vaktstjóra til að fara yfir, samþykkja eða hafna breytingum á vaktaplani.
* **Sjálfvirk regluelding (Validation):** Athugun á því hvort vaktaskipti stangist á við kjarasamninga (t.d. lágmarkshvíld) eða innri reglur vinnustaðarins.
* **Tilkynningastjórnun:** Útsending rauntímatilkynninga í síma notenda þegar vaktir losna eða beiðnir eru samþykktar.
* **Mönnunaryfirlit:** Rauntímayfirlit fyrir vaktstjóra yfir mannahald og ómannaðar vaktir.

### 2. Utan marka kerfisins (Out of Scope)
* **Upphafleg vaktaplangerð:** Kerfið býr ekki til vaktaplön frá grunni heldur móttekur tilbúin plön úr ytri kerfum.
* **Launavinnsla:** Engir útreikningar á lokalaunum, sköttum eða lífeyri fara fram í kerfinu.
* **Viðverustimplun (Clock-in / Clock-out):** Ekkert mætingareftirlit eða stimplunarklukka á vinnustað.
* **Samskiptaspjall (In-app Chat):** Engin frjáls textaskilaboð milli starfsmanna til að koma í veg fyrir óreiðu.

---

### 3. Helstu samskipti við umhverfið

| Ytri aðili / Kerfi | Tegund samskipta | Lýsing á samskiptum |
| :--- | :--- | :--- |
| **Starfsfólk** | Inntak / Úttak | Senda inn óskir um skipti, taka að sér vaktir og fá tilkynningar í snjallsíma. |
| **Vaktstjórar** | Inntak / Úttak | Fara yfir og samþykkja/hafna skiptum; fylgjast með mönnunarstöðu. |
| **Ytra vaktaplankerfi** | Inntak (Import) | Sækir tilbúið vaktaplan og starfsmannalista (t.d. úr Excel/CSV eða API). |
| **Tilkynningaþjónusta** | Úttak (Integration) | Sendir rauntímatilkynningar (Push Notifications / SMS) í gegnum ytri þjónustu (t.d. Firebase). |
| **Launakerfi** | Úttak (Export) | Skilar staðfestum gögnum um samþykkt vaktaskipti í lok tímabils yfir í launakerfi (t.d. DK/Payday). |
### 1.3 Skilgreiningar
| Hugtak | Skýring |
|--------|---------|
| SRS | Software Requirements Specification |


### 1.4 Tilvísanir
- ISO/IEC/IEEE International Standard - Systems and software engineering -- Life cycle processes -- Requirements engineering," in ISO/IEC/IEEE 29148:2018(E) , vol., no., pp.1-104, 30 Nov. 2018, doi: 10.1109/IEEESTD.2018.8559686.ISO/IEC/IEEE 29

---

## 2. Almenn lýsing
### 2.1 Notendahópar
Notendahópum kerfisins **Vaktin** er skipt í tvo meginflokka: **Beinir notendur** (þeir sem nota viðmót kerfisins daglega) og **Óbeinir notendur/Hagsmunaaðilar** (þeir sem nýta gögnin eða verða fyrir áhrifum af virkni þess).

---

### 1. Beinir notendur (Direct Users)

#### A. Starfsfólk / Vaktamenn (Almennir notendur)
* **Hverjir þetta eru:** Starfsmenn í vaktavinnu (t.d. þjónar, barþjónar, afgreiðslufólk eða eldhússtarfsfólk) sem vinna samkvæmt breytilegu vaktaplani.
* **Markmið og þarfir:**
  * Fá skýra yfirsýn yfir eigin vaktir í snjallsíma.
  * Geta sett vaktir í skipti eða fengið afleysingu á einfaldan hátt án þess að senda skilaboð í stóra spjallhópa.
  * Taka að sér aukavaktir/lausar vaktir til að auka tekjur eða vinnutíma.
* **Tæknileg færni:** Yfirleitt vön almennri snjallsímanotkun (öppum eins og Messenger, Instagram o.fl.) og ætlast til þess að ferlið taki aðeins nokkra smelli.

#### B. Vakt- og rekstrarstjórar (Stjórnendur)
* **Hverjir þetta megin eru:** Deildarstjórar, vaktstjórar eða rekstraraðilar sem bera ábyrgð á daglegu mannahaldi og að vaktir séu fullmannaðar.
* **Markmið og þarfir:**
  * Fara yfir, samþykkja eða hafna óskum um vaktaskipti á einum miðlægum stað.
  * Fá rauntímayfirlit yfir mannanarstöðuna (e. coverage) og sjá strax ef eyður myndast á vaktaplani.
  * Tryggja að vaktaskipti stangist ekki á við reglur um hvíldartíma eða sérfræðikröfur á vaktinni.
* **Tæknileg færni:** Meðalnotendur á tölvur og snjalltæki; þurfa skýrt og skilvirkt stjórnendaviðmót (dashboard) sem sparar þeim tíma í daglegum rekstri.

---

### 2. Óbeinir notendur og hagsmunaaðilar (Indirect Stakeholders)

#### C. Eigendur / Framkvæmdastjórar
* **Hverjir þetta eru:** Ákvarðanatökumenn sem bera heildarábyrgð á rekstrinum og fjármálum fyrirtækisins.
* **Markmið og þarfir:**
  * Lágmarka yfirvinnualag og óþarfa launakostnað sem hlýst af lélegu skipulagi eða tvíbókunum.
  * Auka ánægju og halda í starfsfólk með því að bjóða upp á nútímalegt og sveigjanlegt vinnuumhverfi.

#### D. Launadeild / Bókarar
* **Hverjir þetta eru:** Starfsfólk sem sér um launavinnslu í lok hvers mánaðar.
* **Markmið og þarfir:**
  * Fá rétt og staðfest gögn um hver vann hvaða vakt í lok uppgjörstímabils til að forðast launaskekkjur.
### 2.2 Viðskiptaávinningur
Innleiðing á kerfinu **Vaktin** skilar mælanlegum ávinningi bæði fyrir rekstur fyrirtækja og daglega upplifun starfsfólks.

---

### 1. Ávinningur fyrir fyrirtæki og rekstraraðila

* **Tímasparnaður stjórnenda:** Dregur úr þeim tíma sem vaktstjórar eyða í að handskrá breytingar, svara skilaboðum í ólíkum spjallhópum og leita að afleysingafólki á síðustu stundu.
* **Lægri launakostnaður og færri mistök:** Vegna sjálfvirkrar regluvörslu minnka líkur á ótilgreindri yfirvinnu, tvíbókunum og mannlegum mistökum við skráningu á unnum vöktum.
* **Betri nýting á mannafla:** Auðveldar að manna lausar vaktir með stuttum fyrirvara með því að senda rauntímatilkynningar á allt tiltækt og hæft starfsfólk í einu.
* **Aukið rekstraröryggi:** Stjórnendur hafa fulla rauntímayfirsýn yfir mönnunarstöðuna og vita alltaf með bizonysoðum hver ber ábyrgð á hverri vakt.
* **Bætt varðveisluhlutfall starfsfólks (Retention):** Nútímalegt og sveigjanlegt vinnuumhverfi eykur ánægju starfsmanna, sem dregur úr starfsmannaveltu og þjálfunarkostnaði.

---

### 2. Ávinningur fyrir starfsfólk (Notendur)

* **Aukið sjálfstæði og sveigjanleiki:** Starfsfólk getur stýrt sínum eigin vinnutíma, lagt út vaktir og óskað eftir skiptum hvenær sem er milliliðalaust í snjallsíma.
* **Aukin tekjumöguleikar:** Auðvelt er að fylgjast með lausum aukavöktum sem aðrir starfsmenn geta ekki unnið og taka þær að sér með einum smelli.
* **Skýrari ábyrgð og öryggi:** Þegar vaktaskipti eru samþykkt af vaktstjóra í kerfinu færist ábyrgðin opinberlega yfir á nýja starfsmanninn, sem eyðir óvissu.
* **Færri truflanir á frítíma:** Starfsfólk sleppur við stöðugar tilkynningar úr stórum skilaboðahópum (t.d. Messenger) og fær aðeins tilkynningar sem koma þeim við.

---

## 3. Kröfur fyrir kerfið

### 3.1 Viðskiptakröfur
| ID                                        | Titill                    |
|-------------------------------------------|---------------------------|
| [BREQ-1](business_requirements.md#breq-1) | Draga úr óvissu og mistökum við vaktaskipti |
| [BREQ-2](business_requirements.md#breq-2) | Einfalda umsýslu vaktaplans og afleysinga |

### 3.2 Kerfiskrafa
| ID                              | Titill                 |
|---------------------------------|------------------------|
| [SR-1](system_requirement.md#sr-1) | Miðlæg umsýsla vaktaplans og afleysinga |

### 3.3 Eiginleikar (Features)
| ID                     | Titill                 |
|------------------------|------------------------|
| [F-1](feature.md#f-1)  | Vaktaskipti og afleysingar  |
| [F-2](feature.md#f-2)  | Samþykki vaktaskipta og afleysinga  |
| [F-3](feature.md#f-3)  | Vaktaplan og tilkynningar  |

### 3.4 Notendakröfur
| ID                                   | Titill                  | Eiginleiki |
|--------------------------------------|-------------------------|------------|
| [UR-1](user_requirement.md#ur-1)     | Óska eftir afleysingu         | F-1        |
| [UR-2](user_requirement.md#ur-2)     | Taka lausa vakt               | F-1        |
| [UR-3](user_requirement.md#ur-3)     | Skoða beiðnir                 | F-2        |
| [UR-4](user_requirement.md#ur-4)     | Samþykkja eða hafna beiðnum   | F-2        |
| [UR-5](user_requirement.md#ur-5)     | Skoða uppfært vaktaplan       | F-3        |
| [UR-6](user_requirement.md#ur-6)     | Fá tilkynningar um breytingar | F-3        |

### 3.5 Virknikröfur

| ID | Titill | Notendakrafa |
|---|---|---|
| [FR-1](functional_requirement.md#fr-1) | Velja vakt í afleysingu | UR-1 |
| [FR-2](functional_requirement.md#fr-2) | Senda beiðni um afleysingu | UR-1 |
| [FR-3](functional_requirement.md#fr-3) | Skoða stöðu beiðni | UR-1 |
| [FR-4](functional_requirement.md#fr-4) | Skoða lausar vaktir | UR-2 |
| [FR-5](functional_requirement.md#fr-5) | Óska eftir að taka vakt | UR-2 |
| [FR-6](functional_requirement.md#fr-6) | Athuga skilyrði fyrir vakt | UR-2 |
| [FR-7](functional_requirement.md#fr-7) | Skoða óafgreiddar beiðnir | UR-3 |
| [FR-8](functional_requirement.md#fr-8) | Skoða upplýsingar um beiðni | UR-3 |
| [FR-9](functional_requirement.md#fr-9) | Skoða stöðu beiðna | UR-3 |
| [FR-10](functional_requirement.md#fr-10) | Samþykkja beiðni | UR-4 |
| [FR-11](functional_requirement.md#fr-11) | Hafna beiðni | UR-4 |
| [FR-12](functional_requirement.md#fr-12) | Uppfæra ábyrgð á vakt | UR-4 |
| [FR-13](functional_requirement.md#fr-13) | Skoða vaktaplan | UR-5 |
| [FR-14](functional_requirement.md#fr-14) | Skoða ábyrgð á vöktum | UR-5 |
| [FR-15](functional_requirement.md#fr-15) | Uppfæra vaktaplan | UR-5 |
| [FR-16](functional_requirement.md#fr-16) | Tilkynna niðurstöðu beiðni | UR-6 |
| [FR-17](functional_requirement.md#fr-17) | Tilkynna nýja beiðni | UR-6 |
| [FR-18](functional_requirement.md#fr-18) | Tilkynna breytingu á vakt | UR-6 |

### 3.6 Viðskiptareglur
| ID                                  | Titill                     |
|-------------------------------------|----------------------------|
| [BRG-1](business_rule.md#brg-1)     | Samþykki vaktaskipta       |
| [BRG-2](business_rule.md#brg-2)     | Hæfniskröfur fyrir vaktir  |

### 3.7 Gæðaeiginleikar
| ID                                      | Titill                     |
|-----------------------------------------|----------------------------|
| [QA-1](quality_attribute.md#qa-1)       | [Gæðaeiginleiki, titill]   |
| [QA-2](quality_attribute.md#qa-2)       | [Gæðaeiginleiki, titill]   |

### 3.8 Takmarkanir
| ID                              | Titill                |
|---------------------------------|-----------------------|
| [C-1](constraint.md#c-1)        | [Takmörkun, titill]   |
| [C-2](constraint.md#c-2)        | [Takmörkun, titill]   |

### 3.9 Ytri skil (Interfaces)
| ID                                      | Titill                |
|-----------------------------------------|-----------------------|
| [UI-1](external_interface.md#ui-1)      | [Ytri skil, titill]   |
| [UI-2](external_interface.md#ui-2)      | [Ytri skil, titill]   |

---

## 4. Viðaukar
### 4.1 Orðalisti
- Skilgreina lykilhugtök.

  | Hugtak | Skilgreining |
  |--------|--------------|
  |        |              |
  |        |              |

### 4.2 Samþykktir
- Kennari: ____________________  
- Nemandi: ____________________
