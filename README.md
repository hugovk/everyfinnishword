# Every Finnish Word

Words from the [Institute for the Languages of Finland](http://kaino.kotus.fi/sanat/nykysuomi/) (Kotimaisten kielten keskus in Finnish, or KOTUS).

The [kotus-sanalista_v1](/kotus-sanalista_v1) directory contains the original files from KOTUS. The file [kaikkisanat.txt](kaikkisanat.txt) contains a plaintext list of the words from the [XML file](kotus-sanalista_v1/kotus-sanalista_v1.xml), with suffixes (e.g. -aatteinen) and duplicates removed. This plaintext file is used by [@kaikkisanat](https://twitter.com/kaikkisanat) on Twitter.

Files are licensed under GNU LGPL (Lesser General Public License), EUPL v.1.1 (European Union Public Licence) and CC Attribution 3.0 Unported.

Here's the original KOTUS description:

---

## KOTIMAISTEN KIELTEN KESKUKSEN NYKYSUOMEN SANALISTA

Kotimaisten kielten keskus julkaisee taivutustiedoin täydennetyn nykysuomen sanalistan. Sanalista ei ole tyhjentävä tai auktoritatiivinen luettelo suomen kielen sanoista, vaan sen on tarkoitus mm. toimia apuvälineenä suomen kieltä käsittelevien tietokoneohjelmien ja suomenkielisten käyttöliittymien kehitystyössä.

Sanalista julkaistaan lisensseillä GNU LGPL (Lesser General Public License), EUPL v.1.1 (Euroopan unionin yleinen lisenssi) ja CC Nimeä 3.0 Muokkaamaton.

Sanalistan laajuus on 94 110 sanatietuetta. Sanalista on XML-muodossa ja merkistönä on UTF-8. Listaan voidaan tehdä myöhemmin muutoksia, jolloin listan versionumero muuttuu.

### Sanatietueiden elementit

`<st></st>`	   	sanatietue  
`<s></s>`	   	sana  
`<hn></hn>`	   	homonyyminumero  
`<t></t>`	   	taivutustiedot  
`<tn></tn`>	   	taivutusnumero  
`<av></av>`	   	astevaihtelutiedot  

### Esimerkkikatkelma

```xml
<st><s>aloitteikas</s><t><tn>41</tn><av>A</av></t></st>
<st><s>-aloitteinen</s><t><tn>38</tn></t></st>
<st><s>aloittelija</s><t><tn>12</tn></t></st>
<st><s>aloitus</s><t><tn>39</tn></t></st>
<st><s>aloituskorkeus</s></st>
<st><s>aloitusmerkki</s></st>
<st><s>aloituspaikka</s></st>
<st><s>aloitussyöttö</s></st>
<st><s>aloitusviisikko</s></st>
<st><s>alokas</s><t><tn>41</tn><av>A</av></t></st>
<st><s>alokasaika</s><t><tn>9</tn><av>D</av></t></st>
<st><s>alokasaste</s></st>
<st><s>alokasmainen</s><t><tn>38</tn></t></st>
<st><s>aloke</s><t><tn>48</tn><av>A</av></t></st>
<st><s>alpakka</s><hn>1</hn><t><tn>14</tn><av>A</av></t></st>
<st><s>alpakka</s><hn>2</hn><t><tn>14</tn><av>A</av></t></st>
<st><s>alpakkainen</s><hn>1</hn><t><tn>38</tn></t></st>
<st><s>alpakkainen</s><hn>2</hn><t><tn>38</tn></t></st>
<st><s>alpakkalusikka</s></st>
<st><s>alpi</s><t><tn>7</tn><av>E</av></t><t taivutus="harvinainen"><tn>5</tn></t></st>
```

### Sanojen taivutus

Sanan taivutus on osoitettu sanalistassa numerolla (esim. <tn>72</tn>) ja sanaan liittyvä astevaihtelu kirjaimella (esim. <av>A</av>). Numerot ja kirjaimet viittaavat mallisarjoihin Taivutustyypit ja Astevaihtelutyypit, joissa taivutus ja astevaihtelu on esitetty vastaavan numeron ja kirjaimen kohdalla mallisanojen avulla. Jos sana taipuu kahdella eri tavalla, sillä on kaksi taivutusnumeroa.

Taivutukseen liittyvää lisätietoa on annettu t-elementin ja av-elementin attribuuttien avulla. Elementillä t voi olla attribuutti *taivutus*. Elementillä av voi olla attribuutti *astevaihtelu*.

*taivutus*-attribuutin arvot:  
 * harvinainen – t-elementin mukainen taivutus on harvinainen
 * mahdollinen – t-elementin mukainen taivutus on mahdollinen
 * yksikössä – sana taipuu tn-elementin mukaisesti yksikössä
 * monikossa – sana taipuu tn-elementin mukaisesti monikossa

*astevaihtelu*-attribuutin arvo:  
 * valinnainen – sana voidaan taivuttaa astevaihtelullisena tai ilman astevaihtelua

Yhdyssanoihin ei ole yleensä merkitty taivutusnumeroa, jos perusosa on listassa itsenäisenä sanana. Taivutustieto on kuitenkin merkitty niihin yhdyssanoihin, joiden perusosa on homonyymi (esim. iltakuusi 27 ja joulukuusi 24). Yhdysnomineihin on merkitty taivutusnumero silloin, kun on haluttu osoittaa, että sanan alkuosa taipuu (kuten hienosokeri : hienonsokerin, taivutusnumero 51) tai jää taipumatta (isoäiti :isoäidin, taivutusnumero 50). Taipumattomat tai vaillinaisesti taipuvat sanat on merkitty numerolla 99. Pronominien jäljessä ei ole taivutusnumeroa, koska niille ei voida esittää mallitaivutusta. Lukusanojen taivutus ei aina selviä suoraan mallisanan avulla (esim. lukusanat seitsemän, kahdeksan ja yhdeksän taipuvat niin kuin nominatiivit olisivat seitsemä, kahdeksa ja yhdeksä, ja kymmenen taipuu niin kuin nominatiivi olisi kymmen). Lukusanatyyppien kaksitoista, kaksikymmentä, kaksisataa ja kaksituhatta taivutusta ei ole osoitettu.
