## About
This project is forked from (https://github.com/JackyAndroid)'s AndroidChromium repository. Through reading this project code, I will try to figure out chrome browser's basic architecture and understand android development better. While I reading the code, I will write down some notes in this README file. Maybe I will make some modification based this version to build a browser I prefer.

#### Application entry point

##### `ChromeApplication`'s `onCreate`
This is called once per `ChromeApplication` instance, which get created per process (browser OR renderer). It do these things.

* Record entry point time.

* Set show keyboard delegate.

* Init account manager.

* Initialize and install client name generator.

* Set log level.

* Set up the identification generator for sync.

##### General launch process

![Chrome general launch process](https://dl.dropboxusercontent.com/u/83663714/Figures/android_chrome_basic_launcher_process.png)

