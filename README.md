# Nodemcu_as_Hotspot
i will code nodemcu to work as a Assoc point or hotspot 
````
#include <ESP8266WiFi.h>

WiFiClient client;
WiFiServer server(80);
const char *ssid = "Node_groot"; 
const char *pwd = "grootgroot";

IPAddress apIP(192, 168, 4, 3);  // your custome ip address for Nodemcu hotspot 
IPAddress netMask(255, 255, 255, 0);
IPAddress gateway(192, 168, 4, 1);
void setup() {

  Serial.begin(9600);
  WiFi.softAPConfig(apIP, gateway, netMask);
  WiFi.softAP(ssid, pwd);
  Serial.println("Wifi Started");
  Serial.print("IP Address");
  delay(1000);
  Serial.println(WiFi.softAPIP());
}

void loop() {

}


````
