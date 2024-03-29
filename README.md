[![Build and deploy ASP.Net Core app to Azure Web App - hope-toolbox](https://github.com/iranxray/hope-toolbox/actions/workflows/main_hope-toolbox.yml/badge.svg)](https://github.com/iranxray/hope-toolbox/actions/workflows/main_hope-toolbox.yml)

# پروژه امید
ما در پروژه امید خواهان فراهم آوردن اینترنت آزاد برای همه ایران هستیم. هدف ما ساده‌سازی و همگانی کردن دانش عبور از فیلترینگ جمهوری اسلامی است. اینجا محفلی است برای به اشتراک گذاری تکنولوژی‌هایی که برای عبور از فیلترینگ حاکمیت ایران موثر هستند. هویت ما هیچگاه مشخص نخواهد شد و تا روز آزادی تلاش‌مان را برای گسترش اینترنت آزاد در ایران ادامه خواهیم داد.

از همه متخصصین تقاضا می‌کنیم که با مشارکت در این repo دانش خود را در زمینه عبور از فیلترینگ با همه به اشتراک بگذارند.

# تلگرام
برای اینکه محیط تعاملی بهتری در کنار هم داشته باشیم، در تلگرام‌ و توییتر هم حضور داریم.

* [کانال تلگرام](https://t.me/irxray) برای اطلاع‌رسانی‌های گروه امید.
* [گروه تلگرام](https://t.me/irxraycommunity) برای بحث و تبادل تجربه در زمینه عبور از فیلترینگ.
* [اکانت توییتر](https://twitter.com/team_omid) گروه امید برای انتشار به روز رسانی‌ها و تبادل نظر در فضای توییتر.

## این جعبه ابزار برای چه کسانی است؟
هدف اصلی ما آسان‌ کردن فرایند راه‌اندازی فیلترشکن می‌باشد. کلیک کلیک تمام! ما می‌خواهیم حتی کسانی کم‌ترین سواد فنی مرتبط هم ندارند از دیوار فیلترینگ عبور کنند و یا بتوانند برای فامیل و دوست داخل ایران اینترنت آزاد تهیه کنند. اگر می‌ترسید که سمت و سوی کارهای کامپیوتری بروید این جعبه ابزار برای شما است تا به راحتی فرایند نصب و راه‌اندازی را انجام دهید. [جعبه ابزار امید](https://hope-toolbox.azurewebsites.net/) یک وب اپلیکیشن است که به طور رایگان برای استفاده عموم در دسترس می‌باشد.

## این جعبه ابزار چه می‌کند؟
می‌خواستیم کار‌ها را تا حد ممکن ساده کنیم تا نیاز به ssh و کارهای عجیب و غریب با terminal لینوکس نداشته باشید. در حال حاضر امکانات زیر پیاده‌سازی شده‌اند:

* نصب X-UI
* صدور certificate های معتبر توسط certbot
* باز کردن پورت‌های لازم به صورت خودکار توسط ufw
* فراهم‌ آوردن مجموعه‌ای از کانفیگ‌ها و ساده‌سازی امکان نصب آن‌ها با یک کلیک

به کمک جامعه امید امکانات بیشتری به این جعبه ابزار اضافه خواهیم کرد.

## این X-UI‌ چی هست؟
ابزار X-UI یک رابط کاربری تحت وب می‌باشد که با شما اجازه می‌دهد به راحتی پروکسی ایجاد کنید و با دوستان‌تان به اشتراک بگذارید. جعبه ابزار امید جایگزین X-UI نیست. ما فقط تلاش کرده‌ایم تا برخی از کار‌ها را برای کاربران فارسی‌زبان راحت‌تر کنیم. برای یاد‌گیری در مورد [سیستم فیلترینگ و روش‌های عبور](https://github.com/iranxray/hope/blob/main/readme.md#%D8%AF%DB%8C%D9%88%D8%A7%D8%B1%D9%87-%D8%A2%D8%AA%D8%B4-%D9%81%DB%8C%D9%84%D8%AA%D8%B1%DB%8C%D9%86%DA%AF) به مقاله تیم امید رجوع کنید.

## آیا استفاده از این جعبه ابزار پیش‌نیازی هم داره؟
بله! اما فراهم‌ آوردن این پیش‌نیازها کار سختی نیست. 

۱. اول نیاز به تهیه یک `server` دارید. فرایند تهیه ساده است. کلیک کلیک تمام! ما قبلا در راهنمای امید [فرایند خرید سرور از vultr](https://github.com/iranxray/hope/blob/main/buy-server-vultr.md) را توضیح داده‌ایم.

۲. بعد هم نیاز به تهیه یک `domain` یا دامنه دارید. دامنه یک اسم در فضای اینترنت می‌باشد مثل `hope.com`. شما می‌توانید هر اسمی انتخاب کنید. این هم ساده است. کلیک کلیک تمام! اگر خیلی حوصله کار فنی ندارید ما پیشنهاد می‌کنیم که دامنه را از [CloudFlare](https://www.cloudflare.com/products/registrar/) تهیه کنید تا بدون درد و خون‌ریزی از یک سری تکنیک‌های پیشرفته‌تر مربوط به CDN استفاده کنید. 

۳. بعد از اینکه سرور و دامنه را تهیه کردید، نیاز به ساخت `رکورد A` دارید. نترسید! این رکورد یک کار مهم انجام می‌دهد و آن هم اینست که دامنه‌ خریداری شده را به آدرس IP سروری که تهیه کرده‌اید متصل می‌کند. توضیحات بیشتری در رابطه با خرید دامنه و تهیه رکورد A را در [راهنمای امید](https://github.com/iranxray/hope/blob/main/create-tsl-certificate.md#%DA%AF%D8%A7%D9%85-%D8%B5%D9%81%D8%B1) داده‌ایم. از [توضیح سرراست Cloudflare](https://developers.cloudflare.com/dns/manage-dns-records/how-to/create-dns-records#create-dns-records) هم می‌توانید استفاده کنید.  

![image](https://user-images.githubusercontent.com/118040490/212180976-fc9dcf9c-dd25-49a0-89a0-ffa44a72e427.png)


## سرور و دامنه را تهیه کردم. رکورد A هم ساختم. بعدش چی؟

از اینجا به بعد شما می‌تونید از جعبه ابزار امید استفاده کنید.

۱. وارد [وب‌سایت جعبه ابزار](https://hope-toolbox.azurewebsites.net/) امید بشید.

۲. مشخصات سرور را وارد کنیم. ما برای اتصال به سرور به دامنه، نام کاربری و رمز عبور نیاز خواهیم داشت تا بتوانیم با سرور شما ارتباط برقرار کنیم. این مشخصات را از جایی که سرور را تهیه کرده‌اید می‌توانید بگیرید. ما در [مستندات امید نحوه پیدا کردن این مشخصات برای vultr](https://github.com/iranxray/hope/blob/main/buy-server-vultr.md#%DA%AF%D8%A7%D9%85-%D9%87%D9%81%D8%AA%D9%85---%D8%A7%D8%AA%D8%B5%D8%A7%D9%84-%D8%A8%D9%87-%D8%B3%DB%8C%D8%B3%D8%AA%D9%85) را توضیح داده‌ایم.

![image](https://user-images.githubusercontent.com/118040490/212181701-06b1f910-a863-46ef-944d-38993c3afc46.png)


۳. مشخصات X-UI را وارد کنید. اگر هنوز X-UI نصب نیست نگران نباشید. ما از این مشخصات استفاده می‌کنیم که X-UI را بر روی سرور شما نصب کنیم. پورت می‌تواند هر عددی بین 10000 تا 64000 باشد. نام کاربری و رمزعبور هم به دلخواه شماست. فقط بعدا فراموش نکنید چه چیزی انتخاب کردید.

![image](https://user-images.githubusercontent.com/118040490/212182139-1f6196c0-3141-44f0-95a5-66554ccb6181.png)


۴. روی دکمه "تست ارتباط" کلیک کنید تا وضعیت ارتباط با سرور و احیانا X-UI بررسی شود.

![image](https://user-images.githubusercontent.com/118040490/212182299-3b2246ca-1100-45b1-9885-1b49ebc02cb7.png)

۵. اگر X-UI قبلا نصب نشده باشد، ما برای شما دستورات نصب را آماده می‌کنیم. صرفا کافی است که بر روی دکمه «نصب» کلیک کنید و منتظر بمانید.

![image](https://user-images.githubusercontent.com/118040490/212187084-cd3e0c94-eabd-439a-a00a-3477110f2633.png)


۶. بعد از اینکه X-UI نصب شد، مجددا بر روی «تست ارتباط» کلیک کنید تا از صحت نصب مطمئن شوید.

۷. اگر X-UI با موفقیت نصب شده باشد، ‌می‌توانید در قسمت «ساخت کانفیگ» پیشنهاد‌های ما برای نصب Trojan و VLESS را ببینید. توصیه‌ می‌کنیم که آن‌ها که با ستاره ⭐ مشخص شده اند را حتما نصب و امتحان کنید. نصب بقیه هم ضرری ندارد. با کلیک بر روی «نصب»، کانفیگ را راه‌اندازی کنید. بعد هم با کلیک روی «لینک» خواهید توانست که لینک کانفیگ را کپی کنید.

![image](https://user-images.githubusercontent.com/118040490/212183290-e67cb02a-c050-4517-9993-4d03bd5c9a33.png)


![image](https://user-images.githubusercontent.com/118040490/212184020-57370eb0-f9be-4e8a-8921-59e38070786a.png)


۸. لینک را که گرفتید از راهنمای ما برای استفاده فیلتر‌شکن در [گوشی اندروید](https://github.com/iranxray/hope/blob/main/install-android.md) و یا [آیفون](https://github.com/iranxray/hope/blob/main/install-android.md) استفاده کنید.

۹. ابزار ما برای راحتی کار شما است. فراموش نکنید ابزار اصلی یا همان X-UI بر روی سرور شما نصب شده و می‌توانید از طریق آدرس ‍‍`http://domain:xui-port` به آن متصل بشید. به جای domain باید آدرس دامنه خودتان را بزنید و به جای xui-port باید پورتی را که در گام سوم مشخص کردید وارد کنید. برای ورود هم از همان نام کاربری و رمزعبوری استفاده کنید که در گام سوم برای X-UI مشخص کردید. توضیحات بیشتر در مورد X-UI را در [مستندات امید](https://github.com/iranxray/hope/blob/main/install-xui.md#%DA%AF%D8%A7%D9%85-%D9%87%D9%81%D8%AA%D9%85) آورده‌ایم.
