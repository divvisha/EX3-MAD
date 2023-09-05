# Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.<br>
Step 2: Then type the Application name as HelloWorld and click Next. <br>
Step 3: Then select the Minimum SDK as shown below and click Next.<br>
Step 4: Then select the Empty Activity and click Next. Finally click Finish.<br>
Step 5: Design layout in activity_main.xml<br>
Step 6: Display message give in MainActivity file. <br>
Step 7: Save and run the application


## PROGRAM:
~~~
Program to print the text “Implicitintent”.
Developed by: DIVYASHREE B S
Registeration Number : 212221040044
~~~

## activity_main.xml
~~~
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity">
 <Button
 android:id="@+id/button"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginEnd="48dp"
 android:text="NAVIGATE"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.219" />
 <EditText
 android:id="@+id/editTextTextPersonName"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginStart="32dp"
 android:ems="10"
 android:inputType="textPersonName"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.218" />
</androidx.constraintlayout.widget.ConstraintLayout>
~~~

## MainActivity.java
~~~
package com.example.ex3;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.widget.Button;
import android.widget.EditText;
import android.os.Bundle;
public class MainActivity extends AppCompatActivity {
 Button button;
 EditText editText;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 button = findViewById(R.id.button);
 editText = findViewById(R.id.editTextTextPersonName);
 button.setOnClickListener(view -> {
 String url=editText.getText().toString();
 Intent intent=new Intent(Intent.ACTION_VIEW, Uri.parse(url));
 startActivity(intent);
 });
 } }
 ~~~

## OUTPUT

![image](https://github.com/divvisha/EX3-MAD/assets/127508123/c5c334d8-dcee-4642-a3e3-a5bc6f0ed2e1)

![image](https://github.com/divvisha/EX3-MAD/assets/127508123/8831b467-1994-493c-89cb-8392bd4f2214)


## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
