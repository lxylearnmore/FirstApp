### 实验一：验证Activity的生命周期

### 生命周期的截图：

![](https://i.loli.net/2019/03/19/5c905c5d08957.png)

### 相关代码：

``

```
public class MainActivity extends AppCompatActivity {
    private static final String Tag="Android_live_cycle";
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Log.d(Tag,"onCreate");
    }

    @Override
    protected void onStart() {
        super.onStart();
        Log.d(Tag,"onStart");
    }

    @Override
    protected void onResume(){
        super.onResume();
        Log.d(Tag,"onResume");
    }

    @Override
    protected void onPause(){
        super.onPause();
        Log.d(Tag,"onPause");
    }

    @Override
    protected void onStop() {
        super.onStop();
        Log.d(Tag,"onStop");
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        Log.d(Tag,"onDestroy");
    }


}
```

# 实验二：Android布局

## 1）线性布局

### 截图：

![](https://i.loli.net/2019/03/19/5c905c87bb3e5.png)

### 相关代码：

``

```
<?xml version="1.0" encoding="utf-16" ?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical" >
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal" >
        <Button
            android:id="@+id/btn_o1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,One" />
        <Button
            android:id="@+id/btn_o2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="One,Two"/>
        <Button
            android:id="@+id/btn_o3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,Three"/>
        <Button
            android:id="@+id/btn_o4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="One,Four"/>
    </LinearLayout>
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal" >
        <Button
            android:id="@+id/btn_t1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,One"/>
        <Button
            android:id="@+id/btn_t2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,Two"/>
        <Button
            android:id="@+id/btn_t3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,Three"/>
        <Button
            android:id="@+id/btn_t4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,Four"/>
    </LinearLayout>
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal" >
        <Button
            android:id="@+id/btn_th1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Three,One"/>
        <Button
            android:id="@+id/btn_th2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Three,Two"/>
        <Button
            android:id="@+id/btn_th3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Two,Three"/>
        <Button
            android:id="@+id/btn_th4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Three,Four"/>
    </LinearLayout>

    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <Button
            android:id="@+id/btn_f1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Four,One" />

        <Button
            android:id="@+id/btn_f2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Four,Two" />

        <Button
            android:id="@+id/btn_f3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Four,Three" />

        <Button
            android:id="@+id/btn_f4"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="Four,Four" />
    </LinearLayout>


</LinearLayout>
```

## 2）Constraint布局

### 截图：

![](https://i.loli.net/2019/03/19/5c905c97bb8b3.png)

### 相关代码：

``

```
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <Button
        android:id="@+id/button"
        android:layout_width="69dp"
        android:layout_height="46dp"
        android:layout_marginStart="96dp"
        android:layout_marginLeft="96dp"
        android:background="@color/colorAccent"
        android:text="GREEN"
        app:layout_constraintBottom_toBottomOf="@+id/button6"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/button6" />

    <Button
        android:id="@+id/button7"
        android:layout_width="69dp"
        android:layout_height="46dp"
        android:layout_marginEnd="92dp"
        android:layout_marginRight="92dp"
        android:background="@color/colorPrimary"
        android:text="Indigo"
        app:layout_constraintBottom_toBottomOf="@+id/button6"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="@+id/button6" />

    <Button
        android:id="@+id/button2"
        android:layout_width="88dp"
        android:layout_height="46dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:background="@android:color/holo_red_dark"
        android:text="Red"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button3"
        android:layout_width="88dp"
        android:layout_height="46dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_orange_dark"
        android:text="Orange"
        app:layout_constraintEnd_toStartOf="@+id/button4"
        app:layout_constraintStart_toEndOf="@+id/button2"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button4"
        android:layout_width="88dp"
        android:layout_height="46dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_orange_light"
        android:text="Yellow"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button6"
        android:layout_width="69dp"
        android:layout_height="46dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="50dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_blue_light"
        android:text="Blue"
        app:layout_constraintEnd_toStartOf="@+id/button7"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toEndOf="@+id/button"
        app:layout_constraintTop_toBottomOf="@+id/button3" />

    <Button
        android:id="@+id/button8"
        android:layout_width="377dp"
        android:layout_height="46dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="30dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:background="@android:color/holo_purple"
        android:text="Violet"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button6" />

</android.support.constraint.ConstraintLayout>
```

## 3）表格布局

### 截图：

![](https://i.loli.net/2019/03/19/5c905ca5ec60c.png)

### 相关代码：

``

```
<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"

    >
    <TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:paddingLeft="16dp"
        android:paddingRight="16dp"
        >

        <TableRow>
            <TextView
                android:id="@+id/txt_title_r1"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentLeft="true"
                android:layout_weight="1"
                android:text="Open..." />

            <TextView
                android:id="@+id/txt_title_l1"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="right"
                android:text="Ctrl-O" />

        </TableRow>

        <TableRow>

            <TextView
                android:id="@+id/txt_title_r2"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentLeft="true"
                android:layout_weight="1"
                android:text="Save..." />

            <TextView
                android:id="@+id/txt_title_l2"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="right"
                android:text="Ctrl-S" />

        </TableRow>

        <TableRow>
            <TextView
                android:id="@+id/txt_title_r3"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentLeft="true"
                android:layout_weight="1"
                android:text="Save As..." />

            <TextView
                android:id="@+id/txt_title_l3"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="right"
                android:text="Ctrl-Shift-S" />

        </TableRow>
    </TableLayout>

    <View
        android:id="@+id/separator1"
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#90909090" />


    <TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:paddingRight="16dp"
        >
        <TableRow>

            <TextView
                android:id="@+id/txt_title_r4"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentLeft="true"
                android:layout_weight="1"
                android:text=" X Import..." />

        </TableRow>
        <TableRow>

            <TextView
                android:id="@+id/txt_title_r5"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentLeft="true"
                android:layout_weight="1"
                android:text=" X Export..." />

            <TextView
                android:id="@+id/txt_title_l5"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_gravity="right"
                android:text="Ctrl-E" />

        </TableRow>
    </TableLayout>

    <View
        android:id="@+id/separator2"
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#90909090" />

    <TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:paddingLeft="16dp"
        android:paddingRight="16dp"
        >
        <TableRow>

            <TextView
                android:id="@+id/txt_title_r6"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentLeft="true"
                android:layout_weight="1"
                android:text="Quit" />

        </TableRow>
    </TableLayout>

</TableLayout>
```


