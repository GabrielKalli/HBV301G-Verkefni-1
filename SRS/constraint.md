# Takmörkun (Constraints)

Takmörkun sem þrengir valkosti hönnuða við gerð og þróun hugbúnaðarins.

<!--

Afritið sniðmátið hér fyrir neðan fyrir hverja kröfu og gefið henni auðkenni 

## C-1

## 🔒 Lýsing
> Hvaða takmörkun setur þetta á hönnun eða þróun hugbúnaðarins?

## 📝 Athugasemdir
> Tengsl við aðrar kröfur eða upplýsingar.

## 🎯 Áhrif á hönnun eða þróun

-->
## C-1: Stuðningur við snjallsíma (Mobile-First Constraints)

## 🔒 Lýsing
> Kerfið fyrir almenna notendur (starfsfólk) verður að vera hannað og þróað sem snjallsímaforrit (eða responsive vefapp sem virkar eins og snjallapp) þar sem megintilgangurinn er notkun í síma.

## 📝 Athugasemdir
> Tengist QA-1 (Nothæfi) og kröfum um rauntímatilkynningar. Notendur kerfisins eru á ferðinni og þurfa að geta brugðist hratt við vaktaskiptum án þess að sitja við tölvu.

## 🎯 Áhrif á hönnun eða þróun
> Þróunaraðilar þurfa að velja tækni sem styður þvert á stýrikerfi (iOS og Android), t.d. React Native, Flutter eða Progressive Web App (PWA). Hönnun á viðmóti (UI/UX) verður að miðast við smáa skjái, einfalda hönnun og snertivirkni (touch-friendly targets).


## C-2: Gagnatenging og innflutningur á vaktaplónum (Data Integration)

## 🔒 Lýsing
> Kerfið verður að geta flutt inn vaktaplön úr stöðluðum skrám (t.d. CSV eða Excel) þar sem kerfið mun ekki bjóða upp á að búa til upprunaleg vaktaplön frá grunni.

## 📝 Athugasemdir
> Tengist afmörkun kerfisins (Scope), þar sem upphafleg vaktaplangerð var skilgreind utan marka kerfisins.

## 🎯 Áhrif á hönnun eða þróun
> Hönnuðir og þróunaraðilar þurfa að búa til öfluga innflutningsvél (parser) sem getur tekið við ólíkum töflureiknasniðmátum og umbreytt þeim í innri gagnagrunnsgerð Vaktarinnar án þess að kerfið hrynji ef sniðið er óhefðbundið.
