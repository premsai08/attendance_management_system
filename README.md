
https://user-images.githubusercontent.com/91896009/164498733-955df7c1-71d6-42e4-8cdc-7e6b7e30e460.mp4


- Step-0: Make sure you install [flutter] and [androidstudio]

- Step-1: Clone This Project to your local device [With this link](https://github.com/Turing311/FaceAttendance.git)
  
- Step-2: If you want to change the package name of this app run this command: 
  <br> *"flutter pub run change_app_package_name:main com.new.package.name"*

  **remember you need to generate a new AAR** 👆


- Step-3: For name changing go to android/app/src/main/AndroidManifest.xml and change the parameter in *android:label = "yourappName"*

- Step-4: Run this command to build an apk, if you have changed the package name this command will be able to generate a apk, but it won't work <br> *"flutter build apk --split-per-abi"*

- Step-5: Get a Google Map SDK key from Google API [*if you want geolocatio based verification]
   - Follow the below steps [In Order]:<br>
    ![map_doc_1](docs/android_map_sdk.png)
    ![map_doc_2](docs/tap_on_credentials.png)<br>
   - Tap on Create Credintials, after creating you will see something like this.
    ![map_doc_3](docs/map_api_key.png)<br>
   - Now add the google map api key *"android/app/src/main/AndroidManifest.xml"* in application tag
     ``` xml
     <meta-data android:name="com.google.android.geo.API_KEY"
               android:value="your_google_map_api_key _here"/>
      ```
- Step-6: Open a firebase account, create a project.
    - Create an Android App in the console with the package name of the app
    <br> *Package Name: com.example.app*
    - Download the config file googles-services.json
    - Place the file in google-services.json
    - On firestore create 3 root collection: "users", "members", "spaces".
    - Now on authentication enable **"Email/Password"** login in sign in methods
  
- Step-7: Now open a emulator or connect a device with your development machine and open the code editor of your choice and You will see a run button on the **main.dart** file if you have installed flutter extension on vscode. if not then go to your project root directory and run **_flutter run_** from the terminal. It will build the apk and install the app on the device or emulator.

- Step-8: After everything has been setted up, copy and paste the code from **firestore.rules** to the Firebase firestore security rules. This file is included with the project.

### How the data is structured: 
![data_1](docs/database_visualization/face_attendance_data_1.png)
![data_2](docs/database_visualization/face_attendance_data_2.png)
![data_3](docs/database_visualization/face_attendance_data_3.png)

### Common Errors you can get :
- Error_1: If you see red lines or a lot problems in the debug/problems tab, just run **flutter pub get** in the terminal. This happens because on initial stage your projects doesn't have reference to the cached plugin.
- Error_2: If you see init SDK (number) error (on debugging). just uninstall and reinstall the app. it will fix the issue.
- Error_3: If you see some weird plugin errors run this command in terminal it will reset the plugin cache.
> **flutter clean && flutter pub get** 


## Features
- [x] Attendance management with ease
- [x] Get attendance with face verification
- [x] Fast Face Verification
- [x] Use it as Static device to verify multiple person
- [x] Add a member without in need of another app in their phone
- [x] Multiple Space with seperate attendance on each of them
- [x] Attendance filtering
- [x] Holiday Changing
- [x] Dark Mode
- [x] Member Login
- [x] Admin Login
- [x] Admin managment
- [x] Add Member with qr code
- [x] Join Space with qr code
- [ ] Face Login in the app [Coming Soon]
- [ ] Daily log and notification [Can be added with cloud functions]
- [x] Space Range Selection [Admin Side]
- [ ] Geolocation based verification [Coming Soon]
