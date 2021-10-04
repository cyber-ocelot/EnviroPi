<img src= "https://cdn.shopify.com/s/files/1/0174/1800/products/enviro-lifestyle-1_1024x1024.jpg?v=1573820030" alt= "Pimoroni.com" width= "500" height= "500" float= "right">

<h1><a href= "https://github.com/ThuviksaM/Berry_Blob">Berry_Blob MasterMonitor Scripts &#128013;</a></h1>

<p>This repository has all my code for my enviroment monitoring RaspberryPi, named Berry_Blob &#128518;, you're welcome to explore around it! &#128270;</p>

<p>Wanna see the data Berry_Blob gathered? If so, <a href="https://io.adafruit.com/Thuviksa/dashboards/weather-monitor">here</a> is my AdaFruitIO dashboard. &#128187;</p>

<p>Thank you, <a href="https://github.com/tproffen">Dr. Thomas Proffen</a> and Amelie Nagle for all the guidance and debugging help, you both are magical. &#129412;</p>

<hr>

<h2>A Few Reminders</h2>

<h4>&#128272; - Security Warning/Information</h4>
<h4>&#10071; - Important Information/Warning</h4>

<p>You will need a <a href= "https://www.raspberrypi.org/products/raspberry-pi-zero-w/">Raspberry Pi Zero W</a> or another <a href= "https://www.adafruit.com/?q=Raspberry+Pi&sort=BestMatch">Raspberry Pi</a>, a Pimoroni <a href= "https://shop.pimoroni.com/products/enviro?variant=31155658489939">Enviro Hat</a>, an external temperature sensor, a CCS811 sensor, a breadboard (<a href= "https://www.adafruit.com/product/64">ex.</a>), a cooling fan (<a href= "https://www.adafruit.com/product/3368">ex.</a>), and an <a href= "https://io.adafruit.com/">AdaFruitIO</a> account, if you have all of these materials, you're set. &#128077;</p>

<h4>&#10071; Please notify me if you notice any typos or any other kind of error, or if you want to use any of my MasterMonitor Scripts (I know, they're awesome &#128526;), thanks, I appreciate it. &#128516;</h4>

<hr>

<h2>Wiring the Sensors to the Pi</h2>

<p>Before you program anything you have to wire the sensor together...or nothing will work!</p>
<p>The image below is the wiring diagram <a href="https://github.com/tproffen">Dr. Proffen</a> used to help me and the others in the #enviro-masterteam wire their sensors up!</p>

<h4>&#10071; The intersecting lines (wires) are in the same row on the breadboard.</h4>

<img src= "sensor-wiring-img.jpg" alt= "WiringDiagram" width="400" height="400">

<hr>

<h2><a href= "https://github.com/ThuviksaM/Berry_Blob/blob/main/MasterMonitorSensorScript.ipynb">MasterMonitor Sensor Script</a></h2>

<p>This is the MasterMonitor Script that controls all the sensor readings and sends them to AdaFruitIO cloud, which then puts the data into my dashboard's visual graphs and charts.</p>

<p>Make sure you change the AdaFruitIO_Username and the AdaFruitIO_Key variables to your username and key, and remove vvv (except for AdaFruitIO_Username, and AdaFruitIO_Key variables).</p>

    from dotenv import load_dotenv
    import os
    
    load_dotenv()
    
    AdaFruitIO_Username = os.envrion.get("ADAFRUIT_IO_USERNAME")
    AdaFruitIO_Key = os.environ.get("ADAFRUIT_IO_USERNAME")

<h4>&#128272; If you share your code somewhere, make sure to keep ^^^, and create a text file named .env in the EXACT folder you code/notebook is in to keep your ADAFRUIT_IO_USERNAME and ADAFRUIT_IO_KEY variables, here is what you would put vvv.</h4>

    ADAFRUIT_IO_USERNAME = "your-username"
    ADAFRUIT_IO_KEY = "your-key"

<h4>&#128272; DO NOT git add the .env text file to GitHub.</h4>

<h4>&#10071; You can get your key by clicking the My Key tab on the AdaFruitIO website.</h4>

<hr>



<h2><a href= "https://github.com/ThuviksaM/Berry_Blob/blob/main/MasterMonitorGIFDisplayScript.ipynb">MasterMonitor GIF Display Script</a></h2>

<p>This MasterMonitor Script has the exact code you need to make a cute GIF appear on your display!</p>

<p>You can change the code below if you want to make a GIF other than the Party_Blob appear on your display.</p>

    image_file = "party_blob.gif"

<h4>&#10071; Make sure your GIF file is in the same exact folder your code/notebook is in.</h4>

<p>You can also edit or keep the print statements in this code vvv</p>

    image = Image.open(image_file)
    print("Party_Blob is SO cute!!!")
    print("Drawing GIF, Stop This Cell To Exit!")

