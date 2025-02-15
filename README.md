# Arduino-LED-Dimmer

Für unsere Terrassenüberdachung haben wir uns [diese](https://www.ledando.de/detail/index/sArticle/27312/sCategory/277) LED-Leuchten gekauft. Da uns eine einfache Fernbedienung nicht praktisch genug war, habe ich den mitgelieferten LED-Controller durch einen eigenen, mittels Arduino gesteuerten, ersetzt. Dieser kann nun über Funk mit einem ebenfalls Arduino-gesteuerten Touch-Display bedient werden. 

##
_Hier werde ich in den kommenden Tagen & Wochen meine Arduino-Codes, sowie Schaltpläne und Vorgehensweisen mit euch teilen._ \
_Die Dokumentation ist also noch nicht vollständig, schaut einfach alle paar Tage mal vorbei :)_

##
Um die LEDs über Funk ein- und auszuschalten, muss der Controller ausgetauscht werden. 
Hierfür habe ich einen Arduino Nano verwendet. Da die Lampen über ein 12V-Netzteil versorgt werden, werde ich diese über ein MOSFET schalten. Das Dimmen wird über eine PWM-Frequenz realisiert. PWM (Pulsweitenmodulation) ist nichts anderes als ein schnelles Ein- und Ausschalten der Stromversorgung, und je nach Geschwindigkeit der Schaltvorgänge leuchten die Lampen dunkler oder heller. 
Die Kommunikation per Funk wurde mit einem *NRF24L01* realisiert. 
Um den Spannungsregler auf dem Arduino-Board nicht unnötig mit 12V zu belasten, habe ich einen LM7808 vorgeschaltet, welcher die Eingangsspannung auf 8V reduziert. Dies ist jedoch optional.

Entsprechend habe ich mir dafür einen eigenen Schaltplan entworfen und diesen auf dem Steckbrett getestet:
<img src="https://github.com/larsbaum/Arduino-LED-Dimmer/assets/167971634/d3ce2f57-5f22-4485-9399-4e51348532e3" alt="Schaltplan" width="50%" /> \
\
Das ganze funktioniert soweit. In der Firma in der ich Arbeite gibt es einen Platinenlaser für Prototypen. Diesen habe ich verwendet um das ganze auf eine Kompakte größe zu bringen. \
\
<img src="https://github.com/user-attachments/assets/853fa53f-cf95-43d3-8ba1-931d7caa89cb" alt="Platine" width="50%" />


_..._ 

