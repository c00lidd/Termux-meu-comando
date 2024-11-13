# Termux-meu-comando
git push origin main
chmod +x weather.sh
#Termux
./weather.sh
#!/bin/bash
CITY="Nazaré"
API_KEY="sua_chave_de_api"
curl -s "http://api.openweathermap.org/data/2.5/weather?q=$CITY&appid=$API_KEY&units=metric" | jq '. | {temp: .main.temp, description: .weather[0].description}'
nano weather.sh
pkg install curl

