App Requirements: What Device Features Does our App Need?android

Your typical AR application requires access to the following device features:

Access to the camera view
Access to the user’s location
Access to other device sensors, especially a compass (accelerometer and gyroscope can also be useful)
The application may also require other services and permissions, such as network access, but these
are not central to the AR aspects of the application.


Step 2: Configure the Manifest File

 
Next, you’ll want to configure the Android Manifest File. You’ll want to specify the following settings:

On the Manifest Tab, add settings for the following:

android.hardware.camera (Required=true)
android.hardware.camera.autofocus (Required=false)
android.hardware.location.gps (Required=true)
android.hardware.sensor.compass (Required=true)
android.hardware.sensor.gyroscope (Required=true)
android.hardware.sensor.accelerometer (Required=true)
On the Application Tab:

Debuggable should be set to true
On the Permissions Tab, add settings for:

android.permission.CAMERA
android.permission.FINE_LOCATION


Step 1: Defining the App Screen Layout

 
First, we need to define the layout resource that will be used for the main AR screen. A FrameLayout
is most appropriate for our screen, as it allows the layering of views within the display area.
Therefore, our layout resource, /res/layout/main.xml, can be quite simple:


<?xml version="1.0" encoding="utf-8"?>
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/ar_view_pane"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent">
</FrameLayout>
