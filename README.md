ابتدا باید یک پروژه انگولار جدید ایجاد کنیم.

```
ng n <Project-Name>
```

سپس باید بوت استرپ رو روی پروژه‌مون نصب کنیم.

```
npm install bootstrap
```

حالا باید با آدرس دهی بوت استرپ رو به پروژه اضافه کنیم، به آدرس زیر که تنظیمات کلی انگولار در اونجا قرار داره می‌رویم.

```
angular.json
```

در فایل بالا، عبارت `"build"` را سرچ می‌کنیم و کمی پایین‌تر از آن قسمت استایل را مشاهده می‌کنیم. در حالت پیش‌فرض به صورت زیر است.
`"styles": [`
	`"src/styles.scss"`
 `],`
 باید بوت استرپ را زیر استایل scss آدرس‌دهی کنیم و به این موضوع که انتهای آدرس scss یک , قرار دهیم نیز دقت کنیم.
 
```
 "styles": [

              "src/styles.scss",

              "./node_modules/bootstrap/dist/css/bootstrap.rtl.min.css"

            ],
```

حالا بوت استرپ با موفقیت وارد پروژه ما شده است. برای زدن اولین کدمون باید انگولار رو استارت کنیم برای این کار از دستور زیر استفاده می‌کنیم.

```
ng s
```

که این دستور حتما باید در دایرکتوری اصلی انگولار اجرا شود.
با این کار انگولار روی لوکال هاست با پورت 4200 اجرا می‌شود.
برای زدن کد باید به پوشه src سپس app برویم، برای ادیت html فایل زیر را باز می‌کنیم و محتویات آن را پاک می‌کنیم.
app.component.html
ابتدا با یک کد bootstrap شروع می‌کنیم و تست می‌کنیم که بوت استرپ به درستی در پروژه قرار گرفته باشد.
از کد زیر برای پروژه‌مون استفاده می‌کنیم.

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  <div class="row">
    <div class="col-2"></div>
    <div class="card col-3 mt-3 ">
      <img src="https://cdn.create.vista.com/api/media/small/18433525/stock-photo-mountain-summit-sunrise-or-sunset"
        class="card-img-top">
      <div class="card-body">
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
          content.</p>
      </div>
    </div>
    <div class="col-2"></div>
    <div class="card col-3 mt-3 ">
      <img src=https://static9.depositphotos.com/1222912/1091/i/450/depositphotos_10917587-stock-photo-fantasy-landscape.jpg"
        class="card-img-top">
      <div class="card-body">
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's
          content.</p>
      </div>
    </div>
    <div class="col-2"></div>
  </div>
</body>
</html>
```

حالا ما ظاهر لازم رو داریم و باید یک دکمه ایجاد کنیم که با کمک آن کارت بعدی باز یا بسته شود. برای نوشتن یک تابع وارد فایل `app.component.ts` می‌شویم.

```
export class AppComponent {
  title = 'EX1-Cards';
}
```

در این قسمت از فایل می‌توانیم توابعی که می‌خواهیم در app-component اجرا شوند را بنویسیم.
توابع باید با زبان تایپ اسکریپت نوشته شوند.
ما یه تابع می‌خوایم یه مربع باشه هر بار که روش کلیک می‌کنیم. یه کارت دیگه مثل کارت قبلیمون برامون بسازه.
