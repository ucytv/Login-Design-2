### Login-Design-2

This project consists of design only. The design which follows the trends of 2020 includes a screen that you can enter your application. The demo and source codes are shown following. Click on the link for a similar design: [Login-Design-1](https://github.com/ucytv/Login-Design-1)

### Demo

![login_design_2](https://user-images.githubusercontent.com/37077627/82705455-58560200-9c80-11ea-8b8f-7c761f28e9ec.png)

#Dependencies

```
implementation 'com.google.android.material:material:1.1.0'
```

### Style & Theme

```
<style name="LoginTheme" parent="Theme.MaterialComponents.Light.NoActionBar.Bridge">
        <item name="colorPrimary">@color/colorText</item>
        <item name="colorPrimaryDark">@color/colorDark</item>
        <item name="colorAccent">@color/colorLight</item>
        <item name="colorOnSurface">@color/colorText</item>
</style>
```

### Color

```
<color name="colorMain">#FFFFFF</color>
<color name="colorDark">#11C31E</color>
<color name="colorLight">#F1E4E4</color>
<color name="colorText">#198C22</color>
<color name="colorInactive">#C80E0E</color>
<color name="white">#FFFFFF</color>
<color name="black">#000000</color>
```

### Font

```
<font-family xmlns:app="http://schemas.android.com/apk/res-auto"
        app:fontProviderAuthority="com.google.android.gms.fonts"
        app:fontProviderPackage="com.google.android.gms"
        app:fontProviderQuery="Audiowide"
        app:fontProviderCerts="@array/com_google_android_gms_fonts_certs">
</font-family>
```

### Layout Style

```
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="rectangle">
            <corners android:radius="8dp"/>
            <stroke android:color="@color/colorText"
                android:width="2dp"/>
        </shape>
    </item>
</selector>
```

### Button Style
```
<selector xmlns:android="http://schemas.android.com/apk/res/android">
    <item>
        <shape android:shape="rectangle">
            <corners android:radius="8dp"/>
            <gradient android:startColor="@color/colorText"
                android:endColor="@color/colorLight"/>
        </shape>
    </item>
</selector>
```

### String
```
<string name="app_name">LoginDesign2</string>
<string name="account_text">Don\'t you have an account yet?</string>
<string name="sign_up">SIGN UP</string>
<string name="nickname">Nickname</string>
<string name="remember">Remember Me</string>
<string name="forgot">I forgot my password</string>
<string name="login">LOGIN</string>
<string name="password">Password</string>
```

### Java Class
```
@Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        //Must be fullscreen!
        getWindow().setFlags(WindowManager.LayoutParams.FLAG_FULLSCREEN,
                WindowManager.LayoutParams.FLAG_FULLSCREEN);
        setContentView(R.layout.activity_main);

        getSupportActionBar().hide();//This is important
    }
```

### XML File
```
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@color/colorMain"
    android:orientation="vertical"
    android:padding="30dp"
    android:theme="@style/LoginTheme"
    tools:context=".MainActivity"
    >

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:gravity="center"
        android:orientation="horizontal"
        android:layout_marginTop="60dp"
        >

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            android:fontFamily="@font/audiowide"
            android:text="@string/account_text"
            android:textColor="@color/colorText"
            android:textSize="15sp"
            android:textStyle="italic" 
            />

        <TextView
            android:id="@+id/button_signup"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="center"
            android:layout_marginStart="8dp"
            android:fontFamily="@font/audiowide"
            android:text="@string/sign_up"
            android:textAllCaps="true"
            android:textColor="@color/colorText"
            android:textSize="14sp"
            android:textStyle="bold"
            />
    </LinearLayout>

    <ImageView
        android:layout_width="100dp"
        android:layout_height="100dp"
        android:src="@drawable/yaman_new"
        android:layout_gravity="center"
        android:layout_marginTop="40dp"
        />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="40dp"
        android:background="@drawable/layout_style_green"
        >

        <com.google.android.material.textfield.TextInputLayout
            android:id="@+id/text_input_nick"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox.Dense"
            android:hint="@string/nickname"
            app:endIconTint="@color/colorText"
            app:endIconMode="clear_text"
            app:passwordToggleTint="@color/colorDark"
            >

            <com.google.android.material.textfield.TextInputEditText
                android:id="@+id/edit_input_nick"
                android:fontFamily="@font/audiowide"
                android:textSize="12sp"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:inputType="textEmailAddress"
                android:padding="16dp"
                android:textColor="@color/colorText" 
                />
        </com.google.android.material.textfield.TextInputLayout>

        <com.google.android.material.textfield.TextInputLayout
            android:id="@+id/text_input_pass"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            style="@style/Widget.MaterialComponents.TextInputLayout.OutlinedBox.Dense"
            android:hint="@string/password"
            android:layout_marginTop="12dp"
            app:endIconMode="password_toggle"
            app:endIconTint="@color/colorText"
            >

            <com.google.android.material.textfield.TextInputEditText
                android:id="@+id/edit_input_pass"
                android:layout_width="match_parent"
                android:layout_height="wrap_content"
                android:textColor="@color/colorText"
                android:inputType="numberPassword"
                android:fontFamily="@font/audiowide"
                android:textSize="12sp"
                android:padding="16dp"
                app:boxStrokeColor="@color/colorMain"
                />
        </com.google.android.material.textfield.TextInputLayout>

        <RelativeLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            >

            <LinearLayout
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:orientation="horizontal"
                android:layout_marginEnd="2dp"
                android:layout_marginTop="8dp"
                android:layout_alignParentEnd="true"
                >

                <TextView
                    android:id="@+id/button_remember"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    android:text="@string/remember"
                    android:fontFamily="@font/audiowide"
                    android:gravity="center"
                    android:textSize="12sp"
                    android:textColor="@color/colorText"
                    android:layout_marginEnd="4dp"
                    android:layout_gravity="center"
                    />

                <androidx.appcompat.widget.SwitchCompat
                    android:id="@+id/switch_remember"
                    android:layout_width="wrap_content"
                    android:layout_height="wrap_content"
                    app:trackTint="@drawable/switch_style" 
                    />

            </LinearLayout>

        </RelativeLayout>

        <Button
            android:id="@+id/button_login"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="12dp"
            android:background="@drawable/button_style"
            android:text="@string/login"
            android:fontFamily="@font/audiowide"
            android:textSize="12sp"
            android:textStyle="bold"
            android:textAllCaps="true"
            android:textColor="@color/black" 
            />

        <TextView
            android:id="@+id/button_request"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textAllCaps="false"
            android:text="@string/forgot"
            android:textColor="@color/colorText"
            android:gravity="center"
            android:layout_gravity="center"
            android:layout_marginTop="12dp"
            android:textSize="12sp"
            android:fontFamily="@font/audiowide"
            />

    </LinearLayout>
</LinearLayout>
```
