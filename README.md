# प्रवेश जन सेवा केंद्र — GitHub Pages पैकेज

यह एक static HTML frontend package है। इसे GitHub repository के root में `index.html` के रूप में रखने पर GitHub Pages से वेबसाइट प्रकाशित की जा सकती है।

## GitHub पर Live करने के चरण

1. GitHub में नया Public repository बनाएं, उदाहरण: `pravesh-jan-seva-kendra`।
2. इस पैकेज की सभी फाइलें repository के **root** में upload करें (`index.html`, `.nojekyll`, `README.md`)।
3. Repository में **Settings → Pages** खोलें।
4. **Build and deployment** में `Deploy from a branch` चुनें।
5. Branch `main` और folder `/(root)` चुनकर **Save** करें।
6. कुछ मिनट बाद Pages में दिया गया `https://<username>.github.io/<repository>/` URL खोलें।

## जरूरी तकनीकी सीमा — इसे पढ़कर ही वास्तविक ग्राहकों को दें

यह पैकेज अभी frontend/demo है, पूर्ण production portal नहीं। मौजूदा HTML/JavaScript में:

- यूजर, लॉगिन, आवेदन और डैशबोर्ड का डेटा browser page के JavaScript memory में है; server database में save नहीं होता। Reload/दूसरे device पर डेटा भरोसेमंद तरीके से उपलब्ध नहीं रहेगा।
- Demo accounts और demo OTP मौजूद हैं। OTP असली SMS से नहीं जाता।
- अपलोड की गई PDF का वास्तविक content server पर upload नहीं होता; वर्तमान flow मुख्यतः file name दर्ज करता है।
- Payment flow वास्तविक payment gateway से जुड़ा हुआ नहीं है।
- GitHub Pages केवल static hosting है; यह secure backend, database, file storage, SMS OTP या payment processing उपलब्ध नहीं कराता।

**इसलिए अभी इसे preview/demo के रूप में live करें।** असली customer data, Aadhaar/PAN या अन्य संवेदनशील दस्तावेज़, वास्तविक पैसे या production login इस्तेमाल न करें। सुबह से वास्तविक संचालन के लिए अलग secure backend, database, private file storage, authentication/OTP provider और payment gateway integration तथा security testing जरूरी है। GitHub पर passwords, API keys या customer documents कभी commit न करें।
