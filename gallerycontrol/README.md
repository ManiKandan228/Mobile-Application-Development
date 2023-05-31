# Ex.No:8 To create a gallery control using android studio to display images or photos.


## AIM:

To create a gallery control using android studio to display images or photos.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:



## PROGRAM:
```
/*
Program to print the text “GalleryControl”.
Developed by:Manikandan P
Registeration Number :212221040099
*/
```
## activity_main.xml:-
```
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

xmlns:app="http://schemas.android.com/apk/res-auto"

xmlns:tools="http://schemas.android.com/tools"

android:layout_width="match_parent"

android:layout_height="match_parent"

tools:context=".MainActivity">


<ImageView
    android:id="@+id/imageView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginTop="36dp"
    app:layout_constraintBottom_toTopOf="@+id/languagesGallery"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.413"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    tools:srcCompat="@tools:sample/avatars" />
<Gallery
    android:id="@+id/languagesGallery"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginTop="171dp"
    android:layout_marginBottom="204dp"
    android:animationDuration="2000"
    android:padding="10dp"
    android:spacing="5dp"
    android:unselectedAlpha="50"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/imageView" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java:-
```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.Gallery;
import android.widget.ImageView;
public class MainActivity extends AppCompatActivity {

Gallery simpleGallery;
CustomizedGalleryAdapter customGalleryAdapter;
ImageView selectedImageView;
int[] images = {R.drawable.daisy, R.drawable.jasmine,R.drawable.lily,R.drawable.lotus,R.drawable.rose};


@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    simpleGallery = (Gallery) findViewById(R.id.languagesGallery);
    selectedImageView = (ImageView) findViewById(R.id.imageView);

    customGalleryAdapter = new CustomizedGalleryAdapter(getApplicationContext(), images);

    simpleGallery.setAdapter(customGalleryAdapter);

    simpleGallery.setOnItemClickListener(new AdapterView.OnItemClickListener() {
        @Override
        public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
            selectedImageView.setImageResource(images[position]);
        }
    });
}
}
```
## CustomizedGalleryAdapter.java:-
```
package com.example.myapplication;

import android.content.Context;

import android.view.View;

import android.view.ViewGroup;

import android.widget.BaseAdapter;

import android.widget.Gallery;

import android.widget.ImageView;

public class CustomizedGalleryAdapter extends BaseAdapter {

private Context context;
private int[] images;
public CustomizedGalleryAdapter(Context c, int[] images) {
    context = c;
    this.images = images;
}
public int getCount() {
    return images.length;
}
public Object getItem(int position) {
    return position;
}
public long getItemId(int position) {
    return position;
}
public View getView(int position, View convertView, ViewGroup parent) {
    ImageView imageView = new ImageView(context);
    imageView.setImageResource(images[position]);
    imageView.setLayoutParams(new Gallery.LayoutParams(200, 200));
    return imageView;
}
}
```
## OUTPUT

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/a822574e-03e0-47d5-811c-010de64b60e5)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/08e5fda1-61af-4d64-876e-f3cf31be1c1f)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/104c19d9-1238-4dc6-b562-820ea37c2ae2)

![image](https://github.com/ManiKandan228/Mobile-Application-Development/assets/119160414/46e9d530-b724-4e02-93d0-bc1f6fc97fed)


## RESULT
Thus a Simple Android Application to create a gallery control using android studio to display images or photos is developed and executed successfully.


