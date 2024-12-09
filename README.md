
# OpenGK (General Knowledge in Bangla)

এই প্রজেক্টে আন্তর্জাতিক এবং বাংলাদেশের সাধারণ জ্ঞান সম্পর্কিত এমসিকিউ প্রশ্ন সংরক্ষিত আছে।
এটি প্রতিযোগিতামূলক পরীক্ষার্থী এবং সাধারণ জ্ঞান চর্চাকারীদের জন্য সহায়ক।

## প্রশ্নাবলী
- [বাংলাদেশ](./প্রশ্নাবলী/বাংলাদেশ.json)
- [আন্তর্জাতিক](./প্রশ্নাবলী/আন্তর্জাতিক.json)

## কিভাবে অবদান রাখবেন
1. নতুন প্রশ্ন যোগ করতে `.json` ফাইল এডিট করুন।
2. প্রতিটি প্রশ্নের জন্য `প্রশ্ন`, `বিকল্পসমূহ`, এবং `সঠিক_উত্তর` উল্লেখ করুন।

## API ব্যবহারের উদাহরণ
JSON ফাইল থেকে ডেটা ফ্যাচ করতে:
```
fetch('https://raw.githubusercontent.com/username/OpenGK/main/প্রশ্নাবলী/বাংলাদেশ.json')
  .then(response => response.json())
  .then(data => console.log(data));
```
