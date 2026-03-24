# La firma femminile commissionata
## DOI

## Descrizione
Questo progetto consiste in un'analisi esplorativa ed esplicativa di un dataset contenente dati relativi ad opere d'arte figurativa prodotte nell'arco di circa un millennio. L'analisi è focalizzata sull'indagine del rapporto tra le artiste di genere femminile e la committenza nella storia dell'arte attraverso tre domande di ricerca:
1. Esiste un rapporto tra il genere dell'artista e le dimensioni delle opere prodotte? 
2. A quali generi appartengono le opere prodotte da donne?
3. Esiste un rapporto tra il genere artistico e le dimensioni nelle opere prodotte da artiste?

### Quali sono i risultati?
Le risposte a questi tre quesiti, ottenute attraverso l'analisi computazionale all'interno del Jupyter Notebook, hanno permesso di definire un quadro abbastanza chiaro:
1. Le artiste di genere femminile producono, in media, opere di dimensioni maggiori rispetto ai colleghi di genere maschile.
2. I generi maggiormente prodotti dalle artiste non sono generi minori, bensì generi rilievo assoluto: il ritratto e l'arte religiosa.
3. Il rapporto tra genere artistico e area dell'opera è confermato (i generi maggiormente prodotti dalle artiste di genere femminile sono anche quelli delle opere di dimensioni maggiori).

Tutti questi elementi permettono di confermare che anche le artiste di genere femminile svolgono un ruolo primario nella storia dell'arte e lavorano per committenze importanti.


Il progetto è stato realizzato nell'ambito del corso Digital Humanities e Data Management per I Beni Culturali - Informatica per I Beni Culturali 2025-2026 dell'Università di Bologna.

## Fonte dei dati
I dati in input sono costituiti da un file CSV di 229.3+ KB scaricato da una repository GitHub del corso Digital Humanities e Data Management per I Beni Culturali - Informatica per I Beni Culturali dell'anno 2025/2026 (https://raw.githubusercontent.com/dhdmch/2025-2026/refs/heads/main/data/vapod/data.csv).
Le variabili considerate sono:

| Variabile | Tipo |	Definizione | Esempio |
| :------- | :--- | :--------- | :------ |
|  id     |	str | link ID dell'opera | 	http://www.wikidata.org/entity/Q368788	 |
| titolo | str | titolo dell'opera | Pietà |
| artisti | str | nome dell'artista | Perugino |
| data_creazione | int | anno di creazione dell'opera | 1483 |
| generi | str | generi ai quali l'opera afferisce | arte religiosa |
| luoghi | str | luogo di conservazione dell'opera | Palazzo degli Uffizi|
| collezioni | str | collezione alla quale l'opera appartiene | Palazzo degli Uffizi|
| contenuti | str | contenuto dell'opera | Gesù; donna; Maria; uomo|
| movimenti | str | movimenti artistici ai quali l'opera afferisce | rinascimento italiano |
soggetti | str | soggetti rappresentati | Pietà |
| altezza | float | altezza dell'opera in cm | 168.0 |
| larghezza | float | larghezza dell'opera in cm | 176.0 |
| genere_artista | str | genere dell'artista | maschio
| area opera | float | area dell'opera in cm² | 29568.00|

## Metodi e strumenti
Il progetto è stato sviluppato in un ambiente Google Colab utilizzando il linguaggio di programmazione Python. Lo strumento principale utilizzato per la manipolazione e l'analisi dei dati è la libreria Pandas, insieme a Matplotlib/Seaborn per la visualizzazione.

Le operazioni includono:

- Caricamento e ispezione dei dati (__pd.read_csv, .shape, .columns, df.info(), df.describe(), .duplicated(), .nunique(), .head(), .tail()__);
- Bonifica e normalizzazione dei dati (conversione delle date in tipo Int64, correzione manuale di outlier come le altezze e larghezze minime e massime errate, normalizzazione dei valori della colonna generi, correzione manuale di un titolo errato);
- Creazione di nuove variabili calcolate (genere_artista, area_opera);
- Analisi esplorativa tramite aggregazioni (__.value_counts()__), iterazioni (__.iterrows()__) e visualizzazioni tramite grafici a dispersione, a barre e a torta;
- Analisi esplicativa tramite aggregazioni e grafici a barre e a dispersione focalizzata sul rapporto tra i valori incrociati delle colonne genere_artista, area_opera e generi delle opere al fine di evidenziare l'esistenza di un rapporto tra le artiste di genere femminile e committenza importante nel corso della storia dell'arte.

## Responsabile
- Pierno, Chiara - Researcher

## Licenza
I dati di input e il codice di output (incluso in questo Notebook) sono rilasciati sotto licenza [CC0 1.0 Universal]( https://creativecommons.org/publicdomain/zero/1.0/).
