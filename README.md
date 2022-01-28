# Predicting Hard Drive failure
Deze repository bevat de casus voor de minor "Data Science". De opdracht van deze casus was om onderzoek te doen naar 'Predictive Maintenance'. Dit houd in voorspellen wanneer een apparaat onderhoud nodig heeft op basis van operationele gegevens (temperatuur, druk etc) van bijvoorbeeld machines, servers, auto's enzovoorts.

Het project bestaat uit interactieve Jupyter Notebooks (zie folder `notebooks`). Deze Notebooks zijn chronologisch gesorteerd, van de initiele verkenning van de dataset tot het produceren van modellen.

Auteurs:
* Batchev, Dimitri
* Debets, Dwayne
* Grbić, Rade
* Remmen, Martijn
* Roijen, Peter


## Dataset
Wij hebben gekozen om gebruik te maken van de harde schijf dataset van Backblaze, een cloud provider. Deze dataset bestaat uit 'SMART' waardes van de harde schijven. Deze waardes leggen bepaalde operationele gegevens vast over een harde schijf. Zaken zoals de temperatuur, RPM van de schijf, reallocated sectors, read errors etcetera (zie [Wikipedia](https://en.wikipedia.org/wiki/S.M.A.R.T.) voor een complete lijst).

Daarnaast bevat de dataset een 'failure' kolom. Deze geeft aan dat de schijf de volgende dag faalt (dit wordt vastgesteld door de RAID Controller). De failure kolom is van belang bij het toepassen van supervised learning omdat deze als label gebruikt kan worden (deze waarde proberen we te voorspellen aan de hand van de SMART waardes).

## Gebruik
Om de notebooks zelf uit te kunnen voeren

1. *Optioneel* Maak een [Python Virtual Environment](https://docs.python.org/3/tutorial/venv.html) met `python3 -m venv venv`
2. *Optioneel* indien je een Virtual Environment hebt gemaakt, activeer deze met *Windows:* `venv\Scripts\activate.bat`, *Unix/MacOS:* `source venv/bin/activate`
3. Installeer de dependencies: `pip install -r requirements.txt`
4. Het is nodig om [de dataset hier te downloaden](https://www.backblaze.com/b2/hard-drive-test-data.html). De downloadlinks zijn te vinden helemaal onderaan de pagina *"Downloading the Raw Hard Drive Test Data"*. Onze Notebooks zijn gemaakt met de data van heel 2020 (4 kwartalen). Pak deze datasets uit in de folder `data/raw`. (zodat alle csv's in de `raw` folder staan)
5. Voer nu het notebook `1 - sample generating` volledig uit. **Let op: Hier wordt een grote hoeveelheid aan data verwerkt (32gb werkgeheugen aangeraden).**
