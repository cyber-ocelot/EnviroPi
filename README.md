<h1>Berry_Blob MasterMonitor Scripts &#128013;</h1>

<hr>

<p>Reminders: &#128272; - Security Warning   &#10071; - Important Information</p>

<hr>

<p>This is all my code for my enviroment monitoring RaspberryPi, named Berry_Blob &#128518;, you're welcome to explore around it! &#128270;</p>

<p>Wanna see the data Berry_Blob gathered? If so, <a href="https://io.adafruit.com/Thuviksa/dashboards/weather-monitor">here</a> is my AdaFruitIO dashboard. &#128187;</p>

<h4>&#10071; Please contact me if you want to use my code.</h4>

<p>Thank you, <a href="https://github.com/tproffen">Dr. Thomas Proffen</a> and Amelie Nagle for all the guidance and debugging help, you both are magical. &#129412;</p>

<hr>

<h2>MasterMonitor Sensor Script</h2>

<p>This is the MasterMonitor Script that controls all the sensor readings and sends them to AdaFruitIO cloud, which then puts the data into my dashboard's visual graphs and charts.</p>

<p>Make sure you change the AdaFruitIO_Username and the AdaFruitIO_Key variables to your username and key, and remove vvv (except for AdaFruitIO_Username, and AdaFruitIO_Key variables)</p>

<h4>&#10071; You can get your key by clicking the My Key tab on the AdaFruitIO website.</h4>

    from dotenv import load_dotenv
    import os
    
    load_dotenv()
    
    AdaFruitIO_Username = os.envrion.get("ADAFRUIT_IO_USERNAME")
    AdaFruitIO_Key = os.environ.get("ADAFRUIT_IO_USERNAME")

<h4>&#128272; If you share your code somewhere, make sure to keep ^^^, and create a text file named .env to keep your ADAFRUIT_IO_USERNAME and ADAFRUIT_IO_KEY variables, like this vvv, DO NOT git add the .env text file to GitHub.</h4>

    ADAFRUIT_IO_USERNAME = "your-username"
    ADAFRUIT_IO_KEY = "your-key"

<hr>



<h2>MasterMonitor GIF Display Script</h2>

<p>This MasterMonitor Script has the exact code you need to make a cute GIF appear on your display!</p>

<p>You can change the code below if you want to make a GIF other than the Pary_Blob appear on your display.</p>

    image_file = "party_blob.gif"

<h4>&#10071; Make sure your GIF file is in the same exact folder your code is in.</h4>

<p>You can also edit or keep the print statements in this code vvv</p>

    image = Image.open(image_file)
    print("Party_Blob is SO cute!!!")
    print("Drawing GIF, Stop This Cell To Exit!")