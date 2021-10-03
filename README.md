<h1>Berry_Blob MasterMonitor Scripts &#128013;</h1>

<p>Reminders: &#128272; - Security Warning   &#10071; - Important Information</p>

<p>This is all my code for my enviroment monitoring RaspberryPi, named Berry_Blob &#128518;, you're welcome to explore around it! &#128270;</p>

<p>Wanna see the data Berry_Blob gathered? If so, <a href="https://io.adafruit.com/Thuviksa/dashboards/weather-monitor">here</a> is my AdaFruitIO dashboard. &#128187;</p>

<h4>&#10071; Please contact me if you want to use my code.</h4>

<p>Thank you, <a href="https://github.com/tproffen">Dr. Thomas Proffen</a> and Amelie Nagle for all the guidance and debugging help, you both are magical. &#129412;</p>

<hr>



<h2>MasterMonitor Sensor Script</h2>

<p>This is the MasterMonitor Script that controls all the sensor readings and sends them to AdaFruitIO.</p>

<p>Make sure you change the AdaFruitIO_Username and the AdaFruitIO_Key variables to your username and key, and remove vvv (except for AdaFruitIO_Username, and AdaFruitIO_Key variables)</p>

    from dotenv import load_dotenv
    import os
    
    load_dotenv()
    
    AdaFruitIO_Username = os.envrion.get("ADAFRUIT_IO_USERNAME")
    AdaFruitIO_Key = os.environ.get("ADAFRUIT_IO_USERNAME")

<h4>&#128272; If you share your code somewhere, make sure to keep ^^^, and create a text file named .env to keep your ADAFRUIT_IO_USERNAME and ADAFRUIT_IO_KEY variables, DO NOT git add the .env text file to GitHub.</h4>

<hr>



<h2>MasterMonitor GIF Display Script</h2>

<p>Wanna make a cute GIF appear on your display? If so, this script has the exact code you're looking for!</p>

<p>You can change the below code if you want to make a GIF other than the Pary_Blob appear on your display.</p>

    image_file = "party_blob.gif"

<h4>&#10071; Make sure your GIF file is in the same exact folder your code is in.</h4>