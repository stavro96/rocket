# Rocket
A SharedPreferences library for Android , to speed up development

# Download 

### Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:

```Groovy
allprojects {
	repositories {
		...
		maven { url 'https://jitpack.io' }
	}
}
```
### Step 2. Add the dependency

```Groovy
implementation 'com.github.stavro96:Rocket:1.0'
```

## Usage

Just call the rocket instance like : 

```Kotlin
private val rocket = Rocket.launch(mContext, SHARED_PREFERENCES_FILE_NAME)
```

### Saving a value : 

```Kotlin
rocket.writeString(YOUR_DESIRED_KEY_NAME , YOUR_DESIRED_VALUE)
```
### Reading a value : 

```Kotlin
rocket.readString(YOUR_DESIRED_KEY_NAME , YOUR_DESIRED_VALUE)
```

### Deleting all saved SharedPreferences : 

```Kotlin
rocket.crash()
```
### Deleting one particular value :

```Kotlin
rocket.drop(YOUR_DESIRED_KEY)
```

> Note : the current version has only the default private mode for SharedPrefs .

## Licence

```
Copyright 2019 stavro96.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
