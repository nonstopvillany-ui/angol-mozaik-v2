# Angol Mozaik AI V2 – 14 leckés változat

## Tananyag
A New Headway Elementary Student’s Book (Third Edition) 14 egységének témaköreit követő **saját készítésű** szókincs, magyar nyelvtani magyarázat és minden leckéhez 4 eredeti mondat, 4 interaktív feladattípusban, valamint nyomtatható gyakorlólap. A „Tankönyv / Workbook” menüben minden egységhez áttekintés és munkafüzetszerű saját gyakorlás található. A teljes Oxford PDF-eket a csomag **nem tartalmazza**; nyilvános közzétételükhöz kiadói engedély szükséges.

## Diák és tanár
A diák a „Tanár meghívása” gombbal videóhívást indít és a tanári linket a vágólapra másolja. A tanár a linkkel az alkalmazás tanári nézetét nyitja meg, amelyben a Jitsi videóhívás és az élő feladateredmények láthatók. A diák „Képernyő megosztása” gombja a Jitsi képernyőmegosztását kezdeményezi; a Chrome megosztási ablakában az Angol Mozaik lapot kell kiválasztani. A Jitsi szolgáltatója bejelentkezést kérhet, és korlátozhatja a beágyazást.

A feladatállapotot a Node szerver memóriában tárolja (4 órás lejárat, legfeljebb 100 esemény/szoba); Render újraindításakor törlődik. Ez demó, nem hitelesített tanári rendszer: aki ismeri a meghívólinket, láthatja a feladateredményeket. Személyes adatot ne küldjön a diák a feladatmezőkbe. Az óratörténet továbbra is a böngészőben tárolódik.

## Telepítés
GitHub repó gyökerébe töltsd fel a ZIP **tartalmát** (README.md, package.json, server.js, public/), Render automatikusan újratelepíti. Node indítás: `npm start`. A korábbi szerveroldali OpenAI-funkcióhoz az `OPENAI_API_KEY` Render környezeti változó szükséges.

## Ellenőrzés
1. Nyisd meg az oldalt, válassz a 14 leckéből.
2. Diák: Tanár meghívása → tanári link másolása.
3. Tanár: link megnyitása egy másik böngészőben vagy eszközön.
4. Diák: Képernyő megosztása → Chrome-lap → Angol Mozaik → Megosztás.
5. Diák: oldj meg feladatot; a tanári élő feladatkövetés 2 másodpercenként frissül.


## Interaktív munkafüzet
A `public/workbook.html` a felhasználó által feltöltött 14 leckés interaktív munkafüzetből integrált oldal. A főmenü `Interaktív munkafüzet` pontjából érhető el, és a főoldalon kiválasztott leckére vált. A munkafüzet eredeti PDF-mellékletei nem kerültek a nyilvános csomagba. Az eredmények böngészőnként, localStorage-ban tárolódnak.
