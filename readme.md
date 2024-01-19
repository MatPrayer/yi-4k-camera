# Appunti per Xiaomi Yi 4k Camera


## Device info

- Serial Number: Z16V13LW630AUS3463383

## Foto e video

### Impostazioni
Alcune impostazioni della videocamera necessitano di spiegazioni più approfondite. Di seguito sono riportate alcune delle impostazioni più importanti.

- **Risoluzioni Ultra:** Sono modalità di registrazione con un FOV maggiore rispetto a quelle normali.

- **Metering Mode:** (Esposizione spiegata da ChatGPT) 
  - ***Center:***  La fotocamera presta maggiore attenzione alla luce nella parte centrale dell'immagine, ignorando parzialmente le aree periferiche.
  - ***Spot:*** La fotocamera misura solo la luce in una piccola area specifica al centro del fotogramma. Questo è utile quando si desidera misurare accuratamente l'esposizione di un soggetto specifico in una scena.
  - ***Average:*** La fotocamera considera l'illuminazione complessiva della scena e cerca di ottenere una media, regolando i parametri di esposizione di conseguenza.

- **Sharpness:** (Nitidezza) Il suggerimento è di impostare il valore a `low`, che sembra disattivarla. Si tratta di un filtro software che non fa altro che peggiorare la qualità dell'immagine.

- **Electronic Image Stabilization:** (Stabilizzazione elettronica dell'immagine) La stabilizzazione elettronica dell'immagine via software funziona, ma è stato segnalato che può causare problemi di jittering. *Da testare*.

Molte impostazioni, in particolare per quanto riguarda particolari risoluzioni e bitrate sono accessibili solo modificando il file `autoexec.ash`.

## Connettività

### Info generali

- WiFi AP SSID: `YDXJ_XXXXXX_XG`
- WiFi AP Password: `1234567890`

Utilizzando il [firmware custom (Version: 1.10.52)](https://github.com/psolyca/Yi_4k_ROOTFS) è possibile modificare molte impostazioni riguardanti la connettività di rete della camera. Per farlo è necessario modificare il file `wifi.conf` presente nella root della scheda SD. (O nella root del filesystem se si utilizza FTP).

È possibile accedere ad alcune cartelle della camera anche tramite un webserver integrato, disponibile in modalità WiFi AP puntando al Default Gateway.

### Modalità WiFi AP

#### Indirizzi default in modalità WiFi AP:
- Default Gateway: 192.168.50.1
- IPv4 Address: 192.168.50.5

## TELNET
`telnet 192.168.50.1`

- Login: `root`

### Comandi utili

- Avvia FTP: `tcpsvd -u root -vE 0.0.0.0 21 ftpd /tmp`

---

## Link utili / fonti

- [Psolyca's Yi4K Camera Mod](https://psolyca.ovh/)

- [Yi 4k Camera - Custom Firmware](https://github.com/psolyca/Yi_4k_ROOTFS)

- [Irugentoo's Documentation](https://github.com/irungentoo/Xiaomi_Yi_4k_Camera)

- [DashCamTalk](https://dashcamtalk.com/forum/threads/yi-4k-z16vxxl-custom-firmware-and-more-update-20-12-20-release-1-10-52-ethernet-over-usb.35439/)

- [cmdYi - Yi 4k commandline controller for PC](https://github.com/NikolayRag/cmdYi)

- [YiOpenAPI](https://github.com/YITechnology/YIOpenAPI)

- [Yi4kApi - Python](https://github.com/NikolayRag/Yi4kAPI)


