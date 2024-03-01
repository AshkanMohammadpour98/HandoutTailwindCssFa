* فصل اول :clipboard:
  
    * قسمت اول  [TailwindCss چیست؟ ](#چیست؟-tailwindCss)

      
    *  قسمت دوم  [پیش نیاز های TialwindCss ](#پیش-نیاز-های-TialwindCss)
    
      
    * قسمت سوم  [Utility ها در تلویند چی هستند ](#ها-در-تلویند-چی-هستند-Utility  )
      

    * قسمت چهارم  [آیا تلویند بازدهی سایت رو کم میکنه؟! ](#آیا-تلویند-بازدهی-سایت-رو-کم-میکنه؟!)
    
 
    * قسمت پنجم  [Tailwind Css در چه وب سایت های استفاده شده ](#Tailwind-Css-در-چه-وب-سایت-های-استفاده-شده)


 
 * فصل دوم :clipboard:
   
      
    * قسمت اول  [توضیح کلی و نحوه این فصل](#توضیح-کلی-و-نحوه-این-فصل)

    * قسمت دوم  [آماده سازی  کد ادیتور و اکسیشن های مورد نیاز](#آماده-سازی-کد-ادیتور-و-اکسیشن-های-مورد-نیاز)
      
    * قسمت سوم  [نصب تلویند با استفاده از Tailwind CLI](#نصب-تلویند-با-استفاده-از-Tailwind-CLI)
    
    * قسمت چهارم بزودی... :blush: :date:


---

<div align="center">
  <img  src="./img/tailwindcsslogo.png">
</div>

<br/>

فصل 1- معرفی 


> # چیست؟ tailwindCss


*نوشته شده بر اساس دوره تلویندcss با امید بهاری فر سایت [سایت کدنایت](https://codenight.ir/courses)*

کلید یادگیری اینه که یک بار بعد دیدن دوره یا خواندن و یادگیری از حفظ یکبار و چند بار اموخته های خود را کد بزنید

تلویند فریم ورکی برای نوشتن سریع و ساده کد ها و استایل های css است.
تلویند راه حلی به شما میده که بتونیم استایل های css رو به عناصر html رو بدون اینکه از فایل html خارج بشیم اعمال کنیم.
در حالت کلی اگه با سی اس سی خالی بخوایم استایل دهی کنیم باید به عنصرمون یه ایدی یا کلاس بدیم و توی فایل سی اس اس مون اون رو انتخاب کنیم و بهش استایل بدیم هلا ممکنه برای انتخاب اسم clsss یا id درسته براش یه سری قواعد و اصولی رو ابداع کردن ولی باز هم این چالش رو به صفر نمیرسونه حتی گاهن ممکنه اون فایل سی اس اس شما خیلی طولانی شود و دیگه ندونید که از این اسم کلاس یا ایدی استفاده کردین قبلا یا خیر و اگه کلاس های هم نام یا استایل های مشابه داشته باشیم ممکنه تداخل ایجاد کنه و حتی کد های تکرار شده

```html
<div class="container">
  <!-- ... -->
</div>
```

```css
.container {
  background-color: red;
  display: flex;
  justify-content: center;
  height: 100vh;
}
```

###### فرایند استایل دهی سنتی با html , css

<br/>
<br/>

```html
<div class="flex justify-center bg-red-500 h-screen">
  <!-- ... -->
</div>
```

###### استفاده از tailwindCss
هموطور که میبینید برجای اینکه یه کلاس خاص یا ایدی براش درست کنیم و بعدن تو یه فایل سی اس اس دیگه تازه بیاییم بهش استایل هامونو اعمال کنیم اومدیم از کلاس های خاص خود تلویند استفاده کردیم این چهار تاکلاس که نوشتیم درواقع کلاس های خاص تلویند هستند یعنی تلویند این کلاس ها رو در اختیارمون قرار میده 

تلویند همه پراپرتی های css  به همراه مقادیر اونها رو در قالب کلاس های خاصی توی خودش تعریف کرده و در اختیار ما قرار داده

اینجا منضور تلویند رو متوجه شدیم اینکه توی سایت خودشونم گفته بودن دادن استایل ها بدون اینکه نیاز باشه از کد  html  خارج بشید. 
تلویند برخلاف Bootstrap  و MUI استایل و کامپوننت آماده ندارد!



همونطور که دیدیم تلویند فقط میاد نوشتن استایل های سی اس اس رو ساده تر میکنه یعنی همچنان لازمه شما استایل های خودتونو بنویسید . منتها اون شیوه نوشتن و ساده تر میشه اما بوتسترپ و متریال یو آی اینطوری نیستن اینا استایل های از پیش تعین شده  و از پیش آماده دارن مثلا خودشون عناصر و استایل های فورم یا نوبار  و ... رو دارند و اره شما تاحدودی میتونین اینا رو شخصی سازی کنید اما بیس کار توی  اما توی تلویند اینطوری نیست تلونید گقتیم فقط میاد نوشتن کد های CSS  رو ساده تر میکنه و عملا ساختار رو مجدد خودتون باید پیاده سازی کنید. 

هالا مزیت این قضیه چیه؟
اینه که شما کاملا دستتون بازه به اندازه سی اس اس خام که هر استایلی که میخواید هر دیزاینی که میخواید هر چقدر پیچیده هر چقدر هم حرفه ای  با استفاده از تلویند میتونین اون رو پیاده سازی کنید. که خب بوتسترپ و متریال یو ای خیلی جاها دست شما رو میبندند  که خب همه اون سایتایی که با بوتسترپ ساخته شده اند یه پسزمینه مشترکی دارند  چون بهم شبیه هستند استایل ها شون چون اماده هست و برای متریال یو ای هم به همین شکل 
که همه سایت هایی که با تلونید ساخته شده اند همه باهم فرق دارند  و باهم متفاوت هستند. چون دست دولوپر بازه 

`این قضیه مربوط به برتری تلویند یا متریال یو ای یا بوتسترپ نیست بلکه کاربرد اینا باهم متفاوت است . مثلا یه زمانی هست که شما میخواید یه دیزاین پیچیده و خفنی رو درست کنید لازمه که دستتون باز باشه با پراپرتی های سی اس اس بازی کنید واینجور مواقع تلویند به کارمون میاد 
ولی یه زمانی هست که میخوایم خیلی سریع یه دیزانی رو جمع و جور کنیم که کارو رابندازه و  مثلا سایتمون یه دیزاین ساده میخواد بوتسترپ و متریال یو ای خیلی کاربردی ترن هر کدوم به جای خود.
`

---

> # پیش نیاز های TialwindCss

<br/>

<div align="center">
  <img  src="./img/html css log.png">

_Html , Css ضروری_

 تسلط به زبان نشانه گزاری html  ضروری و تسلط به css  ضروری


</div>


<div align="center">
  <img  src="./img/npm-node-package-manager-logo-DE93649ED1-seeklogo.com.png">
  <img  src="./img/Javascript.png" width="200">

_JavaScrip , Npm مزیته اجباری نیست_

</div>

---

> # ها در تلویند چی هستند Utility  

اینکه خود سایت تلویند هم میگه تلویند یه فریم ورک  utility-first هست به چه معنی هست. و یوتیلیتی در اختیار کاربرش قرار میده و اجازه میده که ما از این utility  های استفاده کنیم و با استفاده از این utility  ها استایل خودمون رو به عناصر اعمال کنیم.

تلویند مجموعه ای از یوتیلیتی ها رو در اختیارمون قرار میده مثل کلاس های ریز که هرکدوم کاری انجام میدن و ما میتونیم دونه دونه این کلاس ها که ما بهش میگیم utility  رو به عنصرمون بدیم و  بتونیم اون استایل نهایی رو روش داشته باشیم .

خب شاید سوالی که به زهنتون برسه این باشه خب اگه همه اون استایل های مثل کلاس هستند چرا نیاییم اتربوت style  رو بصورت انلاین بدیم به عناصر و اینطوری استایل ها مون رو اعمال کنیم


```html
    <!-- inline style -->
    <div style="display: flex; background-color: red;">...</div>
```

```html
    <!-- utilitie class tailwindCss -->
    <div class="bg-red-500 flex"></div>
```
<br/>

مهمترین دلیلی که این یوتیلیتی کلاس ها بر اینلاین استایل ها برتری داشته باشند اینه که شما در اینلان استایل ها نمیتونین به مدیاکویری ها دسترسی داشته باشید مدیا کوییری منضور همون دیزاین ریسپانسیو است از طریق انلاین استایل ها مقدور نیست اما تلویند طوری طراحی شده که شما میتونین این یوتیلیتی کلاس ها رو درحالت ریسپانسیو  هم استفاده کنین
مورد بعدی شما در حالت اینلاین استایل ها نمیتونیم به hover , focuse و ... دستری داشته باشیم  مثلا از طریق انلاین استایل نمیتونیم به حالت هاور یه دکمه استایل بدیم  ولی باز هم تلویند فکر اینجاشم کرده و  برای استایل دهی کردن در حالت هاورهم  و سایر... هم سینتکسی داره 
یه نکته دیگه شما اگه از انلاین استایل ها استفاده کنید نمیتونید که مثلا یه کد رنگی داخل یک متغیری تعریف کنیم و بعد از اون اسمه متغیر استفاده کنید  هر بار اگه خاستین یه کد رنگی بنویسد هربار باید اون رو تایپ کنین	 ولی خب تلویند این امکان رو به شما میده که یه سری مقادیر رو داخل یه سری متغیر تعریف کنید و دیگه مجبور نشید هر بار  اون مقدار رو بصورت دستی تایپ کنیم بلکه بجاش از اسم اون متغیر استفاده کنیم که کارمون راحت تر بشه و بعدن هم اگه خاستیم بصورت کلی  اون رنگ یا مقدار رو برای همه عوض کینم خیلی راحت تره 	 
این بصورت کلی برتری یوتیلیتی کلاس ها بر انلاین استایل ها بود
Inline-style , utility-class

---

> # آیا تلویند بازدهی سایت رو کم میکنه؟!

ایا تلویند تاثیر منفی روی سایت میزاره یا مثلا سرعت سایت رو کم میکنه یه سرعت لود سایت رو کم میکنه؟ خیر

تلویند به هیج عنوان پرفورمنس سایت یا سرعت سایت رو کم نمیکنه  بهرحال شاید شنیده یا دیده باشید هر پکیجی تاثیر منفی کمی روی پروژه میزاره  و این طبیعی و مشخصه 
ولی راجب تلویند اینطروی نیست چرا؟
اگه خاطرتون باشه ما از یوتیلیتی های تلویند چند صفحه قبل استفاده کردیم تلویند یه سری یوتیلیتی هایی رو به ما میده که با مجموعه اینا  روی هر کدوم از عناصر سایتمون به اون استایل موردنظر میریسیم 
هالا نکته ای که وجود داره تریکی که تلویند میزنه  اینکه بعد از اینکه فرایند توسعه پروژه ما تموم شد  زمانی که خاستیم نسخه  نهایی رو  استخراج کنیم تلویند تو اون مرحله میاد کل سورس کد  اون قسمتی که براش مشخص میکنیم رو میاد اسکن میکنه و برسی میکنه 	 و  صرفن اون یوتیلیتی هایی که ما ازش استفاده کردیم  رو تشخیص میده  یعنی تشخیص میده که ما از کدوم یوتیلیتی ها استفاده کردیم  و به عنوان خروجی خودش فقط و فقط یه استایل شیت  شامل اون یوتیلیتی هایی که ما ازشون استفاده کردیم اریه  میده  یعنی تنها یادگاری تلونید روی پروژه هایی که از تلویند استفاده میشه  توی خروجی نهایی  یه استایل شیت کاملا بهینه  از اون یوتیلیتی های تلویندی هست که کاربر ازش استفاده کرده  و دیگه بقیه یوتیلیتی هایی که ازش استفاده نکردیم رو توی اون استایل شیتش نمیاره  
و این خروجی سبک و بهینه شده باعث میشه که  تلویند هیچ تاثیر منفی  روی پرفورمنس سایت نزاره و حتی این فایل استایل شیتی که تلویند تو خرجی بهون میده از استایل شیت روش سنتی که قبلا مینوشتیم  خیلی وقتا بازدهی بیشتر و بهتری داره  به این علت که اولا کد تکراری نداره  و خب هرکدوم یوتیلیتی های داخلش هم چند باز مصرف هستن به همین دلیل نه تنها  پرفورمنیس سایتمون رو بدتر نمیکنه بلکه ممکنه در برخی موارد  بهنیه ترم است.

---
> # Tailwind Css در چه وب سایت های استفاده شده

<br/>

وب ساست open ai  هوش مصنوعی چت جی پی تی.

<div align="center">
  <img  src="./img/openAi imge.PNG" width="300">
  
  Openai.com
</div>

<br/>

وب سایت دات نت که برای شرکت مایکروسافت است.
<div align="center">
  <img  src="./img/Net.PNG" width="300">
  
  Dotnet.microsoft.com
</div>

<br/>


وب سایت next.js

<div align="center">
  <img  src="./img/Nextjs.PNG" width="300">
  
  nextjs.org/docs
  
</div>

<br/>

وب سایت کد نایت
<div align="center">
  <img  src="./img/Codenight.PNG" width="300">
  
  codenight.ir
</div>

---
فصل دوم : نصب تلویند وآماده سازی محیط توسعه در فریم وک های مختلف

> # توضیح کلی و نحوه این فصل


توی این فصل اکستیشن ها و مواردی که توی کد ادیتور مون نیاز داریم میپردازیم  ونصب میکنیم و اگه نرم افزاری  روی  کامپیوترمون لازم است نصب میکنیم. و درقدم بعدی تلویند رو به پروژه خودمون اضافه میکنیم.

نکته ای که هست ما توی طول این دوره تلویند رو روی html , css خالی نصب و کار میکنیم . اما اگه خودتون به فریم ورک های دیگه مثل react , next , nuxt ,… تسلط دارید اموزش نصب تلویند روی اون ها هم هست توی داکیومیشن اصلی تلویند و توی دوره 
پس ما تلویند رو روی پروژه خالی html , css   نصب میکنیم  tailwind CLI  رو نصب میکنیم .
البته که کارکرد تلویند روی css , html خالی با فریم ورک های  js  فرقی نداره فقط فرایند نصبشون یکم باهم فرق دارند	
از طریق سایت خود تلویند قسمت داکیومیشن و قسمت نصب  میتونین نصب تلویند و دستورات نصب روی فریم ورک های مختلف رو میتوینن نصب کنین
1-	وارد وب سایت tailwindcss.com
2-	از منوی بالا وارد بخش DOC  بشین داکیومیشن
3-	از منوی سمت چپ  روی Getting Start  بشن  صفحه ای که براتون میاد هم یه منو داره روی  Framework Guids  بشن و لیست لایبری ها و کتاب خانه ها 

https://tailwindcss.com/docs/installation/framework-guides

<div align="center">
  <img  src="./img/installation part-1.PNG"  >
  <img  src="./img/installation part-2.PNG" >
  
</div>
---

> # آماده سازی  کد ادیتور و اکسیشن های مورد نیاز

اکسیشن های کاربردی
Tailwind CSS IntelliSense
که خود تلویند اون رو برای vscode توسعه داده و پیشنهاد اینه که اگه از تلویند داخل پروژه تون استفاده میکنین این extensons رو نصب کنین که راحتر و سریعتر کد بزنین

 <img  src="./img/extation tailwind css isteliSense.PNG" width="300" >

 کاری که این اسیشن برای ما انجام میده میاد یوتیلیتی های تلویند رو موقع کد نویسی برای ما پیشنهاد میکنه یعنی دیگه ما لازم نیست همه یوتیلیتی ها ی تلویند رو حفظ باشیم یه ذره شو که بنویسیم خودش کاملشو پیشنهاد میده

اکستیشن دوم prettier-Code formatter  است


<img  src="./img/extation Prettier code formatter.PNG" >

کاری که این اکستیشن انجام میده اینه که کد های شما رو مرتب میکنه و نتضم میده که کد های تلویندی و ساختار html , ….. رو هم منظم میکنه که کد های تر تمیز تری میکنه.
که با کلید های ترکیبی alt + shift + f عمل میکنه.

همچنین نرم افزاری که نیاز هست برای نصب و راهندازی تلویند نرم افزار 

<img  src="./img/Node.js_logo.svg.png" width="300">
است nodeJs  

---

> # نصب تلویند با استفاده از Tailwind CLI


ما وقتی میخوام تلویند رو به پروژه html , css  خام خود نصب کنیم از  tailwind css CLI   استفاده میکنیم .
بعنی تنها راه مطلوب و درست حسابی استفاده از این تلویند سی اس ای است
خب ما وارد ادرس  و وب سایت tailwindcss.com میشویم  وارد بخش DOC  میشیم و توی بخش installation  روش نصب با استفاده از  tailwind CLI  رو نوشته

برای اینکه بخوایم tailwind cli  رو نصب کنیم  ابتدا لازمه که npm  رو وارد پروژه کنیم که بخاطر همین بود که در جلسه های اول اومدیم و نود جی اس رو نصب کردیم  npm رو که نصب کردیم پکیج هایی که نصب میکنیم تویه قسمت و یه بخش اسم هاشون است
وارد ترمینال و مسیر پروژه میشیم فرض کیند که یه پوشه به اسم tailwind-cli  رو داریم با ترمینال یا cmd  و یا getbash وارد اون مسیر پوشه ای که درست کردیم میشم و  npm  رو نصب میکنیم با دستور 
```
npm init
```
که این دستور حاصل از اون نرم افزار نود جی اس است که جلسه های پیش نصب کردیم اون این دستورات  npm  رو برای ما باز میکنه وقتی این دستور رو زدیم خود نود جی اس شروع به افزودن npm  به پروژه یا پوشه ما میکنه
البته موقع نصب  npm یه سری سوالات ازمون میپرسه که اونا رو رد میکنیم مثل اسم پروژه و ورژنش چیه توضیحات و ... اسم نویسنده پروژه ویه سری سولات
ها لا یه فایل به اسم و پسوند pacage.json   به پوشه ای که ساختیم اضافه میشه 
هالا ما هر پکیج و یا کتاب خانه ای با  npm  نصب کنیم اسمش و ورژن و اطلاعاتش میاد تو این فایل 

خب هالا بریم که تلویند سی ال ای رو نصب کنیم با  npm 
```
npm install -D tailwindcss
``` 
وقتی که این دستور رو بزنیم یه فولدر node_modules  اضافه میشه که وابستگی های پروژه تلویندی ما هست و یه فایل pacage-lock.json  هم اضافه میشه  و همجنین داخل اون فایل pakage.json  مون هم یه قسمت "devDependencies" که داخلش نوشته شده   "3.3.7":"tailwindcss" اسم پکیجی که نصب کردیم و ورژن اون هست . 


<img  src="./img/packagejson.PNG" >

که این کار باعث این میشه که هروقت ما این پروژه رو بدون اون فولدر node_modules  که حجمش یکم زیاده بدون اون بدیم هر کسی و اون شخص دستور
```
npm install 
```
رو که بزنیه مجدد بر اساس اون فایل pakage.json  که هر پکیجی اسمش باشه نصب میشه و اون فولدر node_modules  ساخته میشه .


خب هالا مرحله بعدی اینه که لایبیری تلویند رو روی پروژه استارت بزنیم که فایل هایی که بهش نیاز دار رو روی پروژه بسازه و خب برای اینکه تلویند کارشو روی پروژه ما انجام بده نیاز داره که فایل  tailwind.config.js رو داشته باشیم که کانفیگ ها و تنظیماتمون رو توش اعمال کنیم.
کامند استارت زدن تلویند روی پروژه مون
```
npx tailwindcss init
```
میبینیم که فایل   tailwind.config.js به پروژه مون اضافه میشه که این فایل هسته یا کور اصلی تلویند هست  همه تنظیمات تلویند مون رو توی این فایل انجام میدیم
فرض کنین که ساختار پروژه ما به این شکل است و
کاری که میخوایم انجام بدیم اینه که همه اون یوتیلیتی هایی که توی فایل index.html  برای عناصر  نوشتیم توسط پکیج تلویند شناسایی و اسکن بشه  و از روی یوتیلیتی هایی که نوشتیم یک استایل شیت نهایی خروجی ساخته بشه 
یعنی عملا کاریی که میخواییم بگیم این فایل html   که مثلا توی این پوشه public  است این فایل هایی html رو اسکن کن یوتیلیتی هایی که استفاده کردیم رو استخراج کن در قالب یک فایل   استایل شیت نهایی بده که بعدن ما بتونیم اون فایل نهایی رو لینک کنیم به سند  html لینک کنیم و استایل هامون رو توی پروژه داشته باشیم.
برای اینکار ابتدا وارد اون فایل tailwind.config.js میشیم و توی قسمت
``` ["./public/**/*.html"] : "content" ```
وارد مسیر پوشه هایی که داخل اونا از یوتیلیتی هایی تلویند استفاده کردیم که توی این مثال فقط این یه پوشه داریم گفتیم که **  یعنی همه هرچی پوشه و فایل داریم *.html  یعنی همه فایل هایی که با پسوند .html هستند رو بیا اسکن کن  و باتوجه به اینا بیا جنریت کن  بساز استایل شیت تو 

<img  src="./img/pachagejson routes.PNG" >


> [!NOTE]
> یه نکته اگه چند تا فولدر دارین این ارایه رو میتونین یه  ,    بزارین و یه مسیر دیگه ی رو هم بنویسید.

پس مرحله اول انجام شدالان گفتیم که توی این فولدر دنبال یوتیلیتی ها بگرد و اسکن کن توی مرحله بعدی لازمه که یه استایل شیت ورودی به تلویند بدیم تلویند به یه فایل  css   به عنوان ورودی  که بتونه یه سری استایل های پایه ای خودشو  توی این فایل ورودی لود کنه  و بعدن اونها رو کامپایل کنه داخل فایل css خروجی خودش اونها رو قرار میده 
از اون طرف یه فایل css  خروجی هم میخواد که استایل هایی نهایی یوتیلیتی هایی که استفاده کردیم اونجا قرار بگیره.
و اون فایل style.css نهایی که برای خروجی  ساختیم رو به سند html  لینک میکنیم. 



