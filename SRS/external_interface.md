

# Ytri tenging (External interface)

Lýsing á tengingu milli hugbúnaðarkerfisins og notanda, annars hugbúnaðar, vélbúnaðar eða samskiptakerfis.


<!--

Afritið sniðmátið hér fyrir neðan fyrir hverja kröfu og gefið henni auðkenni 

## UI-1

## 🔌 Skil
> Við hvern eða hvað hefur kerfið samskipti?

## 📥 Inntak / úttak
> Hvaða gögn, skipanir eða merki fara milli kerfisins og ytri aðilans?

## 📚 Samskipti og staðlar
> Hvernig fara samskiptin fram? Eru tiltekin snið, samskiptareglur eða staðlar notaðir?

 ## 📌 Tegund skila
- [x ] Notendaviðmót (User interface)
- [ ] Hugbúnaðarviðmót (Software interface)
- [ ] Vélbúnaðarviðmót (Hardware interface)
- [ ] Samskiptaviðmót (Communications interface)
-->
## UI-1: Tilkynningaþjónusta (Push Notifications)

## 🔌 Skil
> Samskipti milli **Vaktarinnar** og ytri tilkynningaþjónustu (t.d. Firebase Cloud Messaging / Apple Push Notification service) til að senda rauntímatilkynningar í snjallsíma notenda.

## 📥 Inntak / úttak
> **Inntak:** Staðfesting frá þjónustu um að skilaboð hafi borist tæki (e. delivery status).  
> **Úttak:** Tilkynningaskilaboð (fyrirsögn, texti, notenda-ID) og gagnafarmur (payload) sem bendir á ákveðna vakt eða beiðni í appinu.

## 📚 Samskipti og staðlar
> Samskipti fara fram gegnum öruggt REST API ytri þjónustunnar með JSON gagnaformi yfir HTTPS (TLS 1.3). Auðkenning fer fram með API-lyklum eða OAuth 2.0 táknum (tokens).

## 📌 Tegund skila
- [ ] Notendaviðmót (User interface)
- [x] Hugbúnaðarviðmót (Software interface)
- [ ] Vélbúnaðarviðmót (Hardware interface)
- [x] Samskiptaviðmót (Communications interface)


## UI-2: Útflutningur á vaktagögnum til launakerfa

## 🔌 Skil
> Samskipti milli **Vaktarinnar** og ytri launakerfa (t.d. DK, Payday eða bókhaldskerfa) fyrir lokauppgjör á unnum vöktum og vaktaskiptum.

## 📥 Inntak / úttak
> **Inntak:** Svörun frá launakerfi um hvort móttaka á vaktaskrá hafi heppnast (status codes, villumillur).  
> **Úttak:** Skrá eða API-skeyti sem inniheldur kennitölur starfsmanna, dagsetningar, vinnutíma (upphaf/endir), tegund vaktar og samþykkt vaktaskipti á valdu tímabili.

## 📚 Samskipti og staðlar
> Gagnaflutningur fer fram annaðhvort með niðurhali á stöðluðum CSV/Excel skrám eða með beinum köllum í REST API launakerfisins yfir HTTPS. Gögn fylgja stöðluðu UTF-8 textasniði.

## 📌 Tegund skila
- [ ] Notendaviðmót (User interface)
- [x] Hugbúnaðarviðmót (Software interface)
- [ ] Vélbúnaðarviðmót (Hardware interface)
- [ ] Samskiptaviðmót (Communications interface)
