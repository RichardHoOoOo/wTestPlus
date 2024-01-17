We publish the wTest+ tool and the evaluation results in this page.

# Subjects 
* Open-source apps ([download](https://drive.google.com/file/d/1B2DPTC9pF6KmcTuEWSgI1ctONDHzmXO-/view?usp=sharing))

The following table lists the 38 open-source Android apps used in our evaluation.

| Index | Package | Index | Package |
| --- | --- | --- | --- | 
| 1 | app.simple.inure | 20 | de.taz.android.app.free |
| 2 | ch.rmy.android.http_shortcuts.debug | 21 | fr.free.nrw.commons |
| 3 | com.activitymanager | 22 | im.fdx.v2ex.debug |
| 4 | com.boardgamegeek | 23 | io.github.wulkanowy |
| 5 | com.dar.nclientv2.debug | 24 | ml.docilealligator.infinityforreddit |
| 6 | com.ds.avare | 25 | name.boyle.chris.sgtpuzzles |
| 7 | com.flxrs.dankchat | 26 | net.bible.android.activity |
| 8 | com.gh4a | 27 | net.osmand.plus |
| 9 | com.github.k1rakishou.chan | 28 | nl.asymmetrics.droidshows |
| 10 | com.ichi2.anki | 29 | org.andstatus.app |
| 11 | com.kidozh.discuzhub | 30 | org.catrobat.paintroid |
| 12 | com.manimarank.spell4wiki | 31 | org.koitharu.kotatsu |
| 13 | com.nextgis.mobile | 32 | org.openhab.habdroid |
| 14 | com.nutomic.syncthingandroid | 33 | org.quantumbadger.redreader |
| 15 | de.blau.android | 34 | org.runnerup.free |
| 16 | de.danoeh.antennapod | 35 | org.wikipedia.alpha |
| 17 | de.freehamburger.debug | 36 | org.woheller69.omweather |
| 18 | de.herrmann_engel.rbv | 37 | org.woheller69.weather |
| 19 | de.tap.easy_xkcd | 38 | xyz.zedler.patrick.grocy |

# Coverage results
* WebView-specific property coverage, WebView API call site coverage, and code coverage for open-source apps ([link](https://docs.google.com/spreadsheets/d/1o6YrTSbTqygDV3v0rRdAf3w3tMDGeQxi8BbG1HWhiEY/edit?usp=sharing))

# Detected bugs

* bug1 ([link](https://github.com/flex3r/DankChat/issues/238))
* bug2 ([link](https://github.com/woheller69/omweather/issues/49))
* bug3 ([link](https://github.com/woheller69/omweather/issues/50))
* bug4 ([link](https://github.com/Docile-Alligator/Infinity-For-Reddit/issues/1368))
* bug5 ([link](https://github.com/ccomeaux/boardgamegeek4android/issues/181))
* bug6 ([link](https://github.com/andstatus/andstatus/issues/551))
* bug7 ([link](https://github.com/andstatus/andstatus/issues/552))
* bug8 ([link](https://github.com/chrisboyle/sgtpuzzles/issues/626))
* bug9 ([link](https://github.com/kidozh/DiscuzHub/issues/46))
* bug10 ([link](https://github.com/kidozh/DiscuzHub/issues/47))
* bug11 ([link](https://github.com/kidozh/DiscuzHub/issues/48))
* bug12 ([link](https://github.com/kidozh/DiscuzHub/issues/46))
* bug13 ([link](https://github.com/ankidroid/Anki-Android/issues/13230))
* bug14 ([link](https://github.com/Hamza417/Inure/issues/245))
* bug15 ([link](https://github.com/fan123199/v2ex-simple/issues/16))
* bug16 ([link](https://jira.catrob.at/browse/PAINTROID-695))
* bug17 ([link](https://github.com/openhab/openhab-android/issues/2845))
* bug18 ([link](https://github.com/Dar9586/NClientV2/issues/548))
* bug19 ([link](https://github.com/Dar9586/NClientV2/issues/548))
* bug20 ([link](https://github.com/woheller69/weather/issues/81))
* bug21 ([link](https://github.com/woheller69/weather/issues/82))
* bug22 ([link](https://github.com/jonasoreland/runnerup/issues/1094))
* bug23 (reported by email. WebViewActivity in de.taz.android.app.free) [bug23.pdf](https://github.com/RichardHoOoOo/wTestPlus/files/13951192/bug23.pdf)
* bug24 (DataPolicyActivity in de.taz.android.app.free) [bug24.pdf](https://github.com/RichardHoOoOo/wTestPlus/files/13950976/bug24.pdf)
* bug25 (IssueViewerActivity in de.taz.android.app.free) [bug25.pdf](https://github.com/RichardHoOoOo/wTestPlus/files/13951427/bug25.pdf)
* bug26 (SearchActivity in de.taz.android.app.free) [bug26.pdf](https://github.com/RichardHoOoOo/wTestPlus/files/13951486/bug26.pdf)
* bug27 (BookmarkViewerActivity in de.taz.android.app.free) [bug27.pdf](https://github.com/RichardHoOoOo/wTestPlus/files/13951593/bug27.pdf)
* bug28 (PreferenceActivity in app.simple.inure) [bug28.pdf](https://github.com/RichardHoOoOo/wTestPlus/files/13951746/bug28.pdf)

# Tool
Our tool is composed of 3 parts. The first part staticly builds the GUI component transition graph. The second part instruments an app. The third part generates tests for the instrumented app. But before testing an app, a customized Android OS needs to be loaded by Android emulators or real devices.

## Customized Android OS
The instrumented app needs to run on a customized Android system because we add one more ID field in `java.lang.Object` in order to ease the variable tracking. It is very simple to use our customized Android system image, you just need to follow the following 2 steps
* Download our customized [system.img](https://drive.google.com/file/d/1K4_3TDcAYvzyoeVxSDTUEd3SFQxGDwk9/view?usp=share_link), [ramdisk.img](https://drive.google.com/file/d/1AbVckf1BeDMSNUppyyjhZj-IqUh4OhrW/view?usp=share_link), [VerifiedBootParams.textproto](https://drive.google.com/file/d/1PSJi8xJnUG6SRXpV3K--xg9ZoPCnoL41/view?usp=share_link) (They are for Android 10)
* Replace the original `system.img`, `ramdisk.img`, `VerifiedBootParams.textproto` in your Android SDK with the downloaded files

Usually, these files are placed under `<Android_SDK_Root>/system-images/android-29/google_apis/x86`

Once you have finished the above two steps, you can try to start the Android emulator as usual.

## Static analysis ([download](https://drive.google.com/file/d/1x9QGjp0gQvC6H5cZcJdeum9eWtf9ff6u/view?usp=sharing))
### Requirements
* Java 1.8 or above
### Steps to use
* Create a folder for an app under test. The folder name should be the app's package name (We have created a folder for `org.woheller69.weather` under `<path_to_tool>/apps`).
* Run `sh graph.sh APP_FOLDER APP_PACKAGE_NAME NON_LIB_PKGS` to statically build the GUI component transition graph for an app. `NON_LIB_PKGS` is an array of package names separated by "," that are used to filter out library code in an app (e.g., if an app's application code is in `a.b.c` and `a.b.d`, `NON_LIB_PKGS` should be `a.b.c,a.b.d`). An example command can be `sh graph.sh apps/org.woheller69.weather org.woheller69.weather org.woheller69.weather`).


## Instrumentation ([packaged together with static analysis]())
### Requirements
* Java 1.8 or above
* Python 2 or 3 (We have tested on Python 2.7.16 and Python 3.6.8)
* Node.js (We have tested on v16.13.2, v12.16.2, and v10.16.0. You may find these versions [here](https://nodejs.org/en/download/releases/). If you are using a Linux-based OS, you may install node by following the steps [here](https://www.digizol.com/2017/08/nodejs-install-no-root-sudo-permission-linux-centos.html))

### Steps to use
* Run `sh instrument.sh APP_FOLDER APP_PACKAGE_NAME PORT_NUM NON_LIB_PKGS` to instrument an app. `PORT_NUM` is a port used by the instrumented app to communicate with a nodejs server to instrument dynamically-loaded JavaScript code. It is recommended to be set as 3016, 3018, 3020, ..., etc. An example command can be `sh instrument.sh apps/org.woheller69.weather org.woheller69.weather 3016 org.woheller69.weather`).
* When instrumentation finishes, you can see an `output` folder under the `APP_FOLDER`. The apk file whose name ends with `-aligned-debugSigned.apk` is the instrumented apk.

## Test generation (wTest) ([download]())
### requirements
* `export JAVA_HOME=YOUR_JAVA_HOME` (example: `export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_121.jdk/Contents/Home/`)
* `export ANDROID_HOME=YOUR_ANDROID_HOME` (example: `export ANDROID_HOME=/Library/Android/sdk`)
* `export PATH=$PATH:${ANDROID_HOME}`
* `export PATH=$PATH:<path_to_wTest>/node_modules/.bin` (make sure you have downloaded `wTest`)
* `export PATH=$PATH:${ANDROID_HOME}/emulator`
* `export PATH=$PATH:${ANDROID_HOME}/platform-tools`
* build-tools 27.0.3 (for ComboDroid) and 29.0.3 are required (they are usually at `${ANDROID_HOME}/build-tools`)

### Steps to use
* Enter `<path_to_Instrumentation>/js` and run `sh launchServer.sh PORT_NUM`. This nodejs server is registered on a `PORT_NUM` in order to recevice JavaScript code that is dynamically constructed in the app under test. The server is responsible for instrumenting the js code and sending the instrumented code back to the app. `PORT_NUM` should be the same as the one used when instrumenting the app. An example command can be `sh launchServer.sh 3016`
* Launch Appium by `appium -p APPIUM_PORT` (example: `appium -p 4723`)
* Launch an Android emulator
* Enter `<path_to_wTest>` and run `sh test.sh STRATEGY PATH_TO_APP_FOLDER TIME_LIMIT ANDROID_SDK_PATH EMULATOR_ID APPIUM_PORT APP_TYPE AVD_NAME BUILD_TOOLS_VERSION SYSTEM_PORT`. `STRATEGY` can be `wVar` (stands for wTest), or `wDroid`, or `api` (stands for wTest-API), or `QTesting`, or `ComboDroid`, or `Fastbot` (stands for Fastbot2). `AVD_NAME` is the name of the android emulator. `BUILD_TOOLS_VERSION` must be set as 29.0.3. `SYSTEM_PORT` is a port used by appium if you test multiple apps in parallel. It is recommended to be set as 8200, 8201, 8202, etc. An example command can be 
`sh test.sh wVar <path_to_Instrumentation>/apps/org.wikipedia 3600 ${ANDROID_HOME} emulator-5554 4723 OPEN_SOURCE emulator0 29.0.3 8200`
* When reaching the time limit, you can see the output under `<path_to_wTest>/output/<STRATEGY>/<APP_PACKAGE_NAME>` (e.g., `<path_to_wTest>/output/wVar/org.wikipedia`). Under this folder, `coverage.txt` contains the covered WebView-specific properties and WebView API call sites over 60 minutes (time0, time1, ..., time59 means 1 minute, 2 minute, ..., 60 minute). Code coverage is also reported.
