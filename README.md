# Angol Mozaik AI V2

Új, különálló webalkalmazás a korábbi Angol Mozaik helyett. A régi alkalmazást nem módosítja.

## Funkciók
- Szókincs, nyelvtan, mozaik, hiányzó szó, feleletválasztós, fordítás, brit angol felolvasás
- Óraszámláló, óraszorszám, korábbi órák és nyomtatható gyakorlólap (helyi böngészőmentés)
- **Valódi videóhívás** a Jitsi Meet szolgáltatáson keresztül: videóhívás gomb, véletlen szoba, link másolása. A Jitsi különálló külső szolgáltatás; internet, kamera/mikrofon-engedély és a szolgáltató elérhetősége szükséges. A publikus meet.jit.si használatát a szolgáltató korlátozhatja vagy bejelentkezéshez kötheti.
- AI mondatgenerálás és magyar nyelvtani magyarázat OpenAI API-n keresztül (kulcs csak szerveren)

## GitHub és Render telepítés
1. Hozd létre / nyisd meg a **nonstopvillany-ui/angol-mozaik-v2** repót.
2. A ZIP tartalmát (a fájlokat és a `public` mappát) töltsd fel a repó gyökerébe. **Ne** a ZIP fájlt töltsd fel egyben.
3. Render → New → Web Service → GitHub repo: `angol-mozaik-v2`.
4. Runtime: Node; Build command: `npm install`; Start command: `npm start`.
5. Environment → add `OPENAI_API_KEY` = saját titkos API-kulcs, és opcionálisan `OPENAI_MODEL` = `gpt-4o-mini`. A kulcsot soha ne töltsd fel GitHubra.
6. Deploy. A videóhívás a Jitsi külső szolgáltatásán fut; az AI az OpenAI API-val külön díjas.

## Helyi teszt
`npm start`, majd `http://localhost:3000`.

## Korlátok és további feladatok
- A demó tananyag **3 saját példaleckét** tartalmaz; a teljes tankönyv nincs integrálva.
- A **Kreatív angol kezdő könyv PDF-jét szándékosan nem tartalmazza** a nyilvános GitHub-csomag, mert a közzétételhez engedély szükséges.
- Az óratörténet böngészőnként külön, `localStorage`-ban tárolódik, nem többfelhasználós felhőadatbázisban.
- A Jitsi hívás működhet, de a tanár **nem látja automatikusan a diák feladatmegoldásait**; ehhez külön valós idejű backend szükséges.
- Nyilvános AI szolgáltatáshoz bejelentkezés, jogosultságok és felhasználónkénti költségkorlát szükséges. A beépített egyszerű IP-alapú limit nem helyettesíti ezeket.
- Éles oktatási szolgáltatáshoz adatvédelmi tájékoztató és a videó/AI szolgáltatók adatkezelésének ellenőrzése szükséges.
