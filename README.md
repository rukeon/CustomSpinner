# CustomSpinner [![Release](https://jitpack.io/v/piotrek1543/CustomSpinner.svg)](https://jitpack.io/#iotrek1543/CustomSpinner) [![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-CustomSpinner-green.svg?style=true)](https://android-arsenal.com/details/1/4014)

Spinner with hint and open/closed listener that works with jitpack.io.

![alt tag](assets/ezgif-3622619846.gif)

Check this site for specific release: https://jitpack.io/#piotrek1543/CustomSpinner

##Setup:

Add it to your build.gradle with:
```gradle
allprojects {
    repositories {
        maven { url "https://jitpack.io" }
    }
}
```
and:

```gradle
dependencies {
    compile 'com.github.piotrek1543:CustomSpinner:0.1'
}
```

How to use it?
--------------------

- initialization of CustomSpinner

`CustomSpinner` takes two arguments: `String[] values` and `String prompt_text` which is optional and it would be added to `ArrayAdapter` as initial item (hint). 

```
    CustomSpinner colorSpinner = (CustomSpinner) findViewById(R.id.number_spinner);
    String[] types = getResources().getStringArray(R.array.number_array);
    colorSpinner.initializeStringValues(types, getString(R.string.color_spinner_hint));
```
 

- using open/close listener:
```
    colorSpinner.setSpinnerEventsListener(new CustomSpinner.OnSpinnerEventsListener() {
        @Override
        public void onSpinnerOpened() {
            response.setText(R.string.action_spinner_open);
        }

        @Override
        public void onSpinnerClosed() {
            response.setText(R.string.action_spinner_closed);
        }
    });
```
Issues
------

Feel free to submit issues and enhancement requests.

Contributing
------------

Please refer to each project's style guidelines and guidelines for submitting patches and additions. In general, we follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

License
-------

    Copyright 2016 Piotr Ekert

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
