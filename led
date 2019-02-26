import time
import requests

from libraries.RGB_LED import RGB_LED
from libraries.RGB_LED.RGB_LED.COLOR import Color

settingUrl='http://intro-to-iot.herokuapp.com/api/settings'

red_pin = 17
green_pin = 27
blue_pin = 22
is_common_anode=True

rgb = RGB_LED(red_pin, green_pin, blue_pin,is_common_anode)

color = Color()

r = 0
g = 0
b = 0

delay = .1

while True:
    
    settings = requests.get(settingUrl)
    # print settings.json()
    settings = settings.json()

    color.set_color_string(settings['lightColor'])
    rgb.set_color(color)

    time.sleep(delay)
