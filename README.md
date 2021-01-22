Click [here](https://www.youtube.com/watch?v=VPdPOVL8c1Q&list=PL9gEr35J45czlRLHXhA3jShGG_jIrRprJ) to see the video series for how Karen was made.

![Karen](https://alfredo.lol/static/karen/img/karen_small.png)
### open source voice assistant

## Installing
Karen is a standalone Python program, which means that it runs like any other Python program or script. Python 3.5 or newer is required. 

1) Clone or download this repository
2) Install the python dependencies using pip
```
pip3 install -r requirements.txt
```
4) Install the system dependencies. If you want to deploy this on a Raspberry Pi system or a similar Debian distribution, the install_raspberry_pi_requirements.sh file is included to make this easier.
```
sudo install_raspberry_pi_requirements.sh
```
3) Run Karen
```
python3 Karen.py
```

## configuring
Karen can be configured via the `config.json` file in Karen's root directory. The config file will be automatically created during Karen's initial run. Below is an example of the config file:

```
{
  "settings": {
    "names": [
      "karen",
      "kevin"
    ],
    "lang": "en"
  },
  "addons": []
}
```
Karen has a few configurable settings:
`names` [array of strings]: A list of names that will be used as the trigger word to activate the voice assistant.

`land` [string]: The ISO 639-1 language code to be used. This is powered by Google translate.

`addons` [array of objects]: The addons setting is where you will find all your installed add-ons. This setting is automatically populated by Karen at run time, which means that every time you install a new add-on, Karen must be restarted. This is also where you can configure the settings for a specific add-on if an add-on you have installed supports user settings. 

## Add-ons
The functionality for Karen comes from its add-ons, which are Python programs specifically made for use with Karen. [Karen has an add-on repository with add-ons available for you to install ](https://alfredo.lol/karen/). All of the add-ons in this repository are open source and are made by Karen's community.

Add-ons can be installed manually, using Karen's add-on manager, or via the [Karen]() app. For more information on creating and installing add-ons, you can [read the documentation](https://alfredo.lol/karen/docs/0.0.1).

## More
As mentioned before, [Karen also has a mobile app]() that can be used to install and configure add-ons. This mobile app is also open source and cross-platform (IOS & Android) made using React Native.

If you want to deploy Karen on a raspberry pi and create an enclosure for it, [open source stl and openSCAD files for 3D printing are available]().