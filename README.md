# alexa-radiothermostat

This is a module for [node-alexa-server](https://github.com/bbrookfield/node-alexa-server) to integrate with [Radio Thermostats](http://www.radiothermostat.com/) 

####Getting started
1. Make sure you have downloaded and setup your [node-alexa-server](https://github.com/bbrookfield/node-alexa-server)
2. If you do not already have an `app_modules` directory in your server project, you need to create one
3. Clone this project into that directory
4. Setup your Alexa skill
5. Configure your intents
  
  ```
  {
  "intents": [
    {
    "intent": "getTemp",
      "slots": [{
        "name": "getTemperature",
        "type": "AMAZON.LITERAL"
      }]
    },
    {
    "intent": "setHeat",
      "slots": [{
        "name": "setHeating",
        "type": "AMAZON.NUMBER"
      }]
    },
    {
    "intent": "setCool",
      "slots": [{
        "name": "setCooling",
        "type": "AMAZON.NUMBER"
      }]
    },
    {
    "intent": "setOff"
    },
    {
    "intent": "setFanOn"
    },
    {
    "intent": "setFanAuto"
    },
    {
    "intent": "setHoldOn"
    },
    {
    "intent": "setHoldOff"
    },
    {
    "intent": "incTemp",
      "slots": [{
        "name": "increaseTemp",
        "type": "AMAZON.NUMBER"
      }]
    },
    {
    "intent": "decTemp",
      "slots": [{
        "name": "decreaseTemp",
        "type": "AMAZON.NUMBER"
      }]
    }
  ]
}
    
  ```
6. Configure your utterances

  ```
  setOff to turn off thermostat
setOff to turn thermostat off
setOff set thermostat to off
setFanOn to turn on fan
setFanOn to turn on blower
setFanOn to turn blower on
setFanOn to turn fan on
setFanAuto to turn off fan
setFanAuto to turn off blower
setFanAuto to turn blower off
setFanAuto to turn fan off
setFanOn to set fan to on
setFanOn to set blower to on
setFanAuto to set fan to off
setFanAuto to set fan to auto
setFanAuto to set blower to auto
setHoldOn to turn on hold
setHoldOn to turn hold on
setHoldOn to set hold to on
setHoldOff to turn off hold
setHoldOff to turn hold off
setHoldOff to set hold to off
setHeat to set heat to {setHeating}
setCool to adjust cool to {setCooling}
setHeat to adjust heat to {setHeating}
setCool to set cool to {setCooling}
setCool to adjust air conditioning to {setCooling}
setCool to set air conditioning to {setCooling}
setCool to set air to {setCooling}
setCool to adjust air to {setCooling}
setHeat to adjust the heat to {setHeating}
setCool to adjust the air conditioning to {setCooling}
setCool to set ac to {setCooling}
setCool to adjust ac to {setCooling}
setCool to set air conditioning to {setCooling}
getTemp what is the temperature
getTemp what is temperature
getTemp what's the temperature
getTemp say the temperature
getTemp tell me the temperature
getTemp tell me temperature
incTemp raise target temperature by {increaseTemp}
incTemp increase target temperature by {increaseTemp}
decTemp lower target temperature by {decreaseTemp}
decTemp decrease target temperature by {decreaseTemp}
  ```
