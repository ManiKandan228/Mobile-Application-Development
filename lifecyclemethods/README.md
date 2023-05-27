# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
activity_main.xml:-
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        android:textSize="25sp"
        android:textColor="@color/purple_500"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintLeft_toLeftOf="parent"
        app:layout_constraintRight_toRightOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
MainActivty.java:-
```
package com.example.exp1;

import androidx.appcompat.app.AppCompatActivity;

import android.app.Activity;
import android.os.Bundle;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Toast toast;
        Toast.makeText(getApplicationContext(), "onCreate Called",
                Toast.LENGTH_LONG).show();
    }
    protected void onStart() {
        super.onStart();
        Toast toast;
        Toast.makeText(getApplicationContext(), "onStart Called",
                Toast.LENGTH_LONG).show();
    }
    @Override
    protected void onRestart() {
        super.onRestart();
        Toast toast;
        Toast.makeText(getApplicationContext(), "onRestart Called",
                Toast.LENGTH_LONG).show();
    }
    protected void onPause() {
        super.onPause();
        Toast toast;
        Toast.makeText(getApplicationContext(), "onPause Called",
                Toast.LENGTH_LONG).show();
    }
    protected void onResume() {
        super.onResume();
        Toast toast;
        Toast.makeText(getApplicationContext(), "onResume Called",
                Toast.LENGTH_LONG).show();
    }
    protected void onStop() {
        super.onStop();
        Toast toast;
        Toast.makeText(getApplicationContext(), "onStop Called",
                Toast.LENGTH_LONG).show();
    }
    protected void onDestroy() {
        super.onDestroy();
        Toast toast;
        Toast.makeText(getApplicationContext(), "onDestroy Called",
                Toast.LENGTH_LONG).show();
    } }
  ```
## OUTPUT

![2](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/c88aa418-bfc2-48cc-80a5-d6e4eb7b453d)


![4](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/10abf595-ca79-480b-a954-a64cf6d488d5)


![3](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/7f602d7c-9c8f-4d55-87a5-8c3352b228c0)


![1](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/3e1d25ce-3955-427b-bf47-0b3a15f46af0)

## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
