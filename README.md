 مشروع Arduino: تشغيل لمبة عند الضغط على زر
Arduino LED Blink on Button Press

🧾 الوصف | Description
مشروع بسيط باستخدام لوحة Arduino يتم فيه توصيل ثلاث أزرار بثلاث لمبات LED. كل زر عند الضغط عليه يجعل اللمبة المرتبطة به تضيء وتطفئ لمدة قصيرة. عند عدم الضغط على أي زر، يتم إطفاء جميع اللمبات.

A simple Arduino project where three buttons control three LEDs. Pressing a button makes the corresponding LED blink briefly. If no buttons are pressed, all LEDs remain off.

🔌 المكونات | Components
لوحة Arduino ( Uno)

3× أزرار (Push Buttons)

3 × لمبات LED

3 × مقاومات 220 أوم (لـ LEDs)

مقاومات إضافية للأزرار (10 كيلوأوم) إذا لم يتم استخدام INPUT_PULLUP

أسلاك توصيل

لوح تجارب (Breadboard)

⚙️ التوصيل | Wiring
الزر	المنفذ	اللمبة	المنفذ
زر 1	D7	LED 1	D13
زر 2	D4	LED 2	D12
زر 3	D2	LED 3	D8

تأكد من أن كل زر متصل بالأرضي (GND) على أحد الأطراف والمنافذ الرقمية من الطرف الآخر. استخدم مقاومة pull-down إذا لزم الأمر.

💻 الكود | Code

void setup(){
 pinMode(7, INPUT);
 pinMode(4, INPUT);
 pinMode(2, INPUT);
 pinMode(13, OUTPUT);
 pinMode(12, OUTPUT);
 pinMode(8, OUTPUT);
}

void loop(){
  if (digitalRead(7) == HIGH) {
    digitalWrite(13, HIGH);
    delay(300);
    digitalWrite(13, LOW);
    delay(300);
  } else if (digitalRead(4) == HIGH)  {
    digitalWrite(12, HIGH);
    delay(300);
    digitalWrite(12, LOW);
    delay(300);
  } else if (digitalRead(2) == HIGH)  {
    digitalWrite(8, HIGH);
    delay(300);
    digitalWrite(8, LOW);
    delay(300);
  } else {
    digitalWrite(13, LOW);
    digitalWrite(12, LOW);
    digitalWrite(8, LOW);
  }
}

✅ كيفية الاستخدام | How to Use
1-حمّل الكود إلى لوحة Arduino الخاصة بك.

2-شغّل الدائرة.

3-اضغط على أي زر لمشاهدة اللمبة المقابلة تضيء وتنطفئ.

4-اذا لم يتم الضغط على أي زر، ستبقى جميع اللمبات مطفأة.

