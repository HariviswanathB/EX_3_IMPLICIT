## EXPERIMENT:03  Implement an application that uses Intent(Implicit) using Android Studio.
Design an Android application with a text field and an "Open in Browser" button. On pressing the button, the app should fetch the URL from the text field and open it in a browser using an Implicit Intent.

## AIM:

To design an Android application with a TextField and a button labeled "Open in Browser." Upon pressing the button, the application should retrieve the URL entered in the TextField and open it in the device's web browser using an implicit intent.
## EQUIPMENTS REQUIRED:
za
Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as implicitintent and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Type any url, click navigate and that will take you to the expected url.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: HARIVISWANATH B
Registeration Number :  212222040051
*/
```

## MainActivity.java:

```
package com.example.Exp_3;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {
    Button button;

    EditText editText;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final EditText editText = (EditText) findViewById(R.id.urlText);
        Button btn = (Button) findViewById(R.id.btnNavigate);
        btn.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                String url = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
```

## activitymain.xml:

```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/urlText"
        android:layout_alignParentTop="true"
        android:layout_centerHorizontal="true"
        android:layout_marginTop="100dp"
        android:ems="10" />
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/btnNavigate"
        android:layout_below="@+id/urlText"
        android:text="Navigate"
        android:layout_centerHorizontal="true" />
</RelativeLayout>
```

## OUTPUT

<img width="315" alt="Screenshot 2025-06-01 at 7 57 12 PM" src="https://github.com/user-attachments/assets/a4ccb715-0216-45bf-9cb4-19b3141218b1" />
<img width="307" alt="Screenshot 2025-06-01 at 7 57 22 PM" src="https://github.com/user-attachments/assets/f457083d-a71a-4a6f-81d2-5da487b273b6" />
<img width="304" alt="Screenshot 2025-06-01 at 7 57 37 PM" src="https://github.com/user-attachments/assets/47f8c1b8-e4f6-426d-a891-ce29462e7e66" />



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the web page using Android Studio was developed and executed successfully.
