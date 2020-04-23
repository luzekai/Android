### 布局实验

#### 首先我们先在主活动上添加三个按钮用于管理实验的其他布局

![](./image/1.jpg)

#### 编写layout配置文件内容如下

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:orientation="vertical">

​```
<Button
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_gravity="center_horizontal"
    android:id="@+id/linearlayout"
    android:text="@string/activity_linearlayout"/>
<Button
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_gravity="center_horizontal"
    android:id="@+id/constraintlayout"
    android:text="@string/activity_constraintlayout"/>
<Button
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_gravity="center_horizontal"
    android:id="@+id/tablelayout"
    android:text="@string/activity_tablelayout"/>
​```

</LinearLayout>
```

#### 编写MainActivity.java文件实现点击跳转事件

```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.content.Intent;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {
    Button btn_linearlayout;
    Button btn_constraintlayout;
    Button btn_tablelayout;

​```
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    btn_linearlayout = (Button)findViewById(R.id.linearlayout);
    btn_linearlayout.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View view) {
            Intent intent = new Intent(MainActivity.this, LinearLayoutActivity.class);
            startActivity(intent);
        }
    });

    btn_constraintlayout = (Button) findViewById(R.id.constraintlayout);
    btn_constraintlayout.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View view) {
            Intent intent = new Intent(MainActivity.this, ConstraintlayoutActivity.class);
            startActivity(intent);
        }
    });

    btn_tablelayout = (Button) findViewById(R.id.tablelayout);
    btn_tablelayout.setOnClickListener(new View.OnClickListener() {
        @Override
        public void onClick(View view) {
            Intent intent = new Intent(MainActivity.this, TableLayoutActivity.class);
            startActivity(intent);
        }
    });
}
​```

}
```

#### 当我们点击线性布局会跳转到如下页面

![](./image/2.jpg)

#### 编写layout配置文件内容如下

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="wrap_content">
    <LinearLayout android:layout_height="wrap_content"
        android:layout_width="match_parent">
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="One,One"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="One,Two"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="One,Three"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="One,Four"
            android:gravity="center"
            android:layout_margin="5dp"/>
    </LinearLayout>
    <LinearLayout android:layout_height="wrap_content"
        android:layout_width="match_parent">
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Two,One"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Two,Two"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Two,Three"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Two,Four"
            android:gravity="center"
            android:layout_margin="5dp"/>
    </LinearLayout>
    <LinearLayout android:layout_height="wrap_content"
        android:layout_width="match_parent">
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Three,One"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Three,Two"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Three,Three"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Three,Four"
            android:gravity="center"
            android:layout_margin="5dp"/>
    </LinearLayout>
    <LinearLayout android:layout_height="wrap_content"
        android:layout_width="match_parent">
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Four,One"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Four,Two"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Four,Three"
            android:gravity="center"
            android:layout_margin="5dp"/>
        <TextView
            android:layout_height="wrap_content"
            android:layout_width="wrap_content"
            android:layout_weight="1"
            android:text="Four,Four"
            android:gravity="center"
            android:layout_margin="5dp"/>
    </LinearLayout>
</LinearLayout>
```

#### 接下来在相应的Activity.java文件中编写类似如下内容实现返回功能

```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

public class LinearLayoutActivity extends AppCompatActivity {

​```
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_linearlayout);
    getSupportActionBar().setDisplayHomeAsUpEnabled(true);
}
​```

}
```

#### 当我们点击左上角的返回键将返回到主活动页面上，再次点击约束布局将出现如下页面

![](./image/3.jpg)

#### 编写layout配置文件内容如下

```
<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:stretchColumns="1">

​```
<TableRow>
    <TextView
        android:layout_column="1"
        android:text="Open..."
        android:padding="3dp" />
    <TextView
        android:text="Ctrl-O"
        android:gravity="right"
        android:padding="3dp" />
</TableRow>

<TableRow>
    <TextView
        android:layout_column="1"
        android:text="Save..."
        android:padding="3dp" />
    <TextView
        android:text="Ctrl-S"
        android:gravity="right"
        android:padding="3dp" />
</TableRow>

