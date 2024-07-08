# Arduino-LED-Dimmer
Außenleuchten mit Touch-Display und Funk steuern

Für unsere Terassenüberdachung haben wir uns [diese](https://www.ledando.de/detail/index/sArticle/27312/sCategory/277) LED-Leuchten gekauft. Da uns eine einfach Fernbedienung nicht Praktisch genug war, habe ich den mitgelieferten LED-Controller ausgetauscht und durch einen eigenen mittels Arduino gesteuerten ausgetauscht. Dieser kann nun über Funk mit einem Touch-Display (ebensfalls mit Arduino realisiert) gesteuert werden. 
##
_Hier werde ich in den kommenden Tagen & Wochen meine Arduino-Codes, sowie Schaltpläne und Vorgehensweisen mit euch teilen._ \
_Die Dokumentation ist also noch nicht vollständig, schaut einfach alle paar Tage mal vorbei :)_
##
Um die LEDs über Funk Ein- und auszuschalten muss natürlich auch der Controller ausgetauscht werden. \
Hierfür habe ich als Grundlage einen Arduino Nano verwendet./
Da die Lampen über ein 12V-Netzteil versorgt werden, werde ich diese über ein MOSFET Schalten. Das Dimmen wird über eine PWM-Frequenz realisiert. PWM (Pulsweitenmodulation) ist nichts anderes wie ganz schnelles ein/ausschalten der Stromversorgung und je nach Geschwindigkeit der Schaltvorgänge leuchten die Lampen dunkler oder heller. \
Die Kommunikation per Funk wurde mit einem *NRF24L01* realiert. \
Um den Spannungsregler auf dem Arduino-Board nicht unnötig mit 12V zu belasten habe ich einen LM7808 vorgeschaltet, welcher die Eingangsspannung bereits auf 8V reduziert. Dies ist aber Optional. \
\
Entsprechend habe ich mir dafür einen eigenen Schaltplan entworfen und diesen auf dem Steckbrett getestet:
![C9FBBE69-0695-41C5-B4AF-8689455A6226](https://github.com/larsbaum/Arduino-LED-Dimmer/assets/167971634/d3ce2f57-5f22-4485-9399-4e51348532e3)
