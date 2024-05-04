# Simple-UnitConvertor-App in Java
Unitconvertor app is the simply convert the kilogram value to pound.

-----code--------Android Studio----

package com.example.unitconvertor;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

//  Declaring widgets
    TextView textView2,textView5,textView4;
    EditText editTextNumber;
    Button button1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
//      EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);

//      Instantiating widgets

        textView2 = findViewById(R.id.textView2);
        textView5 = findViewById(R.id.textView5);
        textView4 = findViewById(R.id.textView4);
        editTextNumber = findViewById(R.id.editTextNumber);
        button1 = findViewById(R.id.button1);

//      Adding a click event on button  when clicked button..
        button1.setOnClickListener(new View.OnClickListener(){
            @Override
            public void onClick(View v) {
                textView4();

            }

        });
    }
    private void textView4() {

//  This method will convert the entered kg value to pounds
     String valueEnteredInKILO = editTextNumber.getText().toString();

//     converting string to number
       double KILO = Double.parseDouble(valueEnteredInKILO);

//       Converting to kilo
        double pounds = KILO * 2.2046;
        textView4.setText(" "+pounds + "pound");

    }
}
