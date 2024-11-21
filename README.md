# ESPHOME-ESP32_CYD_V2-SmartEnergyMeter Solar Monitor Configuration

[20241121_190408](https://github.com/user-attachments/assets/98b5d0d1-35e8-4e53-99f0-1f9d7d111d01)

## Descrizione

L'**ESP32 Solar Monitor** è una configurazione avanzata per ESPHome che integra un display **ESP32-2432S028R** con **Home Assistant**. Questo progetto consente di monitorare in tempo reale i dati del tuo impianto fotovoltaico, tra cui produzione solare, consumo domestico, immissione/prelievo dalla rete e stato della batteria. 

L'interfaccia grafica è sviluppata con **LVGL**, offrendo un design moderno e interattivo con supporto touch.

## Funzionalità

- **Produzione Solare**: Monitoraggio in tempo reale della potenza generata.
- **Consumo Domestico**: Visualizzazione dell'energia consumata in casa.
- **Immissione/Prelievo dalla Rete**: Dati sull'energia importata o esportata.
- **Stato della Batteria**: Percentuale di carica e stato di ricarica/scarica.
- **Interfaccia Touch**: Navigazione fluida tra le diverse schermate.
- **Grafici e Indicatori**: Barre di progresso e icone dinamiche per rappresentare i dati.!


## Requisiti di Sistema

- **Hardware**:
  - ESP32-2432S028R con display TFT e touchscreen.
  - Inverter fotovoltaico configurato in Home Assistant.
  - Sensori per produzione, consumo e batteria.

- **Software**:
  - [ESPHome](https://esphome.io/) configurato nella rete locale.
  - Font `materialdesignicons-webfont.ttf` da posizionare nella directory `fonts/`.

## Installazione

1. **Clona il repository**:
   ```bash
   git clone https://github.com/tuonome/esp32-solar-monitor.git
   cd esp32-solar-monitor

2. **Prepara i file necessari**:
   - Copia il font `materialdesignicons-webfont.ttf` nella directory `fonts/`.
   - Configura il file `secrets.yaml` con le tue credenziali Wi-Fi e chiavi API.

3. **Carica la configurazione su ESPHome**:
   - Modifica i parametri necessari nel file YAML (nome dispositivo, ID delle entità di Home Assistant, ecc.).
   - Carica la configurazione sul dispositivo ESP32 tramite l'interfaccia ESPHome.

4. **Configura Home Assistant**:
   - Assicurati che i sensori siano configurati correttamente in Home Assistant per fornire i dati richiesti.

## Utilizzo

Dopo l'installazione, l'interfaccia mostrerà:

- **Produzione Solare**: Valore corrente in watt, con barra di progresso.
- **Consumo Casa**: Energia consumata dalla casa.
- **Rete**: Energia immessa o prelevata dalla rete.
- **Batteria**: Stato di carica e flusso di energia (ricarica/scarica).

Puoi navigare tra le schermate utilizzando il menu interattivo touch nella parte inferiore del display.

## Personalizzazioni

- **Font e Stili**: Modifica colori e dimensioni nella sezione `lvgl.theme` del file YAML.
- **Sensori Home Assistant**: Aggiorna gli ID delle entità nella sezione `sensor` per adattarli alla tua configurazione.
- **Navigazione e Schermate**: Personalizza layout e contenuti nelle sezioni `lvgl.pages`.

## Contribuire

I contributi sono benvenuti! Per segnalare problemi o proporre miglioramenti, apri una [issue](https://github.com/simone7121/ESPHOME-ESP32_CYD_V2-SmartEnergyMeter/issues) o invia una pull request. 

## Licenza

Questo progetto è distribuito sotto licenza **GPL V3**. Per maggiori dettagli, consulta il file [LICENSE](LICENSE).

## Autore

Sviluppato con passione da **[Simone7121]**.

Per ulteriori informazioni o domande, contatta [info@simonedanna.it](mailto:info@simonedanna.it).
