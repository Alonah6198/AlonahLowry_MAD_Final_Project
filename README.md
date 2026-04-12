# AlonahLowry_MAD_Final_Project
This repository is for my Mobile Application Development final project

## April 12, 2026 Update
Currently, I edited the home page to the color purple. I also was able to add three check boxes. The code is below:

### activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

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
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.072" />

    <TextView
        android:id="@+id/allergy_question"
        android:layout_width="0dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="32dp"
        android:layout_marginTop="24dp"
        android:layout_marginEnd="32dp"
        android:text="@string/allergy_question"
        android:textAlignment="center"
        android:textColor="@color/purple"
        android:textSize="24sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@id/welcome_text" />

    <CheckBox
        android:id="@+id/checkBox"
        android:layout_width="115dp"
        android:layout_height="49dp"
        android:layout_marginBottom="450dp"
        android:text="@string/Peanuts"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/allergy_question"
        app:layout_constraintVertical_bias="0.761"
        tools:ignore="VisualLintOverlap" />

    <CheckBox
        android:id="@+id/checkBox3"
        android:layout_width="123dp"
        android:layout_height="51dp"
        android:text="@string/tree_nuts"
        tools:ignore="MissingConstraints"
        tools:layout_editor_absoluteX="144dp"
        tools:layout_editor_absoluteY="290dp" />

    <CheckBox
        android:id="@+id/checkBox4"
        android:layout_width="116dp"
        android:layout_height="50dp"
        android:text="@string/both"
        tools:ignore="MissingConstraints"
        tools:layout_editor_absoluteX="147dp"
        tools:layout_editor_absoluteY="355dp" />

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
    }
}

