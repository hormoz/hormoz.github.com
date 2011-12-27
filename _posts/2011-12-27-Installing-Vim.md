---
layout: post
title: Test Post
---

Vim در سیستم عامل های مکینتاش لینوکس و ویندوز قابل نصب هست. برای پیدا
کردن لیست دانلود نسخه های مختلف به سایت اصلی
[Vim](http://www.vim.org/download.php) بروید هنگام نوشتن این پست نسخهی
فعلی Vim ۷.۳ هست.

### نصب Vim روی سیستمعاملهای ویندوز

برای کاربران ویندوز بهترین راه استفاده از GVim هست. برای دریافت، به
صفحهی دانلودهای سایت Vim بروید و فایل gvim73‪.‬exe را دریافت و نصب
کنید. در هنگام نصب فراموش نکنید که گزینهی

Create .bat files for command line use

رو تیک بزنید تا بتوانید از vim در command line استفاده کنید‪.‬ اگر از
Cygwin استفاده میکنید میتوانید Vim را هم به همراه آن نصب کنید. زمانی
که gvim نصب شد در command line به جای دستور vim از gvim استفاده کنید.

### نصب روی سیستمعاملهای لینوکس

به احتمال زیاد Vimدر حال حاضر روی سیستم عامل نصب هستش ولی ممکنه به روز
نباشه. برای نصب یا به روز کردن Vim سادهترین راه اینه که از package
manager سیستم استفاده کنید. برای به روز کردن اول چک کنید که Vim روی
سیستم نصب هست

`$ vim --version`

با این فرمان اگر Vim روی سیستم نصب باشه ورژن و لیست packageهای نصب شده و
نصب نشده رو نشون میده. اگر از لینوکسهای نسخهی Debian مثل Ubuntu
استفاده میکنید برای بروز کردن از فرمان زیر استفاده کنید:

`$ sudo apt-get update $ sudo apt-get upgrade vim`

اگر

vim --version

جواب نداد میتونید از دو طریق Vim رو نصب کنید. برای نصب از طریق package
manager :

`$ sudo apt-get update $ sudo apt-get install vim`

نصب Vim از سورس کد مشکل نیست و بعضیها ترجیحش میدن. آخرین نسخه (۷.۳)
رو دریافت و باز کنید:

`$ wget ftp.vim.org/pub/vim/unix/vim-7.3.tar.bz2 $ bunzip2 -c vim-7.3.tar.bz2 | tar -xf - $ cd vim73`

هنگام نصب Vim امکانات زیادی هست که میشود به صورت انتخابی آنها را انتخاب
کرد. امکانات به دستههای tiny, small, normal (the default), big و huge
تقسیم شدهاند. به نظر من Huge رو انتخاب کنید! برای نصب Vim با بستهی
انتخابی Huge فرمان زیر را وارد کنید:

`$ ./configure --with-features=huge`

اگر در زبانهای ruby، perl، python یا Tcl برنامه مینویسید Vim این امکان
رو بهتون میده تا فرمان های این زبانها رو از داخل Vim اجرا کنید و یا
اسکریپتهای برای Vim در این زبانها بنویسید. برای نصب Vim با پشتیبانی از
ruby فرمان زیر رو وارد کنید:

`$ ./configure --with-features=huge --enable-rubyinterp`

روی default برنامه در مسیر /usr/local نصب میشود. برای تغییر دادن مسیر
نصب

--prefix

رو به فرمان اضافه کنید:

`$ ./configure --with-features=huge --enable-rubyinterp > --prefix=/your/path/here`

الان Vim آماده نصبِ:

`$ make $ make install`

و آخر سر چک کنید

`$ vim --version`

### نصب روی مک

برای کاربران مک پیشنهاد میشه از MacVim استفاده کنند. چند راه برای
دریافت و نصب MacVim هست که رفتن به سایت اصلی MacVim و دریافت Universal
binary و نصبش سر راست ترین راه هست. ولی اگر از package manager هایی مثل
MacPort و یا Homebrew استفاده میکنید راه بهتر و کم دردسر اینِ که MacVim
رو از طریق اونها نصب کنید. اگر از MacPort استفاده میکنید (که اگر
میکنید بد کاری میکنید):

`$ sudo macport install macvim`

و یا اگر از Homebrew استفاده میکنید (که خوب کاری میکنید):

`$ sudo brew install macvim`

این مطلب در تاریخ سه شنبه، مرداد ۱۱م، ۱۳۹۰ در زمان ۱:۴۳ ق.ظ با موضوع
[ویرایشگرها](http://hormoz.ws/blog/topics/editors "View all posts in ویرایشگرها")
فرستاده شده است.
