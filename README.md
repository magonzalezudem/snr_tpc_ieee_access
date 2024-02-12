# Subset of LoRaWAN Path Loss Dataset including Environmental Variables
This dataset includes a subset of the measurement campaign for LoRaWAN End Nodes measuring path loss and environmental variables previously shared in https://github.com/magonzalezudem/MDPI_LoRaWAN_Dataset_With_Environmental_Variables. This subset included one daily register per End Node where we guaranteed that the SNR variability was high, i.e., the SNR values were under the percentile 5th and above the percentile 95th. 

The subset includes the following fields:

### Row identification
- **row_number**: A sequential number from 1 to 990750
- **timestamp**: The date and time field for the current measurement
- **device_id**: The name of the EN that corresponds to the current measurement
### Physical/geometric conditions
- **distance**: The distance between the EN and the GW in meters
- **ht**: Antenna height of the EN in meters
- **hr**: Antenna height of the GW in meters
### Link budget features
- **ptx**: Transmitter (EN) radio power in dBm
- **ltx**: Transmitter (EN) losses associated to cables and connectors in dB
- **gtx**: Transmitter (EN) antenna gain (characterized with a Vector Network Analyzer) in dBi
- **lrx**: Receiver (GW) losses associated to cables and connectors in dB
- **grx**: Receiver (GW) antenna gain (characterized with a Vector Network Analyzer) in dBi
- **frequency**: Carrier frequency in Hz
- **frame_length**: Number of bytes of the current transmission
### Environmental variables
- **temperature**: Environment temperature of the current measurement in °C
- **rh**: Relative humidity of the current measurement in %
- **bp**: Barometric pressure of the current measurement in hPa
- **pm2_5**: Particulate matter of the current measurement in ug/m3
### Received signal strength and channel signal to noise ratio
- **rssi**: Received signal strength indicator in the GW in dBm
- **snr**: Channel signal to noise ratio in dB
- **toa**: Time on air of the current transmission in seconds
### Calculated path loss and energy
- **experimental_pl**: Experimental path loss calculated by ptx+gtx-ltx+grx-lrx-rssi
- **energy**: Consumed energy in current transmission in Joules

This dataset can be used to estimate the impact of the weather changes in path loss for LoRaWAN deployments, and get more accurate tracking/positioning data or more efficient energy reduction strategies.
