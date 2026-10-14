# رفع نظام جار الخليج إلى GitHub Pages

> تنبيه: البوابة الحالية تستخدم PIN/نمط/كلمة مرور محلية، وهي ليست نظام مصادقة يؤمن البيانات أو يمنع فتح صفحات apps مباشرة. لا تنشر نسخة مرتبطة بالبيانات الحساسة قبل تأمين Firebase Authentication وFirestore Security Rules، وإزالة أي كلمات مرور أو مفاتيح خاصة من الواجهات.

## طريقة الرفع

1. فك ضغط هذه الحزمة. يجب أن يظهر ملف **index.html** وبجواره **apps** و **assets** مباشرة.
2. أنشئ مستودع GitHub جديدًا (مثلاً jar-alkhaleej-portal).
3. داخل المستودع اختر **Add file > Upload files** وارفع **كل الملفات والمجلدات داخل الحزمة** مع الحفاظ على بنية المجلدات. لا ترفع ملف ZIP وحده. يمكن استعمال GitHub Desktop ونسخ المحتوى إلى المجلد المحلي للمستودع إذا كان رفع المجلدات من المتصفح غير مناسب.
4. من **Settings > Pages** حدد **Build and deployment > Source: Deploy from a branch** ثم **Branch: main** و **Folder: /(root)** واضغط **Save**.
5. افتح عنوان Pages الذي يظهر في الإعدادات، وعادةً https://USERNAME.github.io/jar-alkhaleej-portal/ .
6. جرّب التطبيقات وروابطها وصلاحيات Firebase والطباعة؛ إن استُخدمت خدمات Firebase Authentication المعتمدة على إعادة التوجيه، فقد يلزم إضافة نطاق الاستضافة إلى Authorized domains ضمن كل مشروع.

## تنبيهات مهمة

- حتى في مستودع خاص، قد تكون صفحة GitHub Pages عامة افتراضيًا؛ خصوصية الموقع تتطلب إعدادات Enterprise Cloud التي تدعم تقييد الوصول.
- GitHub Pages استضافة للملفات الثابتة فقط؛ ليست بديلاً عن المصادقة والصلاحيات الموجودة في قاعدة البيانات.
- لا تعدل مسميات الملفات أو مواقع **apps/** و **assets/** وإلا قد تنكسر الروابط.
- بعض التطبيقات تحتوي تسجيل دخول مستقل وقد تطلب بياناته حتى بعد فتح البوابة.
- الخطوات الرسمية: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
