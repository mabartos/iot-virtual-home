# IoT Virtual Home

Subject: 11769 - Connectivitat i Integració de Sistemes a IoT

### Architecture of the system

<img width="617" src="img/diagram.png" alt="Diagram"/>

### Development
We can directly store separate Node-RED flows directly in the repository. 
File `flows.json` contains all exported Node-RED flows.

### How to run
1. Run MQTT Broker (configuration is for localhost:1883) - you can run `mosquitto`
2. Run InfluxDB (next section)
2. Fetch all dependencies - `npm install`
3. Start Node-Red - `npm start`
4. Navigate to `localhost:1880`

#### InfluxDB

##### General
1. Download InfluxDB 2.0 from official website - https://portal.influxdata.com/downloads/
2. Run InfluxDB Daemon - `influxd` script in the downloaded folder

##### First set up
1. Navigate in browser to `localhost:8086`
2. Set your username and password
3. Set initial organization name to `alinaMartin`
4. Set initial bucket name to `home1`
5. Click to 'Configure Later'
6. Go to `localhost:8086` and navigate to `Load Data` and then `API Tokens`
WARNING: **The API token is visible only once!**
7. If you're able to see your account's API token, save it
8. If not, just click to `Generate API Token` and create `All Access API Token` and save it
9. In the Node-Red (`localhost:1880`) go to some InfluxDB element and configure the instance
<img width="417" src="img/influxSettingsNodeRed.png" alt="Diagram"/>
10. Add the saved token there
11. Click `Deploy`

##### Normal startup
1. Just run the `influxd` daemon
2. You can find received data on `localhost:8086` in section Data Explorer