<TableRow>
    <TextView
        android:layout_column="1"
        android:text="Save As..."
        android:padding="3dp" />
    <TextView
        android:text="Ctrl-Shift-S"
        android:gravity="right"
        android:padding="3dp" />
</TableRow>

<View
    android:layout_height="2dp"
    android:background="#FF909090" />

<TableRow>
    <TextView
        android:text="X"
        android:padding="3dp" />
    <TextView
        android:text="Import..."
        android:padding="3dp" />
</TableRow>

<TableRow>
    <TextView
        android:text="X"
        android:padding="3dp" />
    <TextView
        android:text="Export..."
        android:padding="3dp" />
    <TextView
        android:text="Ctrl-E"
        android:gravity="right"
        android:padding="3dp" />
</TableRow>

<View
    android:layout_height="2dp"
    android:background="#FF909090" />

<TableRow>
    <TextView
        android:layout_column="1"
        android:text="Quit"
        android:padding="3dp" />
</TableRow>
​```

</TableLayout>
```

#### 最后点击左上角的返回键返回到主活动页面上，再次点击表格布局将出现如下页面

![](./image/4.jpg)

#### 编写layout配置文件内容如下

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".ConstraintlayoutActivity">

​```
<TextView
    android:id="@+id/TextView1"
    android:text="@string/TextView1"
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:background="#f00"
    android:gravity="center"
    android:textColor="#000"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintVertical_bias="0"
    app:layout_constraintHorizontal_bias="0"
    android:padding="25dp"></TextView>

<TextView
    android:id="@+id/TextView2"
    android:text="@string/TextView2"
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:background="#ffa500"
    android:gravity="center"
    android:textColor="#000"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintVertical_bias="0"
    app:layout_constraintHorizontal_bias="0.5"
    android:padding="25dp"></TextView>

<TextView
    android:id="@+id/TextView3"
    android:text="@string/TextView3"
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:background="#ffff00"
    android:gravity="center"
    android:textColor="#000"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintVertical_bias="0"
    app:layout_constraintHorizontal_bias="1"
    android:padding="25dp"></TextView>

<TextView
    android:id="@+id/TextView4"
    android:text="@string/TextView4"
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:background="#0f0"
    android:gravity="center"
    android:textColor="#000"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintVertical_bias="0.15"
    app:layout_constraintHorizontal_bias="0.15"
    android:padding="25dp"></TextView>

<TextView
    android:id="@+id/TextView5"
    android:text="@string/TextView5"
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:background="#00f"
    android:gravity="center"
    android:textColor="#fff"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintVertical_bias="0.15"
    app:layout_constraintHorizontal_bias="0.5"
    android:padding="25dp"></TextView>

<TextView
    android:id="@+id/TextView6"
    android:text="@string/TextView6"
    android:layout_height="wrap_content"
    android:layout_width="wrap_content"
    android:background="#4b0082"
    android:gravity="center"
    android:textColor="#fff"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintVertical_bias="0.15"
    app:layout_constraintHorizontal_bias="0.85"
    android:padding="25dp"></TextView>

<TextView
    android:id="@+id/TextView7"
    android:text="@string/TextView7"
    android:layout_height="wrap_content"
    android:layout_width="0dp"
    android:background="#ee82ee"
    android:gravity="center"
    android:textColor="#000"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintVertical_bias="0.3"
    android:padding="25dp"></TextView>
​```

</androidx.constraintlayout.widget.ConstraintLayout>
```

#### 编写AndroidManifest.xml文件，编写内容如下

```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.myapplication">

​```
<application
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">
    <activity android:name=".MainActivity">
        <intent-filter>
            <action android:name="android.intent.action.MAIN" />

            <category android:name="android.intent.category.LAUNCHER" />
        </intent-filter>
    </activity>
    <activity android:name=".LinearLayoutActivity"
        android:label="@string/activity_linearlayout"
        android:parentActivityName=".MainActivity" />
    <activity android:name=".ConstraintlayoutActivity"
        android:label="@string/activity_constraintlayout"
        android:parentActivityName=".MainActivity"/>
    <activity android:name=".TableLayoutActivity"
        android:label="@string/activity_tablelayout"
        android:parentActivityName=".MainActivity"></activity>
</application>
​```

</manifest>
```

