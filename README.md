
* فصل اول
    * قسمت اول  [Tailwind چیست؟](#tailwindcss-چیست؟)
      
    *  قسمت دوم  [پیش نیاز های TialwindCss ](#پیش-نیاز-های-TialwindCss)
    
      
    * قسمت سوم  [Utility ها در تلویند چی هستند](#Utility-ها-در-تلویند-چی-هستند) 
      

  


---

<div align="center">
  <img  src="./img/tailwindcsslogo.png">
</div>

<br/>

فصل 1- معرفی 


> # tailwindCss چیست؟


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

> # Utility  ها در تلویند چی هستند

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
