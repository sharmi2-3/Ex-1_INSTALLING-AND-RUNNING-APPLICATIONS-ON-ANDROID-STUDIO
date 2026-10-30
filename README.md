# EX-1: INSTALLING AND RUNNING APPLICATIONS ON ANDROID STUDIO

**Name:** SHARMILA P

**Register Number:** 212224220094

## Software Requirements
- Android Studio
- Android SDK
- Android Virtual Device (AVD)
- Java
- XML

---

## Step 1 – System Requirements

The required software tools are used to develop, design, and run Android applications. Android Studio provides the development environment, Java is used to implement application functionality, and XML is used to design the user interface.

**Required Software**

Android Studio

Java Development Kit (JDK)

Android SDK

Android Emulator

---

## Step 2 – Setup Android Studio

Android Studio is the official Integrated Development Environment (IDE) used for Android application development.

### Installation Procedure
1. Download Android Studio from the official website.
2. Run the installer and follow the installation instructions.
3. Install the required Android SDK components.
4. Configure the Android SDK location.
5. Set up the Android Virtual Device if required.
6. Launch Android Studio.
7. Create a new Android project using the Empty Views Activity template.
8. Select Java as the programming language.

---

## Creating the Campus Connect Application

1.Open the project in Android Studio.

2.Design the user interface using the activity_main.xml file.

3.Add a heading named CAMPUS CONNECT.

4.Add a subtitle named College Event Registration.

5.Add an EditText field to enter the student's name.

6.Add a Spinner to select the college event.

7.Add an EditText field to enter the email address.

8.Add a Button named Register Now.

9.Add a TextView to display the registration details.

10.Open the MainActivity.java file.

11.Initialize the EditText, Spinner, Button, and TextView using findViewById().

12.Implement the button click event using setOnClickListener().

13.Retrieve the student's name, email address, and selected event.

14.Validate the input fields to ensure that they are not empty.

15.Display the registration details when the button is clicked.

16.Change the button text to Registered after successful registration.

---

## Step 3 – Create Android Virtual Device (AVD)

An Android Virtual Device is used to test and run the application without requiring a physical Android phone.

### Procedure
1. Open Device Manager in Android Studio.
2. Click **Create Virtual Device**.
3. Select a suitable device configuration.
4. Select and download an Android system image if required.
5. Finish the configuration and start the emulator.
6. Select the emulator from the device dropdown menu.

---
## Step 4 – Run the Application

1.Open the Campus Connect project in Android Studio.

2.Select the configured Android Emulator.

3.Click the Run ▶ button in Android Studio.

4.Wait for the application to build and launch.

5.Verify that the Campus Connect registration screen appears.

6.Enter the student's name and email address.

7.Select an event from the available event list.

8.Click the Register Now button.

9.Verify that the registration details are displayed successfully.

10.Check that the button text changes to Registered.

---

## CODE 

**activity_main.xml**:
```

<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="25dp"
    android:background="#FFF7FF">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Student Details"
        android:textSize="24sp"
        android:textStyle="bold"
        android:textColor="#333333"
        android:layout_marginBottom="25dp"/>

    <EditText
        android:id="@+id/studentName"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Student Name"
        android:inputType="textPersonName"/>

    <EditText
        android:id="@+id/registerNumber"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Register Number"
        android:inputType="number"/>

    <EditText
        android:id="@+id/department"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Department"
        android:inputType="textCapWords"/>

    <EditText
        android:id="@+id/email"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Email ID"
        android:inputType="textEmailAddress"/>

    <Button
        android:id="@+id/saveButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Save Student"
        android:layout_marginTop="20dp"
        android:backgroundTint="#7050B5"
        android:textColor="#FFFFFF"/>

    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:textSize="16sp"
        android:textColor="#333333"
        android:layout_marginTop="20dp"/>

</LinearLayout>

```

**MainActivity.java.**

```

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import android.widget.Toast;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText studentName, registerNumber, department, email;
    Button saveButton;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        studentName = findViewById(R.id.studentName);
        registerNumber = findViewById(R.id.registerNumber);
        department = findViewById(R.id.department);
        email = findViewById(R.id.email);
        saveButton = findViewById(R.id.saveButton);
        result = findViewById(R.id.result);

        saveButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {

                String name = studentName.getText().toString().trim();
                String regNo = registerNumber.getText().toString().trim();
                String dept = department.getText().toString().trim();
                String mail = email.getText().toString().trim();

                if (name.isEmpty() || regNo.isEmpty()
                        || dept.isEmpty() || mail.isEmpty()) {

                    Toast.makeText(MainActivity.this,
                            "Please fill all fields",
                            Toast.LENGTH_SHORT).show();

                } else {

                    saveButton.setText("Details Revealed");

                    result.setText(
                            "Student Name: " + name +
                            "\nRegister Number: " + regNo +
                            "\nDepartment: " + dept +
                            "\nEmail: " + mail
                    );
                }
            }
        });
    }
}

```

## Output

The application displays the heading **STUDENT DETAILS** and a button. When the button is clicked, the following details appear:

- **Name:** SHARMILA P
- **Register Number:** 212224220094

<img width="639" height="375" alt="Screenshot 2026-10-29 205314" src="https://github.com/user-attachments/assets/32bce0c9-f1bb-44c4-b402-f21b361a719e" />





## Result

Thus, the Campus Connect – College Event Registration Android application was successfully developed, installed, and executed using Android Studio. The application allows users to enter their details, select a college event, and view their registration information.
