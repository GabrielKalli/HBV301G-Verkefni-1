# 📦 Verkefni #1 - Tegundir krafna og samhengi 

<!-- Fyllið inn í þessa kafla áður en verkefninu er skilað 

Heiti kerfis: 
Höfundar: Nöfn nemenda 
Stutt lýsing á kerfinu
Stutt lýsing á innihaldi geymslunnar. 
    - Lesendur eru viðskiptavinir og kaupendur, notendur, kerfishönnuðir, forritarar og prófarar. Einnig verkefnisstjórar og viðhaldsteymi. 

Annars ráðið þið hvernig þið viljið lýsa geymslunni eða ná til lesenda 
-->

<!-- Nemendur fjarlægi eftirfarandi eða setji sem comment áður en verkefni er skilað 
-->

## Geymslan er í fjórum hlutum
- README, þessi skrá
- SRS - Software Requirement Specifications
- SDS - System Description Specification 
- Vinnuferli 
    - Hópavinna og geymsla
    - Verkaskipting
    - Ígrundun
    - Gagnsæisyfirlýsing um notkun gervigreindar

## Sniðmát fyrir kröfutegundir 

Hver kröfutegund hefur sér xxx.md skrá, t.d. business_requirements.md, undir SRS möppunni. Í skránni er sniðmát fyrir lýsingu á einni kröfu. Afritið nýtt sniðmát fyrir hverja kröfu og fyllið inn í. 

## Leiðbeiningar fyrir Template  
Þessi geymsla er sniðmát fyrir verkefni 1 í námskeiðinu **HBV301G Verkfræði kröfugreiningar**. 

## Uppsetning 

Annar nemandinn í teyminu:
1. Ýtir á **Use this template** og býr til nýtt repository fyrir verkefnið.
2. Býr til **Project** sem tengist repository-inu og setur það upp sem **Kanban-borð**.
3. Bætir félaga sínum við sem **collaborator** bæði í repository-inu og Project-inu.

Báðir nemendur: 

4. **Clone-a repository-ið á sína tölvu** og opna það í því þróunarumhverfi/editor sem þeir ætla að nota.
 
Að því loknu eruð þið bæði með aðgang að sama repository og getið unnið með það bæði á GitHub og local.


## Leiðbeiningar fyrir vinnu við verkefnið á Github

Vinnulagið fyrir verkefnið er eftirfarandi, sem er útskýrt nánar hér á eftir. Þið getið unnið allt á GitHub (remote) eða unnið mest af vinnunni í IDE/skel eða öðrum editor og skel (local) og á GitHub (remote)

**Task/Issue (GitHub) → Create a branch (GitHub) → vinna/commits/push (local) → Pull Request (PR) (GitHub) → review (GitHub) → merge (GitHub) → issue lokast → pull á main (local)**
Eftir merge má eyða vinnubranchinum á GitHub og local. Ef eyddur remote branch sést enn í local má nota git fetch --prune.

Farðu eftir eftirfarandi vinnulagi til að vinna SRS hlutann 
- Búðu til nýtt **Issue**, t.d. "skrá viðskiptakröfur",  fyrir verkið sem á að vinna og úthlutaðu því á annan hvorn teymismeðliminn. Þegar issue-ið er búið til fær það númer, t.d. **#12**.
- Settu issue-ið í réttan dálk á **Kanban-borði** verkefnisins.
- Farðu í issue-ið (**#12**) á GitHub og veldu **Create a branch** undir *Development*.
  Þannig tengist branch-ið sjálfkrafa við issue-ið.
- Vinna skal verkið á branch-inu. Lýstu kröfum í viðeigandi kröfuskrá samkvæmt sniðmáti.
- Þegar þú bætir við  kröfu skaltu bæta henni við **SRS.md** og vísa þar í kröfuna/kröfurnar í kröfuskránni.
- Gerðu **commit og push** reglulega
- Stofnaðu **Pull Request (PR)** á GitHub þegar breytingarnar eru tilbúnar fyrir rýni og skrifaðu `Closes #12` í lýsingu PR svo issue **#12** lokist sjálfkrafa þegar PR-ið er sameinað við `main`.
- Teymisfélaginn rýnir PR-ið og samþykkir það (**Approve**). Að rýni lokinni er PR-ið sameinað (**merge**) við `main` og issue-inu lokað sjálfkrafa.

### Rýni á Pull Request

**Höfundur breytinga**

Í lýsingu PR skaltu biðja teymisfélaga um að rýna sérstaklega hvort:
- kröfurnar séu af réttri kröfutegund,
- kröfurnar séu skýrar og ótvíræðar,
- viðeigandi sniðmáti sé fylgt,
- auðkenni og tengingar við aðrar kröfur séu réttar.

**Rýnandi**
- Rýndu breytingarnar og skráðu athugasemdir (*comments*) í PR eftir þörfum. Þegar þú ert tilbúin/n að samþykkja breytingarnar skaltu velja **Approve**.

Að lokinni rýni sameinar höfundur PR-ið (**merge**) við `main`.

Ljúktu við aðra þætti verkefnisins eins og SDS og Vinnuferlið með sambærilegum hætti, þ.e. að skipta með ykkur verkum með issues, branches og PR 
