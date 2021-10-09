<h1><a href= "https://github.com/ThuviksaM/Berry_Blob">Berry_Blob MasterMonitor Scripts &#128013;</a></h1>

<p>This repository has all my code for my enviroment monitoring RaspberryPi, named Berry_Blob &#128518;, you're welcome to explore around it! &#128270;</p>

<p>Wanna see the data Berry_Blob gathered? If so, <a href="https://io.adafruit.com/Thuviksa/dashboards/weather-monitor">here</a> is my AdaFruitIO dashboard. &#128187;</p>

<p>Thank you, <a href="https://github.com/tproffen">Dr. Thomas Proffen</a> and Amelie Nagle for all the guidance and debugging help, you both are magical. &#129412;</p>

<hr>

<h2>A Few Reminders</h2>

<p><b>&#128272; - Security Warning/Information</b></p>
<p><b>&#10071; - Important Information/Warning</b></p>

<p>You will need a <a href= "https://www.raspberrypi.org/products/raspberry-pi-zero-w/">Raspberry Pi Zero W</a> or another <a href= "https://www.adafruit.com/?q=Raspberry+Pi&sort=BestMatch">Raspberry Pi</a>, a Pimoroni <a href= "https://shop.pimoroni.com/products/enviro?variant=31155658489939">Enviro Hat</a>, an external temperature sensor, a CCS811 sensor, a breadboard (<a href= "https://www.adafruit.com/product/64">ex.</a>), a cooling fan (<a href= "https://www.adafruit.com/product/3368">ex.</a>), and an <a href= "https://io.adafruit.com/">AdaFruitIO</a> account, if you have all of these materials, you're set &#128077;, though you also have to connect your Pi to the internet your computer is on, after you get your Pi.</p>

<p><b>&#10071; Please notify me if you notice any typos or any other kind of error, or if you want to use the code in any of my MasterMonitor Scripts (I know, they're awesome &#128526;), thanks, I appreciate it. &#128516;</b></p>

<hr>

<h2><a href= "https://github.com/ThuviksaM/Berry_Blob/blob/main/sensor-wiring-img.jpg">Wiring the Sensors to the Pi</a></h2>

<p>Before you program anything you have to wire the sensor together...or nothing will work!</p>
<p>The image below is the wiring diagram <a href="https://github.com/tproffen">Dr. Proffen</a> used to help me and the others in the <a href= "https://www.orcsgirls.org/masterclass">#Enviro-MasterTeam</a> wire their sensors up!</p>

<p><b>&#10071; The intersecting lines (wires) are in the same row on the breadboard.</b></p>

<img src= "sensor-wiring-img.jpg" alt= "WiringDiagram" width="300" height="300">

<hr>

<h2><a href= "https://github.com/ThuviksaM/Berry_Blob/blob/main/MasterMonitorSensorScript.ipynb">MasterMonitor Sensor Script</a></h2>

<p>This is the MasterMonitor Script that controls all the sensor readings and sends them to AdaFruitIO cloud, which then puts the data into my dashboard's visual graphs and charts.</p>

<p>Make sure you change the AdaFruitIO_Username and the AdaFruitIO_Key variables to your username and key, and remove vvv (except for AdaFruitIO_Username, and AdaFruitIO_Key variables).</p>

    from dotenv import load_dotenv
    import os
    
    load_dotenv()
    
    AdaFruitIO_Username = os.envrion.get("ADAFRUIT_IO_USERNAME")
    AdaFruitIO_Key = os.environ.get("ADAFRUIT_IO_USERNAME")

<p>&#128272; <b>If you share your code somewhere, make sure to keep ^^^, and create a text file named .env in the EXACT folder you code/notebook is in to keep your ADAFRUIT_IO_USERNAME and ADAFRUIT_IO_KEY variables, you might, also, need to dowload the dotenv module, here is what you would need to put in a terminal to do that vvv.</b></p>

    pip3 install python-dotenv

<p>&#128272; <b>Here is what you would put in your .env text file , of course replacing your-username and your-key with your actual username and key vvv.</b></p>

    ADAFRUIT_IO_USERNAME = "your-username"
    ADAFRUIT_IO_KEY = "your-key"

<h4>&#128272; DO NOT git add the .env text file to GitHub.</h4>

<p>&#10071; <b>You can get your key by clicking the My Key tab on the AdaFruitIO website.</b></p>

<p>You can also change the below code to whatever long break you want your Pi to take before sending data to the AdaFruitIO Cloud.</p>

<hr>



<h2><a href= "https://github.com/ThuviksaM/Berry_Blob/blob/main/MasterMonitorGIFDisplayScript.ipynb">MasterMonitor GIF Display Script</a></h2>

<p>This MasterMonitor Script has the exact code you need to make a cute GIF appear on your display!</p>

<p>You can change the code below if you want to make a GIF other than the Party_Blob appear on your display.</p>

    image_file = "party_blob.gif"

<p><b>&#10071; Make sure your GIF file is in the same exact folder your code/notebook is in.</b></p>

<p>You can also edit or keep the print statements in this code vvv.</p>

    image = Image.open(image_file)
    print("Party_Blob is SO cute!!!")
    print("Drawing GIF, Stop This Cell To Exit!")

<hr>

<p>Try my teammates' enviroment monitoring code, they're awesome! &#128526;</p>
<p>- <a href= https://github.com/apzzd/EnviroPi>Ada's code</a></p>
<p>- <a href= https://github.com/tproffen/ORCSPiCamp>Dr. Proffen's code</a> - the actual master-code</p>