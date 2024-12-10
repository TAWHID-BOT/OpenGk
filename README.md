# OpenGK - সাধারণ জ্ঞান প্রশ্ন ব্যাংক

এই রেপোটি সাধারণ জ্ঞান নিয়ে তৈরি একটি উন্মুক্ত সোর্স। এখানে **বাংলাদেশ** এবং **আন্তর্জাতিক** বিষয়ের উপর ভিত্তি করে MCQ (Multiple Choice Questions) ডাটাবেস রয়েছে।  
JSON ফরম্যাটে থাকা প্রশ্নাবলী সহজে ফেচ করে আপনার ওয়েবসাইট বা অ্যাপ্লিকেশনে ব্যবহার করা যাবে।

---

## ক্যাটাগরি সমূহ

রেপোতে নিচের ৪টি ক্যাটাগরি অন্তর্ভুক্ত করা হয়েছে:

1. **বাংলাদেশ বিষয়াবলী**
   - বাংলাদেশ-পরিচিতি.json
   - বাংলাদেশের-নদনদী.json  
2. **আন্তর্জাতিক বিষয়াবলী**
   - বিশ্ব-পরিচিতি.json
   - নদনদী.json 

---

## JSON ডেটা ফেচ করার লিংক স্ট্রাকচার

আপনার প্রয়োজনীয় ডেটা ফেচ করার জন্য লিংক স্ট্রাকচারটি হবে:
```
https://raw.githubusercontent.com/TAWHID-BOT/OpenGK/main/{ফাইল-পাথ}/{ফাইল-নাম.json}
```

- **আন্তর্জাতিক বিষয়াবলী ডেটা ফেচ করার লিংক**
```
https://raw.githubusercontent.com/TAWHID-BOT/OpenGK/main/প্রশ্নাবলী/আন্তর্জাতিক-বিষয়াবলী/বিশ্ব-পরিচিতি.json
```

---

## ডেটা ফেচ করার উদাহরণ

আপনার ওয়েবসাইট বা অ্যাপে JSON ডেটা ফেচ করার জন্য নিচের কোডটি অনুসরণ করতে পারেন:

```javascript
const fetchData = async () => {
const url = "https://raw.githubusercontent.com/TAWHID-BOT/OpenGK/main/প্রশ্নাবলী/বাংলাদেশ-বিষয়াবলী/বাংলাদেশ-পরিচিতি.json";
const response = await fetch(url);
const data = await response.json();

data.forEach((item) => {
  console.log("প্রশ্ন:", item.প্রশ্ন);
  console.log("অপশন:", item.অপশন.join(", "));
  console.log("সঠিক উত্তর:", item.সঠিক_উত্তর);
  console.log("বর্ণনা:", item.বর্ণনা);
});
};

fetchData();
