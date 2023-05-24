# Herkansing CSS to the Rescue

![cover](https://github.com/maxvl3/cssHerkansing/assets/94384526/7188b4c7-63e0-4635-8d4b-a059c8083290)

Live demo: https://maxvl3.github.io/cssHerkansing/

Dit is mijn herkansingsopdracht voor het vak CSS to the rescue. Tijdens dit vak leer ik nieuwe CSS technieken, en bouw ik als eindproduct een interactief experiment.  Als eindproduct heb ik gekozen om een bedieningspaneel te bouwen waarmee de gebruiker het licht kan bedienen in een kamer.

## Functionaliteiten

- Aan/uit zetten
- Dimmen/feller zetten
- Kleur aanpassen
- Partymode activeren

## Gebruikte technieken

- HTML
- CSS
- JavaScript (mini range scriptje)

## Reflectie eerste beoordeling

Voor mijn eerste beoordeling heb ik een dj draaitafel gemaakt als eindproduct. Hier het linkje naar de repository: https://github.com/maxvl3/css-to-the-rescue-2223. Helaas was dit nog niet goed genoeg om het vak af te sluiten met een voldoende. Hierbij even een kort overzicht van wat er goed en fout was aan dit eindproduct:

Wat was al goed?
- Geëxperimenteerd met nieuwe css technieken
- Goed en duidelijk concept
- Mooie vormgeving

Wat moest beter?
- Er waren geen interacties
- Proces was niet op orde

## Nieuw concept

Ik heb ervoor gekozen om niet door te gaan met mijn oude concept (dj draaitafel). De reden daarvoor was dat ik te weinig ideeën had hoe ik de draaitafel interactief kon maken. Ook waren de HTML elementen die ik had geschreven niet helemaal optimaal om interactie aan toe te voegen.

Mijn nieuwe concept focust zich voornamelijk op interactie, omdat dit juist hetgeen was dat miste. Ik heb een digitale LoFi schets gemaakt in Figma zodat ik me minder druk hoefde te maken met de vormgeving.

![concept](https://github.com/maxvl3/cssHerkansing/assets/94384526/86ba8950-89f2-43b8-a02a-df8389332844)

## Nieuwe CSS technieken

Ik mijn vorig eindproduct had al wat geëxperimenteerd met nieuwe CSS technieken. Dat waren de volgde technieken:

- HSL kleuren
- Display p-3
- Native CSS nesting
- Dark/light mode

Voor mijn herkansing heb ik nog eens gekeken welke technieken nog meer handig zijn om te leren. En vooral de technieken die nuttig zijn bij het maken van interacties.

- Has selector
- ::before/::after
- Data attributes

De has selector vond ik voordat ik mijn herkansings eindproduct maakte erg vaag. Maar nu heb ik me er meer in verdiept en uiteindelijk ook best vaak gebruikt in mijn nieuwe concept. Ik vind het een zeer krachtige css selector omdat je in combinatie met :checked zowat elk element uit je body kan aanpassen. Hier een voorbeeld hoe ik dit in mijn code heb verwerkt:

```
body:has(header > div:nth-of-type(1) input:checked)
  main
  section
  div:nth-of-type(3) {
  display: block;
}
```

Ik had ook nog weinig ervaring met ::before en ::after in css. Dit zijn belangrijke pseudo-elements voor het stylen van input’s en labels. In mijn herkansing eindproduct heb ik hier erg veel gebruikt van gemaakt. Hier een voorbeeld: 

```
header > div:nth-of-type(1) label span:nth-of-type(2)::before {
  right: -0.375em;
  background-color: transparent;
  transform: skewY(65deg);
}
```

Als laatst heb ik ook gewerkt met data attributes in HTML/CSS. Hiervoor heb ik het korte range scripje gebruikt als enige JavaScript. De data value is gemakkelijk te gebruiken in CSS, hier een voorbeeld:

```
head[data--x="9"] + body main section div:nth-of-type(3) {
  opacity: 0.9;
}
```

## Bronnenlijst

- https://developer.mozilla.org/en-US/docs/Learn/HTML/Howto/Use_data_attributes
- https://css-tricks.com/almanac/selectors/a/after-and-before/
- https://codepen.io/nelledejones/pen/gOOPWrK
- https://www.magicpattern.design/tools/css-backgrounds
- https://developer.mozilla.org/en-US/docs/Web/CSS/:has
- https://freefrontend.com/css-toggle-switches/
