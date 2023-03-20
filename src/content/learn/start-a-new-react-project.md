---
title: Aloita uusi React projekti
---

<Intro>

Jos haluat rakentaa uuden sovelluksen tai uuden verkkosivuston kokonaan Reactilla, suosittelemme valitsemaan yhden yhteisön suosituimmista React-pohjaisista kehyksistä. Kehykset tarjoavat useimpien sovellusten ja sivustojen tarvitsemat ominaisuudet, kuten reitityksen, datan hakemisen ja HTML:n luomisen.

</Intro>

<Note>

**Sinun täytyy asentaa [Node.js](https://nodejs.org/en/) paikalliseen kehitykseen.** Voit *myös* käyttää Node.js:ää tuotannossa, mutta ei ole pakko. Monet React-kehykset tukevat staattisen HTML/CSS/JS-kansion luomista.

</Note>

## Tuotantovalmiit React-kehykset {/*production-grade-react-frameworks*/}

### Next.js {/*nextjs*/}

**[Next.js](https://nextjs.org/) on täysin React-kehys.** Se on monipuolinen ja antaa sinun luoda minkä tahansa kokoisia React-sovelluksia--pienistä, pääasiassa staattisista blogeista suuriin monimutkaisiin sovelluksiin. Luo uusi Next.js-projekti ajamalla seuraava komento:

<TerminalBlock>
npx create-next-app
</TerminalBlock>

Jos olet uusi Next.js:ään, tutustu [Next.js -opetukseen.](https://nextjs.org/learn/foundations/about-nextjs)

[Vercel](https://vercel.com/) ylläpitää Next.js:ää. Voit [pyörittää Next.js -sovellusta](https://nextjs.org/docs/deployment) missä tahansa Node.js- tai serverless-palvelussa tai omalla palvelimella. [Täysin staattiset Next.js -sovellukset](https://nextjs.org/docs/advanced-features/static-html-export) voidaan sijoittaa mihin tahansa staattiseen palveluun.

### Remix {/*remix*/}

**[Remix](https://remix.run/) on full-stack React-kehys sisäkkäiellä reitityksellä.** Se mahdollistaa sovelluksen jakamisen sisäkkäisiin osiin, jotka voivat ladata dataa rinnakkain ja päivittää käyttäjän toimintojen mukaisesti. Luo uusi Remix-projekti ajamalla seuraava komento:

<TerminalBlock>
npx create-remix
</TerminalBlock>

Jos olet uusi Remixiin, tutustu Remixin [blogiopetukseen](https://remix.run/docs/en/main/tutorials/blog) (lyhyt) ja [sovellusopetukseen](https://remix.run/docs/en/main/tutorials/jokes) (pitkä).

[Shopify](https://www.shopify.com/) ylläpitää Remixiä. Kun luot Remix-projektin, sinun on [valittava palvelin, johon sovellus sijoitetaan](https://remix.run/docs/en/main/guides/deployment). Voit sijoittaa Remix-sovelluksen mihin tahansa Node.js- tai serverless-palveluun käyttämällä tai kirjoittamalla [adapterin](https://remix.run/docs/en/main/other-api/adapter).

### Gatsby {/*gatsby*/}

**[Gatsby](https://www.gatsbyjs.com/) on nopea, CMS-taustainen React-kehys.** Sen runsas lisäosaekosysteemi ja GraphQL-tietokerros helpottavat sisällön, API:en ja palveluiden integrointia yhteen verkkosivustoon. Luo uusi Gatsby-projekti ajamalla seuraava komento:

<TerminalBlock>
npx create-gatsby
</TerminalBlock>

Jos olet uusi Gatsbyyn, tutustu [Gatsby -opetukseen.](https://www.gatsbyjs.com/docs/tutorial/)

[Netlify](https://www.netlify.com/) ylläpitää Gatsbyä. Voit [sijoittaa Gatsby-sovelluksen](https://www.gatsbyjs.com/docs/how-to/previews-deploys-hosting) mihin tahansa staattiseen palveluun. Jos käytät palvelimiin perustuvia ominaisuuksia, varmista, että palveluntarjoajasi tukee niitä Gatsbylle.

### Expo (natiivisovelluksille) {/*expo*/}

**[Expo](https://expo.dev/) on React-kehys, joka mahdollistaa Android-, iOS- ja web-sovellusten luomisen oikeilla, natiiveilla käyttöliittymillä.** Se tarjoaa [React Native](https://reactnative.dev/) SDK:n, joka tekee natiiviosien käytöstä helpompaa. Luo uusi Expo-projekti ajamalla seuraava komento:

<TerminalBlock>
npx create-expo-app
</TerminalBlock>

Jos olet uusi Expoon, tutustu [Expo-opetukseen.](https://docs.expo.dev/tutorial/introduction/)

[Expo (the company)](https://expo.dev/about) ylläpitää Expoa. Expo-sovellusten luominen on ilmaista, ja voit lähettää ne Google Playn ja App Storen ilman rajoituksia. Expo tarjoaa lisäksi maksullisia pilvipalveluja.

<DeepDive>

#### Voinko käyttää Reactia ilman ohjelmistokehystä? {/*voinko-kayttaa-reactia-ilman-kehysta*/}

Voit käyttää Reactia ilman kehystä--niin [käyttäisit Reactia osana sivua.](/learn/add-react-to-an-existing-project#using-react-for-a-part-of-your-existing-page) **Kuitenkin, jos rakennat uutta sovellusta tai kokonaista sivustoa täysin Reactilla, suosittelemme kehystä.**

Tässä miksi.

Vaikka et tarvitse reititystä tai datanhakua aluksi, saatat todennäköisesti lisätä kirjastoja niitä varten. Kun JavaScript bundle -kokosi kasvaa jokaisen ominaisuuden kanssa, saatat joutua ratkomaan koodin jakamisen jokaiselle polulle erikseen. Kun datanhakusi tarpeet muuttuvat monimutkaisemmiksi, törmäät todennäköisesti palvelin/asiakas -verkkovesiputouksiin, jotka saavat sovelluksesi tuntumaan erittäin hitaalta. Kun yleisösi sisältää enemmän käyttäjiä huonoilla verkkoyhteyksillä ja vähempitehoisilla laitteilla, saattaa olla tarpeen luoda komponenttiesi HTML etuajassa--joko palvelimella tai build -prosessin aikana. Ympäristön muuttaminen suorittamaan osa koodistasi palvelimella tai build -prosessin aikana voi olla erittäin hankalaa.

**Nämä ongelmat eivät koske vain Reactia. Tämän takia Sveltellä on SvelteKit, Vuella Nuxt, ja niin edelleen.** Ratkaistaksesi nämä ongelmat omillasi, täytyy sinun integroida reititys ja datanhakukirjasto bundleriisi. Alkuperäisen asetuksen saaminen toimimaan ei ole vaikeaa, mutta on paljon yksityiskohtia, jotka on otettava huomioon, jotta sovellus latautuu nopeasti, toimii myös kasvaessaan. Saatat haluta lähettää sovelluksesi koodia mahdollisimman vähän, mutta yhdessä asiakas/palvelin kierroksessa, samanaikaisesti sivun tarvitsemien tietojen kanssa. Saatat haluta sivun olevan interaktiivinen ennen kuin JavaScript -koodisi on edes ajettu, jotta se tukee asteittaista parantamista (engl. progressive enhancement). Saatat haluta luoda kansion täysin staattisista HTML-tiedostoista markkinointisivuillesi, jotka voidaan julkaista missä tahansa ja toimivat myös JavaScriptin poiskytkemisen jälkeen. Näiden ominaisuuksien rakentaminen itse vaatii todellista työtä.

**React ohjelmistokehykset tällä sivulla ratkaisevat tämän kaltaisia ongelmia oletuksena, ilman ylimääräistä työtä puolestasi.** Niiden avulla voit aloittaa sovelluksen hyvin pienellä määrällä koodia ja sitten skaalata tarpeidesi mukaan. Jokainen React-kehys on oma yhteisönsä, joten kysymysten vastaaminen ja työkalujen päivittäminen on helpompaa. Kehykset antavat myös koodillesi rakenteen, joka auttaa sinua ja muita säilyttämään asiayhteyden ja taidot eri projekteissa. Vastaavasti, mukautetulla ympäristöllä on helpompi joutua jumiin riippuvuuksien ei-tuettuihin versioihin, ja lopulta päädyt luomaan oman kehyksen--tai ainakin sellaisen, jolla ei ole yhteisöä tai päivityspolkua (ja jos se on yhtään mitä olemme tehneet aikaisemmin, se tulee olemaan sattumanvaraisesti suunniteltu).

Jos et ole vielä vakuuttunut tai sovelluksellasi on poikkeuksellisia rajoituksia, jotka eivät sovi näihin ohjelmistokehyksiin, ja haluat luoda oman mukautetun ympäristösi, emme voi estää sinua--anna palaa! Hae `react` ja `react-dom` npm:stä, määritä mukautettu build -prosessi bundlerin kanssa kuten [Vite](https://vitejs.dev/):n tai [Parcel](https://parceljs.org/):in, ja lisää muut työkalut tarvittaessa reititykseen, staattiseen generointiin tai renderöintiin palvelimella ja muihin.
</DeepDive>

## Kehityksen reunalla olevat React ohjelmistokehykset {/*bleeding-edge-react-frameworks*/}

Kuten olemme tutkineet miten jatkaa Reactin kehittämistä, olemme huomanneet, että Reactin integroiminen tiiviimmin kehyksiin (erityisesti reititykseen, bundlaamiseen ja palvelinteknologioihin) on suurin mahdollisuus auttaa React-käyttäjiä rakentamaan parempia sovelluksia. Next.js -tiimi on yhtynyt meihin tutkimuksen, kehityksen, integroinnin ja testaamisen parissa ohjelmistokehys-agnostisiin, kehityksen reunalla oleviin ominaisuuksiin kuten [React Server Components](/blog/2020/12/21/data-fetching-with-react-server-components):iin.

Nämä ominaisuudet ovat lähempänä tuotantoa joka päivä, ja olemme keskustelleet muiden bundlerien ja kehysten kehittäjien kanssa integroimasta näitä ominaisuuksia. Toivomuksemme on, että vuoden tai kahden kuluttua kaikki tämän sivun kehykset tukevat täysin näitä ominaisuuksia. (Jos olet kehysten kehittäjä, joka on kiinnostunut yhteistyöstä meidän kanssamme näiden ominaisuuksien kokeiluun, ilmoita meille!)

### Next.js (App Router) {/*nextjs-app-router*/}

**[Next.js's App Router](https://beta.nextjs.org/docs/getting-started) on Next.js API:en uudelleen-suunniteltu versio, joka pyrkii täyttämään React -tiimin full-stack arkkitehtuurin vision.** Se mahdollistaa datan hakemisen asynkronisissa komponenteissa, jotka toimivat palvelimella tai jopa build -prosessin aikana.

[Vercel](https://vercel.com/) ylläpitää Next.js:ää. Voit [pyörittää Next.js -sovellusta](https://nextjs.org/docs/deployment) missä tahansa Node.js- tai serverless-palvelussa tai omalla palvelimella. Staattinen vienti on [suunniteltu, mutta ei vielä tuettu](https://beta.nextjs.org/docs/app-directory-roadmap#configuration) Next.js:n App Routerissa.

<Pitfall>

Next.js:n App Router on **tällä hetkellä beta-tilassa ja sitä ei vielä suositella tuotantokäyttöön** (marraskuussa 2023). Seuraamalla [tätä asteittaista päivitysohjetta](https://beta.nextjs.org/docs/upgrade-guide#migrating-from-pages-to-app), voit kokeilla sitä olemassa olevassa Next.js -projektissa.

</Pitfall>

<DeepDive>

#### Mitkä ominaisuudet muodostavat React -tiimin full-stack arkkitehtuurin vision? {/*which-features-make-up-the-react-teams-full-stack-architecture-vision*/}

Next.js:n App Router bundler toteuttaa täysin virallisen [React Server Components -määrittelyn](https://github.com/reactjs/rfcs/blob/main/text/0188-server-components.md). Tämä mahdollistaa build -aikaisen, palvelimella toimivan ja interaktiivisen komponenttien sekoittamisen yhteen React-puuhun.

For example, you can write a server-only React component as an `async` function that reads from a database or from a file. Then you can pass data down from it to your interactive components:

Esimerkiksi, voit kirjoittaa palvelimella toimivan React-komponentin `async` -funktiona, joka lukee tietokannasta tai tiedostosta. Sitten voit välittää datan interaktiivisiin komponentteihin:

```js
// Tämä komponentti suoritetaan *vain* palvelimella (tai build -prosessin aikana).
async function Talks({ confId }) {
  // 1. Olet palvelimella, joten voit jutelalta tietokantasi kanssa. API-endpointtia ei tarvita.
  const talks = await db.Talks.findAll({ confId });

  // 2. Lisää niin paljon renderöintilogiikkaa kuin haluat. Se ei tee JavaScript bundlestasi yhtään sen suurempaa.
  const videos = talks.map(talk => talk.video);

  // 3. Välitä data selaimessa toimiviin komponentteihin.
  return <SearchableVideoList videos={videos} />;
}
```

Next.js:n App Router myös integroi [datan hakemisen Suspensella](/blog/2022/03/29/react-v18#suspense-in-data-frameworks). Tämän avulla voit tehdä lataustilan (kuten luuranko-rakenteen) määrittämisen käyttöliittymäpuussa suoraan React-puussa:

```js
<Suspense fallback={<TalksLoading />}>
  <Talks confId={conf.id} />
</Suspense>
```

Palvelinkomponentit ja Suspense ovat React ominaisuuksia toisin kuin Next.js ominaisuuksia. Kuitenkin niiden hyväksyminen ohjelmistokehyksen tasolla vaatii hyväksynnän ja ei niin pienimuotoista toteutustyötä. Tällä hetkellä Next.js App Router on täydellisin toteutus. React-tiimi työskentelee bundler-kehittäjien kanssa tekemään nämä ominaisuudet helpommin toteutettaviksi seuraavan sukupolven ohjelmistokehyksissä.

</DeepDive>
