## Objective:
		* To develop a non-expensive Home control/Automation Solution
		* To have the same kind of support for pelothra of Devices
		* Easy one-time setup with unlimited expandability
		* Incorporating AI for Security
		* Develop an app for constant monitoring with greater control to the user	

#### One must understand the reasoning behind  to understand this project better. India is a country with one of the biggest population. It is a developing nation and is shifting towards technology slowly. Nature is being affected by this changing landscape. We see cities like Delhi, where a clear sky is like a Day of Warmth in Antarctica. Pollution has been our problem since generation, but this is high time we put a check on it. One of the major producer of pollution is generation of electricity.   <br>
#### Major sources of Energy production have not been shifted to renewable sources for varied reasons. We have exsisting smart solutions but not limited to Google Home, Amazon Alexa and so on. One thing that strikes me the most is the affordability. Aisan contries are still developiing and the installation charges as well monthly recuring charges alone for operating these devices are high. Moreover smart devices which can be operated using these devices are very expensive at least.  
#### One might be thinking now, how does clean air related to all this? An average household consumes 200-300 units per month. Everyday, cummulative 2/3 hours of appliances (considering average consumtion of 50watts) are operated for no use. considering 150 watts of electricity being wasted per day, it will be 4500 watts(i.e. merely 4.5kW) Consider a population size of let's say 1lakh out of 1.5lakh who aren't aware of smart appliances or just find them two expensive to buy, su 4.5*100000 = 450000kW = 450mW. Where do you think this electricity comes from? Most of it directly from burning coal.  <br>
### I suppose this is where this project could be best suited. This project overlaps the exsisting home connections and bridges the gap between our analog devices with the digital.
## Implementation
### This can be implemented in 2 levels: 
### 1. At the circuit
### 2. An Application on a smartphone
#### 1. At the circuit we use the master-slave configuration. The GSM module/wifi-module whichever the user choose needs to be connected only at the master controller. All the slave modules are connected using RF module. The data received by either GSM Module/wifi-module is sent serially to the master controller. It checks each digit serially. Consider an example: ***#Am00100A*** Here, # is the unique character that can be used to recognize if the data is garbage or useful. The second character 'm' represents master. '001' stands for the numbered controller. In the case of master it will always be '001'. but in case of slaves, there can be a total of 128 modules. The next '0' defines the pin number the device is interfaced with and the next digit represents '0' for 'OFF' and '1' for 'ON'. The last character 'A' is similar to the first character '#' to mark the end.
#### The vision to take this further is by defining for how long we want the device to be ON or what values should be sent to the IR blaster. Let's understand the later example. We all have seen remote control apps on mobile phones in which we need to choose the the right company and type. Each has its own unique set of codes. Here, comes the mobile application into play.
#### 2. Instead of making the controller complicated with 'n' number of features, it will make it more expensive as it will require more memory and supporting devices. Coming back to the application, we can set up the correct brand and make model of a device. When ever we choose to ON/OFF the devices, we simple press ON/OFF but on the inside, the application will send the data in the spedific format that will define the values given to the IR blaster. Similarly, we can interface devices.
#### The user is free to define as many rules as possile on the application. If he/she want to save water by strictly monitoring it by using an IoT based solution or wants to automatically turn OFF devices OR controlling the temperature of AC or speed of Fan at no additional Infrastructural costs. It can save a lot of electricity and in term contribute to the safe and clean air. 
#### While handling so much sensitive data, one must not forget security. For this, the data between the devices can be encypted using BlockChain. BlockChain being one of the most secure systems established, we could easiliy safe guard the data maintaining the privacyof the users.

#### For more advanced options, we could also include NodeMCU to provide firmware updates to the users as new devices keep adding to the portfolio.
#### A basic version of this project has already been verified on Proteus and is working perfectly.

	
## Application

#### With this approach, the possibilities are endless - Alarm  temperature sensor, air quality sensor, smoke alarm, water pump for watering plants, preconfigured washing machine on/off using robotic finger, baby awake monitor message, gas and co detector, security cameramotion sensor, interfacing rtc and timer generation, soil moisture. It can be implemented at home, offices, warehouses or any other place for that matter. There is no requirement for any new appliances. It can work on exsisting infrastructure at a minimal installation cost. There won't be any need to change the code to add a new appliance. With the addition of blockchain we can ensure security and privancy of the user data.
