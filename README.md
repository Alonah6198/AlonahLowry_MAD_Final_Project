# AlonahLowry_MAD_Final_Project
This repository is for my Mobile Application Development final project

## May 3, 2026 Update
Today, I added three dishes for each checkbox. I also added constraints to the dishes to prevent them from colliding with each other. The code is below:

### activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    tools:ignore="ExtraText">


    <TextView
        android:id="@+id/welcome_text"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/welcome_home"
        android:textColor="@color/purple"
        android:textSize="32sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.023"
        tools:ignore="VisualLintSystemUi" />

    <TextView
        android:id="@+id/allergy_question"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="32dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="32dp"
        android:text="@string/allergy_question"
        android:textAlignment="center"
        android:textColor="@color/purple"
        android:textSize="24sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/welcome_text" />

    <CheckBox
        android:id="@+id/peanut_checkbox"
        android:layout_width="150dp"
        android:layout_height="48dp"
        android:layout_marginTop="8dp"
        android:drawableTint="#FF9800"
        android:text="@string/Peanuts"
        android:textColor="#D37D0B"
        android:textColorLink="#FF9800"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.122"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/allergy_question"
        tools:ignore="TextContrastCheck" />

    <CheckBox
        android:id="@+id/tree_nuts_checkbox"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="156dp"
        android:text="@string/tree_nuts"
        android:textColor="#4CAF50"
        android:textColorLink="#4CAF50"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.101"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/peanut_checkbox"
        tools:ignore="TextContrastCheck" />

    <CheckBox
        android:id="@+id/both_checkbox"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginTop="140dp"
        android:text="@string/both"
        android:textColor="#C752DC"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.091"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/tree_nuts_checkbox"
        tools:ignore="TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText2"
        android:layout_width="239dp"
        android:layout_height="49dp"
        android:layout_marginStart="32dp"
        android:layout_marginTop="8dp"
        android:autofillHints=""
        android:drawableTint="#FF9800"
        android:ems="10"
        android:inputType="text"
        android:text="@string/jamaican_jerk_chicken"
        android:textColor="#D37D0B"
        android:textColorLink="#FF9800"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/peanut_checkbox"
        tools:ignore="LabelFor,MissingConstraints,TextSizeCheck,TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText3"
        android:layout_width="223dp"
        android:layout_height="48dp"
        android:layout_marginStart="32dp"
        android:autofillHints=""
        android:drawableTint="#FF9800"
        android:ems="10"
        android:inputType="text"
        android:text="@string/insalta_di_pasta"
        android:textColor="#D37D0B"
        android:textColorLink="#FF9800"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText2"
        tools:ignore="LabelFor,MissingConstraints,TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText4"
        android:layout_width="226dp"
        android:layout_height="49dp"
        android:layout_marginStart="32dp"
        android:autofillHints=""
        android:drawableTint="#FF9800"
        android:ems="10"
        android:inputType="text"
        android:text="@string/flan_de_la_abuela"
        android:textColor="#D37D0B"
        android:textColorLink="#FF9800"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText3"
        tools:ignore="LabelFor,MissingConstraints,TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText5"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="32dp"
        android:layout_marginTop="8dp"
        android:autofillHints=""
        android:ems="10"
        android:inputType="text"
        android:text="@string/sha_cha_beef_bao_bun"
        android:textColor="#4CAF50"
        android:textColorLink="#4CAF50"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/tree_nuts_checkbox"
        tools:ignore="LabelFor,MissingConstraints,TouchTargetSizeCheck,TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText6"
        android:layout_width="286dp"
        android:layout_height="42dp"
        android:layout_marginStart="32dp"
        android:autofillHints=""
        android:ems="10"
        android:inputType="text"
        android:text="@string/Miso"
        android:textColor="#4CAF50"
        android:textColorLink="#4CAF50"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText5"
        tools:ignore="LabelFor,MissingConstraints,TextSizeCheck,TouchTargetSizeCheck,TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText7"
        android:layout_width="263dp"
        android:layout_height="46dp"
        android:layout_marginStart="32dp"
        android:autofillHints=""
        android:ems="10"
        android:inputType="text"
        android:text="@string/hot_honey"
        android:textColor="#4CAF50"
        android:textColorLink="#4CAF50"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText6"
        tools:ignore="LabelFor,MissingConstraints,TouchTargetSizeCheck,TextContrastCheck,TextSizeCheck" />

    <EditText
        android:id="@+id/editTextText8"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="32dp"
        android:layout_marginTop="8dp"
        android:autofillHints=""
        android:ems="10"
        android:inputType="text"
        android:text="@string/tenderloin"
        android:textColor="#C752DC"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/both_checkbox"
        tools:ignore="LabelFor,MissingConstraints,TouchTargetSizeCheck,TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText9"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="32dp"
        android:layout_marginTop="8dp"
        android:autofillHints=""
        android:ems="10"
        android:inputType="text"
        android:text="@string/pretzel_bread"
        android:textColor="#C752DC"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText8"
        tools:ignore="LabelFor,MissingConstraints,TouchTargetSizeCheck,TextContrastCheck" />

    <EditText
        android:id="@+id/editTextText10"
        android:layout_width="246dp"
        android:layout_height="41dp"
        android:layout_marginStart="32dp"
        android:layout_marginTop="8dp"
        android:autofillHints=""
        android:ems="10"
        android:inputType="text"
        android:text="@string/crossant"
        android:textColor="#C752DC"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextText9"
        tools:ignore="LabelFor,MissingConstraints,TouchTargetSizeCheck,TextSizeCheck,TextContrastCheck" />

</androidx.constraintlayout.widget.ConstraintLayout>



### AndroidManifet.xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.MyApplication">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>



### string.xml
<resources>
    <string name="app_name">My Application</string>
    <string name="welcome_home">Welcome</string>
    <string name="allergy_question">Are you allergic to peanuts, tree nuts, or both?</string>
    <string name="Peanuts">Peanuts</string>
    <string name="tree_nuts">Tree Nuts</string>
    <string name="both">Both</string>
    <string name="selection_details">Selection Details</string>
    <string name="selected_format">Selected: %1$s</string>
    <string name="jamaican_jerk_chicken">Jamaican Jerk Chicken</string>
    <string name="insalta_di_pasta">Insalta di Pasta</string>
    <string name="flan_de_la_abuela">Flan de la Abuela</string>
    <string name="sha_cha_beef_bao_bun">Sha Cha Beef Bao Bun</string>
    <string name="Miso">Miso Cola-glazed Sticky Pork Ribs</string>
    <string name="hot_honey">Hot Honey Chicken Sandwich</string>
    <string name="tenderloin">Beef Tenderloin Tips</string>
    <string name="pretzel_bread">Toasted Pretzel Bread</string>
    <string name="crossant">Crossant with Goat Cheese</string>
    @string CheckBox

</resources>



### colors.xml
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="purple">#800080</color>
</resources>



### MainActivity.java
package com.example.myapplication;

import android.os.Bundle;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });

        findViewById(R.id.peanut_checkbox);
        findViewById(R.id.tree_nuts_checkbox);
        findViewById(R.id.both_checkbox);


    }
}
}

