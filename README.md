# rndatecs-printer

It only **works on Android** and have only few specific methods.

As I made this project with a very short deadline, it's specific for the app that I was working on.
My plan is to make a full port of cordova-plugin-datecs-printer for React Native.

### Printer used for tests
DPP 250

---

## Getting started (latest version)

`$ npm install rndatecs-printer --save`

### Mostly automatic installation

`$ npx react-native link rndatecs-printer`

### Add permissions in your AndroidManifest.xml
```
<uses-permission android:name="android.permission.BLUETOOTH"/>
<uses-permission android:name="android.permission.BLUETOOTH_ADMIN"/>
```

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.rn.datecsprinter.RNDatecsPrinterPackage;` to the imports at the top of the file

2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':rndatecs-printer'
  	project(':rndatecs-printer').projectDir = new File(rootProject.projectDir, '../node_modules/rndatecs-printer/android')

  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
	  dependencies {
		compile project(':rndatecs-printer')  
	  }
      
  	```

### Tags definition
- `{reset}`	    Reset to default settings.
- `{br}`	    Line break. Equivalent of new line.
- `{b}, {/b}`	Set or clear bold font style.
- `{u}, {/u}`	Set or clear underline font style.
- `{i}, {/i}`	Set or clear italic font style.
- `{s}, {/s}`	Set or clear small font style.
- `{h}, {/h}`	Set or clear high font style.
- `{w}, {/w}`	Set or clear wide font style.
- `{left}`	    Aligns text to the left paper edge.
- `{center}`	Aligns text to the center of paper.
- `{right}`	    Aligns text to the right paper edge.
