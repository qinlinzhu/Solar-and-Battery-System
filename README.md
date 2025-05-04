# Solar-and-Battery-System-
Solar and battery system design

## **Schematic**


<sub>CELLS1 and CELLS0 both strapped to INTVcc for 1 cell charging</sub>

**CSP/CSN and CLP/CLN sense resistor calculations:**

<sub>LTC4162EUFD-L42#PBF is a 4.2V Fixed Voltage therefore sense voltage is 50mV</sub>

<sub>CLP/CLN Input current limit:
solar panel peak current 540 mA
sense resistor value = 50mV / 540mA = 100 mΩ</sub>

<sub>CSP/CSN Battery Charge limit:
1000 mAh LiFePO₄ cell standard Charge 0.2C
0.2×1000mAh = 200mA
sense resistor value = 50mV / 200mA = 250 mΩ</sub>

<sub>PGND (Pins 23,24): Power ground pins. These pins should 
be connected to a copper pour that forms the return for 
the VOUT bypass capacitor on the top layer of the printed 
circuit board.</sub>

**MOSFETS**
<sub>**Pin 6 external N-channel MOSFET:**</sub>
<sub>The MOSFET used as a smart reverse-current protection switch between solar panel and the charger input (VIN). Protects battery from reverse current when solar panel loses power. More efficent than a diode.Higher efficiency, less heat, longer battery life.</sub>

<sub></sub>
<sub></sub>
<sub></sub>

## **Sources**

Polymer Lithium Ion Battery (LiPo) 3.7V 1100mAh
https://ecocell.com.au/product/lipo-1100-603450/

Charger for Solar Power
https://www.digikey.co.nz/en/products/detail/analog-devices-inc/LTC4162EUFD-L42-PBF/9446104


Solar panel
https://wiki.seeedstudio.com/3W_Solar_Panel_138x160/

Voltage regulator for system load
https://www.ti.com/lit/ds/symlink/tps62840.pdf?ts=1742364920887&ref_url=https%253A%252F%252Fwww.ti.com%252Fproduct%252FTPS62840%253Futm_source%253Dgoogle%2526utm_medium%253Dcpc%2526utm_campaign%253Dapp-bsr-null-44700045336317629_prodfolderdynamic-cpc-pf-google-soas_en_int%2526utm_content%253Dprodfolddynamic%2526ds_k%253DDYNAMIC+SEARCH+ADS%2526DCM%253Dyes%2526gad_source%253D1%2526gclid%253DEAIaIQobChMI1bXC4rqVjAMVVxGDAx20FQmZEAAYASAAEgJg-_D_BwE%2526gclsrc%253Daw.ds
