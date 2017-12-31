# Using Android Studio
open `build.gradle`

Do **not** update Gradle to >4.0!

## For running on desktop
* `Run -> Edit Configurations...`
* Click plus (+) and add `Application`
* add `Main class` (DesktopLauncher)
* change working directory to ...android/assets
* `Use classpath of module` to `desktop`
* Click `Apply` and `Run`.

## For running on Android
Select configuration and run.

## For running IOS
* [Install the RoboVM IntelliJ IDEA plugin or Intel Multi-OS Engine](http://robovm.mobidevelop.com).
* `Run -> Edit Configurations...`, click the plus (+) button and select `RoboVM iOS`.
* Set the `Name` to `iOS`.
* The `Module` should be set to `ios` if not already done.
* To run on the simulator select `Simulator` as radio button and select a Device.
* Click `Apply` and `Run`.

## For running html
`View -> Tool Window -> Terminal`, in the terminal, make sure you are in the root folder of your project. Then execute `gradlew.bat html:superDev` (Windows) or `./gradlew html:superDev` (Linux, Mac OS X).
This will take a while, as your Java code is compiled to Javascript.
Once the code is compiled it will start something for GWT on port 9876 and go to [http://localhost:8080/html](http://localhost:8080/html) to run the app.
When you change any of your Java code or assets, just click the `SuperDev refresh` button while you are on the site and the server will recompile your code and reload the page!
To kill the process, simply press `CTRL + C` in the terminal window.