1. Buka Android Studio
2. Beri Nama Project dan Package Name
3. Pilih Minimum SDK Version
4. Lalu kita ke folder res -> values -> themes -> themes.xml
    Ubah parent .

    <style name="Base.Theme.Calculator" parent="Theme.AppCompat.NoActionBar">

5. Kemudian kita ke Gradle Scripts -> build.gradle(Module:app)
    kita tambahkan di dependencies.

    implementation("net.objecthunter:exp4j:0.4.8")
    implementation("org.jetbrains.kotlin:kotlin-stdlib:1.8.0")

6. Lalu kita kembali ke folder res -> values -> colors.xml
    Kita tambahkan setelah warna putih / white.

    <color name="navi">#1199AA</color>
    <color name="red">#E53935</color>
    <color name="yellow">#FFB300</color>

7. Lalu di folder res -> drawable, kita klik kanan kemudian pilih New Drawable Resource File
    Kita bikin File Name : rounded_button, kemudian klik ok.
    kemudian buka file rounded_button.xml yang sebelumnya dibuat,
    kemudian klik ctrl+A lalu ctrl+V kode dibawah ini :

    <?xml version="1.0" encoding="utf-8"?>
        <shape xmlns:android="http://schemas.android.com/apk/res/android"
            android:shape="oval">
            <solid android:color="#A8A8A8" />
            <size
                android:width="80dp"
                android:height="80dp" />
        </shape>

8. Lalu Desain User Interface di activity_main.xml, mengikuti kode dibawah ini

    <?xml version="1.0" encoding="utf-8"?>
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@color/white"
        android:orientation="vertical">


        <EditText
            android:id="@+id/editText"
            android:textSize="30sp"
            android:textAlignment="textEnd"
            android:layout_marginRight="20sp"
            android:textColor="@color/black"
            android:layout_marginBottom="20dp"
            android:layout_width="match_parent"
            android:text="0"
            android:layout_height="100dp"
            android:hint="0" />

        <LinearLayout
            android:orientation="vertical"
            android:gravity="bottom"
            android:layout_width="match_parent"
            android:layout_height="match_parent">

            <EditText
                android:id="@+id/resultTextView"
                android:textSize="70sp"
                android:textAlignment="textEnd"
                android:layout_marginRight="20sp"
                android:textColor="@color/black"
                android:layout_marginBottom="20dp"
                android:layout_width="match_parent"
                android:text="0"
                android:layout_height="wrap_content"
                android:hint="0" />

            <LinearLayout
                android:paddingTop="20sp"
                android:background="#F4F4F4"
                android:orientation="vertical"
                android:layout_width="match_parent"
                android:layout_height="wrap_content">

                <LinearLayout
                    android:layout_width="match_parent"
                    android:padding="10dp"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <Button
                        android:id="@+id/backspace"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="C"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/buttonBr1"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="("
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/buttonBr2"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text=")"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/buttonDivide"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="/"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"/>
                </LinearLayout>

                <LinearLayout
                    android:layout_width="match_parent"
                    android:padding="10dp"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <Button
                        android:id="@+id/button1"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="1"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/button2"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="2"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/button3"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="3"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/buttonAdd"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="+"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"/>
                </LinearLayout>

                <LinearLayout
                    android:layout_width="match_parent"
                    android:padding="10dp"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">

                    <Button
                        android:id="@+id/button4"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="4"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/button5"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="5"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/button6"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="6"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/buttonSubtract"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="-"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"/>
                </LinearLayout>

                <LinearLayout
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:padding="10dp"
                    android:orientation="horizontal">

                    <Button
                        android:id="@+id/button7"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="7"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/button8"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="8"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/button9"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="9"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/buttonMultiply"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="*"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"/>
                </LinearLayout>

                <LinearLayout
                    android:padding="10dp"
                    android:layout_width="match_parent"
                    android:layout_height="wrap_content"
                    android:orientation="horizontal">


                    <Button
                        android:id="@+id/AC"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="AC"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>

                    <Button
                        android:id="@+id/button0"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="0"
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>


                    <Button
                        android:id="@+id/buttonDot"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="."
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"
                        android:layout_marginRight="8dp"/>


                    <Button
                        android:id="@+id/buttonEquals"
                        android:layout_width="0dp"
                        android:layout_height="wrap_content"
                        android:text="="
                        android:textSize="25sp"
                        android:layout_weight="1"
                        android:background="@drawable/rounded_button"
                        android:textStyle="bold"/>
                </LinearLayout>

            </LinearLayout>

        </LinearLayout>

    </LinearLayout>

