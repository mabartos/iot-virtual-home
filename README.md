# IoT Virtual Home

Subject: 11769 - Connectivitat i Integració de Sistemes a IoT

### Architecture of the system

<img width="617" src="img/diagram.png" alt="Diagram"/>

### Development
We can directly store separate Node-RED flows directly in the repository. 
File `flows.json` contains all exported Node-RED flows.

### How to run
1. Run MQTT Broker (configuration is for localhost:1883) - you can run `mosquitto`
2. Fetch all dependencies - `npm install`
3. Start Node-Red - `npm start`