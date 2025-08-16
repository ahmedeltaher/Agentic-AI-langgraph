# دليل استخدام Template الـ Transcripts

## النمط المحفوظ لتحويل الـ Transcripts

هذا الـ template مصمم لتحويل أي transcript إلى شرح مفصل باللغة العربية العامية مع استخدام Card Style.

### كيفية الاستخدام:

1. **انسخ ملف `transcript_template.html`**
2. **استبدل المتغيرات التالية:**
   - `[TITLE_PLACEHOLDER]` - عنوان الموضوع
   - `[SUBTITLE_PLACEHOLDER]` - العنوان الفرعي
   - `[CONTENT_PLACEHOLDER]` - المحتوى الرئيسي

### المكونات المتاحة:

#### 1. Card عادي للشرح:
```html
<div class="card">
    <h2 class="card-title">📝 عنوان الموضوع</h2>
    <div class="card-content">
        <p>الشرح هنا بالمصرية العامية...</p>
    </div>
</div>
```

#### 2. Code Card (LTR) للكود:
```html
<div class="code-card">
    <h2 class="card-title">🔧 مثال الكود</h2>
    <div class="code-block">
        <pre><code>
# الكود هنا
print("Hello World")
        </code></pre>
    </div>
    <div class="card-content">
        <p>شرح الكود هنا...</p>
    </div>
</div>
```

#### 3. صناديق التنبيه:

**صندوق الأهمية:**
```html
<div class="highlight-box">
    <strong>نقطة مهمة:</strong><br>
    النص هنا...
</div>
```

**صندوق التحذير:**
```html
<div class="warning-box">
    <strong>تنبيه:</strong><br>
    النص هنا...
</div>
```

**صندوق النجاح:**
```html
<div class="success-box">
    <strong>نجح!</strong><br>
    النص هنا...
</div>
```

#### 4. شبكة المعلومات:
```html
<div class="info-grid">
    <div class="info-item">
        <h4>🎯 العنوان</h4>
        <p>الوصف هنا</p>
    </div>
    <!-- المزيد من العناصر -->
</div>
```

### قواعد الشرح:

1. **اللغة**: مصرية عامية فقط
2. **التفصيل**: شرح مستفيض ومفصل
3. **الكود**: فقط الكود المذكور في الـ transcript الأصلي
4. **النمط**: استخدام Card Style لكل موضوع
5. **الاتجاه**: RTL للنص العربي، LTR للكود
6. **عدم تكرار**: لا نضيف النص الإنجليزي الأصلي

### مثال لاستخدام الـ Template:

```html
<!-- استبدال العنوان -->
<h1>أساسيات الـ ReAct Agent في LangGraph</h1>
<p class="subtitle">فهم عميق لآلية عمل الوكلاء التفاعليين</p>

<!-- إضافة كارت الشرح -->
<div class="card">
    <h2 class="card-title">🤖 إيه هو الـ ReAct Agent؟</h2>
    <div class="card-content">
        <p>الـ ReAct Agent ده اختصار لـ Reasoning and Acting، يعني الوكيل ده بيقدر يفكر ويتصرف في نفس الوقت...</p>
    </div>
</div>

<!-- إضافة كود لو موجود -->
<div class="code-card">
    <h2 class="card-title">💻 كود المثال</h2>
    <div class="code-block">
        <pre><code>
from langgraph import Graph

# إنشاء الـ graph
graph = Graph()
        </code></pre>
    </div>
    <div class="card-content">
        <p>الكود ده بيوضح إزاي ننشئ graph جديد...</p>
    </div>
</div>
```

### ملاحظات مهمة:

- كل كود يجب أن يكون في `code-card` منفصل
- استخدم الإيموجي في العناوين لجعلها أكثر جاذبية
- اشرح بالتفصيل حتى لو المتحدث لم يشرح
- لا تضيف كود من عندك إذا لم يكن مذكور في الـ transcript
- استخدم الصناديق الملونة للنقاط المهمة

هذا النمط محفوظ ويمكن استخدامه لكل الـ transcripts القادمة!
