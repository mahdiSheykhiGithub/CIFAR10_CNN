# طراحی یک شبکه عصبی عمیق :
قصد من از انجام این پروژه طراحی و ساخت یک شبکه عصبی عمیق و آموزش آن بوده است. برای انجام این پروژه به سراغ یکی از دیتاست های معروف سایت Keras رفتم. دیتاستی با 50000 عدد تصویر 32*32 رنگی برای آموزش و 10000 عدد تصویر با همین مشخصات برای test. دیتاست ما شامل 10 کلاس لیبل گذاری شده میباشد که بهتره برای آشنایی بیشتر با این دیتاست و اطلاع از کلاس ها و جزئیات به این لینک سر بزنید https://keras.io/api/datasets/cifar10/ 

# معماری شبکه :
برای طراحی این شبکه از معماری های معروف و بزرگ دنیا مثل ResNet , VGG , AlexNet ایده گرفتم و با مقایسه معماری های مختلف به این معماری که در ادامه توضیح خواهم داد رسیدم.
- دولایه Conv با 32 عدد فیلتر 3*3
- دولایه Conv با 64 عدد فیلتر 3*3
- دولایه Conv با 128 عدد فیلتر 3*3
- یک لایه پنهان Dense با 512 عدد نورون
- یک لایه خروجی با 10 نورون برای کلاس بندی

# جلوگیری از Overfit :
برای جلوگیری از بیش برازش داده ها به شکل گسترده از DropOut استفاده کردم اما اون چیزی که تا حد بسیار زیادی از overfit جلوگیری کرده است Data Augmentation بوده که این امر با جابه جایی تصاویر به سمت چپ و راست و بالا پایین و همچنین flip کردن افقی تصاویر و زوم رو تصاویر اجرا شده است.

## دقت مدل و تعداد پارامتر های یادگیرنده :
در نهایت با تعداد 4486954 عدد پارامتر یادگیرنده و 200 بار epoch به دقت 83 درصد در داده های test رسیدم



