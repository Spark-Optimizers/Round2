<p align="center">
  <a href="" rel="noopener">
 <img src="http://optimizer.math.sharif.edu/wp-content/uploads/2021/02/optimizer.png" alt="Optimizer logo"></a>
</p>
<h3 align="center">تیم اسپارک</h3>


## 📝 فهرست مطالب
- [صورت‌بندی سوال](#problem_statement)
- [الگوریتم بهینه‌سازی](#idea)
- [محدودیت‌ها](#limitations)
- [ایده‌های گسترش](#future_scope)
- [روند اجرا](#getting_started)
- [نحوه استفاده](#usage)
- [وابستگی‌ها](#tech_stack)
- [نویسندگان](#authors)

## 🧐 صورت‌بندی سوال <a name = "problem_statement"></a>
صورت برنامه‌ریزی :
  
  ```math
  min  ||v||_0
  s.t.  Sv=0
        l <= v <= u
  ```
تابع نرم صفر یک تابع غیر محدب و ناپیوسته است و میتوان نشان داد که برنامه ریزی بالا 
<div>NP-hard</div>
است. پس تابع هدف را با تابع نرم یک جایگزین میکنیم. در این قسمت برای نشان دادن قدر مطلق در تابع عدف از دو قید معادل استفاده میکنیم:

 ```math
  min  a_1 + a_2 + ... + a_n
  s.t.  Sv=0
        l <= v <= u
        a >= v
        a >= -v
  ```
  
 با پیاده سازی این بخش در جومپ میتوان به یک جواب شدنی رسید. اما برای بیشتر کردن تعداد سطر های صفر دو روش مختلف به کار گرفتیم :
 </br>
 روش اول : وزن دار کردن تابع هدف و به روز رسانی وزن ها
 </br>
 ایده‌ی کلی این است که هر درآیه از بردار تابع هدف را وزن دار کنیم و با بزرگ شدن اندازه‌ی آن بردار وزن متناظر با آن را آپدیت کنیم به گونه ای که اثر درآیه ها بزرگتر در تابع هدف کمتر شود. این ایده  در  
 <a href="https://ttu-ir.tdl.org/bitstream/handle/2346/ETD-TTU-2010-12-1056/JAIN-THESIS.pdf?sequence=2">این مقاله</a>
بررسی شده است.
</br>
روش دوم :
استفاده از خروجی قسمت قبل و اضافه کردن سطر های صفر شده به عنوان قید به تابع هدف.
</br>
این ایده توسط متین امینی مطرح شد و تعداد سطر های صفر را کمی افزایش داد.
  
## 💡 الگوریتم بهینه‌سازی <a name = "idea"></a>

روش ها و رفرنس در بخش قبلی ذکر شدند.


## ⛓️ محدودیت‌ها <a name = "limitations"></a>
محدودیتی در این بخش وجود ندارد و با نصب
پکیج های مورد نظر 
میتوان یک جواب شدنی برای هر ۳ ورودی مسابقه به دست آورد.

## 🚀 ایده‌های گسترش <a name = "future_scope"></a>
در ایده‌ی آپدیت کردن وزن ها شاید بتوان از تابع موثر تری برای به روزرسانی وزن ها استفاده کرد.
در این صورت کافیست تابع
<div>update_weights</div>
را با فرمول دیگری بازنویسی کرد.

## 🏁 روند اجرا <a name = "getting_started"></a>

نوت بوک شامل دو بخش است. بخش اول، پیاده سازی ایده‌ی اضافه کردن قید سطر صفر و بخش دوم پیاده سازی  ایده‌ی آپدیت کردن وزن هاست.
هر بخش یک خروجی میدهد که تعداد سطر های صفر در آن ها تفاوت اندکی دارد. در نهایت خروجی بهتر را سابمیت کردیم.

### پیش‌نیازها
  

## 🎈 نحوه استفاده <a name="usage"></a>
ابتدا بخش خواندن ورودی در نوت بوک ها را اجرا کنید. سپس میتوانید پیاده سازی هر ایده را که در نوت بوک به صورت جداگانه مشخص است ران بگیرید و خروجی در همان مسیر اجرایی ذخیره میشود.


## ⛏️ وابستگی‌ها <a name = "tech_stack"></a>
  برنامه در زبان جولیا نوشته شده و لیست پکیج های مورد نیاز در ادامه آمده است :
```
  MAT
  JuMP
  GLPK
  SparseArrays
  DelimitedFiles
```

## ✍️ نویسندگان <a name = "authors"></a>
ایده‌ی آپدیت کردن وزن ها توسط آیدا افشارمحمدیان مطرح و پیاده سازی شد.
</br>
ایده‌ی اضافه کردن قید های سطر صفر توسط متین امینی مطرح و پیاده سازی شد.
</br>
متاسفانه خانم مهرانی به دلیل مشکلاتی نتوانستند به همکاری در مسابقه ادامه دهند.
