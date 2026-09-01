# Ansluta Progressorn

Så kopplar du din Tindeq Progressor till appen via Bluetooth — från att väcka dosan till att kurvan följer draget. Guiden är skriven för Progressor 200, men modellnumret är bara maxlasten (200 kg): alla Progressor-modeller pratar samma protokoll, så appen fungerar rakt av.

Knappnamnen nedan följer appens engelska gränssnitt (**Connect**, **Tare**, **Start session**).

## Det här behöver du

- **En Progressor** med batteri i.
- **Chrome eller Edge** på dator eller Android — de har Web Bluetooth. På iPhone/iPad saknar Safari och Chrome det: installera webbläsarappen **Bluefy** och öppna appen där i stället.
- **Appen över https** — GitHub Pages-adressen eller `localhost`. Web Bluetooth vägrar osäkra sidor, så en `index.html` öppnad direkt från hårddisken ger bara demoläget.
- **Bluetooth på** i systemet. På macOS behöver webbläsaren dessutom Bluetooth-behörighet: Systeminställningar → Integritet och säkerhet → Bluetooth.

## Anslut, steg för steg

1. **Rigga och väck dosan.** Förankra Progressorn i något stabilt — räcke, krok, ribbstol — och häng listen eller blocket under. Tryck sedan på knappen på dosan så att lampan börjar blinka: då annonserar den och går att hitta. Den somnar om efter en stund utan anslutning, så väck den strax innan du ansluter.

2. **Tryck på Connect i appen** (uppe till höger). Webbläsaren öppnar en lista över Bluetooth-enheter i närheten.

3. **Välj din Progressor i listan.** Den heter `Progressor_` följt av ett nummer. Markera den och tryck på Koppla/Para. Dyker den inte upp inom några sekunder har dosan oftast hunnit somna — tryck på knappen igen och låt listan söka om.

4. **Vänta in den gröna pricken.** Appen läser av batteriet, nollar vågen och börjar strömma. Statuspillret växlar från "No device" till t.ex. "Progressor_1234 · 3021 mV" — grön prick betyder ansluten, siffran är batterispänningen.

5. **Kontrollera med ett drag.** Dra lätt i listen. Kilosiffran ska röra sig direkt och kurvan följa handen. Gör den det är du klar — välj program och tryck **Start session**.

   Nollningen sker med det som hänger i dosan just då, och appen nollar även automatiskt när ett pass startar. Låt därför riggen hänga stilla och obelastad vid anslutning och start. Byter du block: häng på det nya, låt det hänga fritt och tryck **Tare**.

> **Ingen dosa till hands?** Tryck Connect i en webbläsare utan Web Bluetooth så startar demoläget — håll musknappen eller mellanslag nedtryckt för att simulera kraft. Bra för att utforska appen, men inget att bygga riktiga maxvärden på.

## Om det strular

**Progressorn syns inte i listan.** Nästan alltid: den har somnat — tryck på knappen så lampan blinkar, och sök igen. Annars: stäng Tindeqs egen app om den är igång på en telefon i närheten. Bluetooth tillåter bara en anslutning åt gången, och en dosa som redan är upptagen annonserar inte.

**Knappen startar demoläget i stället.** Webbläsaren saknar Web Bluetooth, eller så visas sidan över en osäker anslutning. Använd Chrome eller Edge över https — på iPhone/iPad: Bluefy.

**Ansluten, men siffran står stilla på 0.0.** Tryck **Tare** och dra igen. Hjälper inte det: ladda om sidan, väck dosan och anslut på nytt.

**Kontakten bryts mitt i ett pass.** Appen avbryter då passet och maxtestet självt — inget halvfärdigt värde sparas. Väck dosan, tryck Connect och starta om passet. Bryts det ofta: kortare avstånd mellan dosa och skärm, och kolla batterisiffran i statuspillret — en fräsch cell ligger kring 3000 mV, och en bra bit därunder är batteriet första misstänkta.

**Ingen behörighetsfråga, inget händer.** På macOS: ge webbläsaren Bluetooth-behörighet under Systeminställningar → Integritet och säkerhet → Bluetooth, och ladda om sidan. På Windows/Android: kontrollera att Bluetooth är på i systemet.

## Före första riktiga passet

Kör ett **maxtest** per hand först. Alla mål i programmen räknas som procent av uppmätt max — utan det vägrar appen starta, med flit.
