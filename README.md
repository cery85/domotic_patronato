# domotic_patronato

## Intro
progetto orientato alla domotica che permette l'accensione e spegnimento delle luci di casa da remoto.  

Il progetto utilizza un **Raspberry P3**, una scheda relè.  
Il software è basato **Openhabian** e **MQTT** (tramite mosquito)  
Lattuazione delle luci nell'impianto avviene tramite il servizio cloud di openhub, su una pagina web 
![openhab screenshot](https://image.ibb.co/eoFCVq/openhab-screen.png)
** GRASSETTO  
° CORSIVO  
_**GRASSETTO CORSIVO**_
MONOSPACE

## Hardwere
BOM(Bill of Materials):  
* Raspberry PI 3;  
* Modulo relè optoisolato, con il numero di canali necessari  
* Jumper Dupont  
* Pulsante 6x6  

## Software

1. Installare openhabian seguendo la [guida ufficiale](https://www.openhab.org/docs/installation/openhabian.html#features)  
1. Prima del primo avvio, creare il file vuoto `ssh ` nella root della SD, facendo attenzione che non abbia estensione.
1. Trovare l'ip del raspberry connesso in rete ed utilizzare un client SSH (_ad esempio putty_) per connettersi.Di default sono user:  `openhabian ` pw:  `openhabian`.  
1. Aggiornare il sistema con:
    
    ```
    sudo apt update
    sudo apt upgrade 
    ```
1. nella cartella /etc/openhab2/items creare il fil [user]
