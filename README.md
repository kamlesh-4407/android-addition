# Android Workshop – Addition of Two Numbers

## Aim

To develop an Android application that gets two values from the user and displays their **summation value** in a text box.

## Requirements

* Android Studio
* Java
* XML
* Android SDK

## Application Description

This application contains:

* Two `EditText` fields to enter two numbers.
* One `Button` to calculate the sum.
* One `EditText` to display the result.

## 1. XML Code

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number" />

    <Button
        android:id="@+id/addButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ADD" />

    <EditText
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Summation Result"
        android:enabled="false" />

</LinearLayout>
```

## 2. Java Code

```java
package com.example.add;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2, result;
    Button addButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        result = findViewById(R.id.result);
        addButton = findViewById(R.id.addButton);

        addButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                int n1 = Integer.parseInt(num1.getText().toString());
                int n2 = Integer.parseInt(num2.getText().toString());

                int sum = n1 + n2;

                result.setText(String.valueOf(sum));
            }
        });
    }
}
```


## 4. Output

<img width="1535" height="912" alt="image" src="https://github.com/user-attachments/assets/15c5bfe6-a149-4a90-b0f2-ed0cf118924c" />

<img width="1535" height="913" alt="image" src="https://github.com/user-attachments/assets/99fe440a-44cc-463f-9f45-cdcab0631c1e" />

## 5. Result

Thus, an Android application was successfully developed using **XML and Java** to get two values from the user and display their **summation value** in a text box.