9. Lalu di File MainActivity.kt ikuti codingan dibawah ini :

    package com.example.calculator

    import android.graphics.PorterDuff
    import android.os.Bundle
    import android.text.Editable
    import android.text.TextWatcher
    import android.view.View
    import android.widget.Button
    import android.widget.EditText
    import androidx.appcompat.app.AppCompatActivity
    import androidx.core.content.ContextCompat
    import net.objecthunter.exp4j.ExpressionBuilder
    import java.lang.Exception

    class MainActivity : AppCompatActivity() {

        private lateinit var editText: EditText
        private lateinit var resultTextView : EditText

        override fun onCreate(savedInstanceState: Bundle?) {
            super.onCreate(savedInstanceState)
            setContentView(R.layout.activity_main)

            editText = findViewById(R.id.editText)
            resultTextView = findViewById(R.id.resultTextView)

            setupInputChangeListener()

            val buttonIds = arrayOf(
                R.id.button0, R.id.button1, R.id.button2, R.id.button3, R.id.button4,
                R.id.button5, R.id.button6, R.id.button7, R.id.button8, R.id.button9,
                R.id.buttonDot, R.id.buttonAdd, R.id.buttonSubtract, R.id.buttonMultiply,
                R.id.buttonDivide, R.id.buttonBr1, R.id.buttonBr2, R.id.backspace,
                R.id.AC, R.id.buttonEquals
            )

            for (buttonId in buttonIds) {
                val button = findViewById<Button>(buttonId)
                if (buttonId in arrayOf(R.id.buttonDot, R.id.button0,R.id.button1, R.id.button2, R.id.button3, R.id.button4, R.id.button5, R.id.button6, R.id.button7, R.id.button8, R.id.button9)) {
                    val color = ContextCompat.getColor(this, R.color.navi)
                    val drawable = ContextCompat.getDrawable(this, R.drawable.rounded_button)
                    drawable?.setColorFilter(color, PorterDuff.Mode.SRC)

                    button.background = drawable
                }

                if (buttonId in arrayOf(R.id.buttonEquals, R.id.buttonAdd, R.id.buttonSubtract, R.id.buttonMultiply, R.id.buttonDivide)) {
                    val color = ContextCompat.getColor(this, R.color.yellow)
                    val drawable = ContextCompat.getDrawable(this, R.drawable.rounded_button)
                    drawable?.setColorFilter(color, PorterDuff.Mode.SRC)

                    button.background = drawable
                }

                if (buttonId in arrayOf(R.id.backspace, R.id.AC)) {
                    val color = ContextCompat.getColor(this, R.color.red)
                    val drawable = ContextCompat.getDrawable(this, R.drawable.rounded_button)
                    drawable?.setColorFilter(color, PorterDuff.Mode.SRC)

                    button.background = drawable
                }

                button.setOnClickListener { onButtonClick(it) }
            }

            findViewById<Button>(R.id.buttonEquals).setOnClickListener { onEqualsButtonClick() }
        }

        private fun setupInputChangeListener() {
            editText.addTextChangedListener(object : TextWatcher {
                override fun beforeTextChanged(s: CharSequence?, start: Int, count: Int, after: Int) {}

                override fun onTextChanged(s: CharSequence?, start: Int, before: Int, count: Int) {
                    // Calculate and display result while typing
                    val expression = s.toString()
                    try {
                        val result = evaluateExpression(expression)
                        resultTextView.setText(result.toString())
                    } catch (e: Exception) {
                        // Handle invalid expressions
                        resultTextView.text.clear()
                    }
                }

                override fun afterTextChanged(s: Editable?) {}
            })
        }


        private fun onButtonClick(view: View) {
            val button = view as Button
            val buttonText = button.text.toString()
            val currentText = editText.text.toString()

            when (buttonText) {
                "AC" -> editText.setText("")
                "C" -> {
                    if (currentText.isNotEmpty()) {
                        editText.setText(currentText.dropLast(1))
                    }
                }
                else -> editText.setText(currentText + buttonText)
            }
        }

        private fun onEqualsButtonClick() {
            val currentText = editText.text.toString()
            try {
                val result = evaluateExpression(currentText)
                val resultInt = result.toInt() // Convert result to integer
                resultTextView.text = Editable.Factory.getInstance().newEditable(resultInt.toString())
            } catch (e: Exception) {
                editText.setText("Error: ${e.message}")
            }
        }




        private fun evaluateExpression(expression: String): Int {
            return ExpressionBuilder(expression).build().evaluate().toInt()
        }

    }

10. Setelah itu silakan coba untuk dijalankan. :)

