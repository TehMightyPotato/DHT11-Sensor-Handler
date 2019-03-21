## DHT11-Sensor-Handler
A little python script to read values from a Adafruit DHT11 sensor and to store them in a Excel spreadsheet and send them to a server via POST

## Usage
* Run with python3 and add the following environment variables:
  * `url=<your_server_url>` defaults to 127.0.0.1 if not specified
  * `file_path=<your_file_path>.xlsx` the path the Excel spreadsheet will be stored. Defaults to `./dump.xlsx` 
  * `id=<your_pi_id>` is sent with POST requests to the server. Ignore unless you use my nodejs API for this application found [here](https://github.com/TehMightyPotato/DHT11-Database-API)
  * `sleep=<your_sleep_value>` the time between two polls. Defaults to 300s
  * `pin=<your_DHT11_pin>` the data-pin for your DHT11 connection. Defaults to GPIO23
  
Your full command will look something like this:

`url=127.0.0.1 file_path=my_file.xlsx id=living_room sleep=600 pin=23 python3 DHT11-Reader.py`
