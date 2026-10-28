BUY & SELL — शुरुआती वेबसाइट + PWA डेमो
==========================================

इस पैकेज में
- index.html       ग्राहक स्टोर / उत्पाद खोज / कार्ट डेमो / विक्रेता उत्पाद फॉर्म
- admin.html       स्थानीय डेमो Admin Panel
- styles.css       मोबाइल-फ्रेंडली डिजाइन
- app.js           स्टोर का डेमो लॉजिक
- admin.js         उत्पाद मंजूर/अस्वीकार/हटाने का डेमो
- manifest.webmanifest, sw.js, icon-192.png, icon-512.png
- firestore.rules.example  भविष्य में Firebase Firestore के लिए उदाहरण नियम
- FIREBASE-SETUP-HI.txt    लाइव बैकएंड जोड़ने की अगली योजना

महत्वपूर्ण सीमा / सुरक्षा
-------------------------
यह शुरुआती FRONTEND DEMO है, लाइव मार्केटप्लेस नहीं।
1. उत्पाद और कार्ट उसी ब्राउज़र के localStorage में सेव होते हैं।
2. दूसरे मोबाइल पर डेटा अपने-आप साझा नहीं होगा।
3. Admin Panel में वास्तविक authentication/authorization नहीं है। इसे निजी डेमो के अलावा सार्वजनिक लाइव डेटा के लिए न इस्तेमाल करें।
4. भुगतान, वास्तविक ऑर्डर, OTP, विक्रेता सत्यापन, रिटर्न, डिलीवरी, ईमेल/SMS शामिल नहीं हैं।
5. URL से दिखाई जाने वाली उत्पाद फोटो बाहरी साइट पर हो सकती है। अज्ञात URL न डालें।
6. केवल HTTPS hosting पर PWA install/offline सुविधा ठीक से काम करती है (localhost भी विकास के लिए मान्य है)।
7. यह पैकेज अपने-आप APK नहीं बनाता। Android ऐप के लिए बाद में PWA/TWA या native wrapper और Play Console प्रक्रिया चाहिए।

अपने कंप्यूटर पर जाँच
---------------------
1. ZIP को extract करें।
2. आसान तरीका: index.html को ब्राउज़र में खोलें। कुछ PWA सुविधाएँ नहीं चलेंगी।
3. PWA/service worker जाँचने के लिए HTTPS hosting या localhost का उपयोग करें।
4. index.html में उत्पाद जोड़ें; admin.html खोलकर उसे मंजूर/अस्वीकार करें।
   ध्यान दें: दोनों एक ही ब्राउज़र और उसी origin पर चलें, तभी localStorage साझा होगा।

GitHub Pages पर डालना (अगला कदम)
--------------------------------
1. GitHub पर नया repository बनाएँ।
2. ZIP extract करके सभी फाइलें repository के root में upload करें।
3. Settings → Pages → Deploy from a branch → main / root चुनें।
4. प्रकाशित HTTPS URL खोलें। GitHub Pages पर सीधे .html file URL भी काम करेगा।
5. Admin panel का URL /admin.html होगा, पर इसे सार्वजनिक वास्तविक प्रबंधन के लिए न इस्तेमाल करें।

लाइव उत्पादन के लिए आवश्यक
-------------------------
- Firebase Authentication या अन्य सुरक्षित auth
- Firestore/समान डेटाबेस और server-enforced role checks
- उत्पाद चित्रों के लिए सुरक्षित Storage rules, file type/size validation
- server-side order creation, stock validation और payment verification
- भुगतान प्रदाता की webhook signature verification
- privacy policy, terms, returns/refunds, grievance contact
- लागू भारतीय ई-कॉमर्स/GST/उपभोक्ता नियमों की पेशेवर जाँच

इस डेमो को लाइव बिक्री चालू होने का प्रमाण न मानें।
