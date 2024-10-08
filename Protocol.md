### TCP (Transmission Control Protocol)
#### توضیحات کلی
TCP یکی از پروتکل‌های اصلی مجموعه پروتکل‌های اینترنت (IP) است که برای انتقال داده‌ها به صورت قابل اعتماد و با تضمین تحویل کامل استفاده می‌شود. این پروتکل در لایه انتقال مدل OSI عمل می‌کند.

#### ویژگی‌ها
- **اتصال‌محور:** برای برقراری ارتباط، ابتدا یک اتصال (Connection) بین کلاینت و سرور ایجاد می‌شود.
- **قابلیت اطمینان:** تضمین می‌کند که داده‌ها به ترتیب و بدون از دست رفتن به مقصد می‌رسند.
- **کنترل جریان:** از مکانیزم‌هایی برای جلوگیری از ارسال بیش از حد داده‌ها به یکباره استفاده می‌کند.
- **کنترل خطا:** از چک‌سام‌ها و مکانیسم‌های بازپخش برای تصحیح خطاها و بازیابی داده‌های از دست رفته استفاده می‌کند.
- **سه‌مرحله‌ای هندشیک (Three-Way Handshake):** برای برقراری ارتباط، از یک فرآیند سه مرحله‌ای استفاده می‌شود که شامل ارسال SYN، دریافت SYN-ACK و ارسال ACK می‌شود.

#### کاربردها
- **وب و مرورگرها:** HTTP و HTTPS
- **ایمیل:** SMTP، IMAP، POP3
- **انتقال فایل:** FTP
- **پروتکل‌های از راه دور:** SSH، Telnet

### UDP (User Datagram Protocol)
#### توضیحات کلی
UDP نیز یکی از پروتکل‌های لایه انتقال است، اما برخلاف TCP، اتصال‌محور نیست و داده‌ها را به صورت بدون اتصال و غیرقابل اعتماد ارسال می‌کند.

#### ویژگی‌ها
- **بدون اتصال:** نیازی به ایجاد و نگهداری اتصال ندارد.
- **غیرقابل اعتماد:** تضمینی برای تحویل داده‌ها یا ترتیب آنها وجود ندارد.
- **سرعت بالا:** به دلیل عدم استفاده از مکانیزم‌های کنترل جریان و کنترل خطا، دارای سرعت بالاتر و تاخیر کمتری است.
- **ساده و سبک:** نسبت به TCP دارای سربار کمتر و ساده‌تر است.

#### کاربردها
- **استریمینگ:** ویدیو و صوت
- **بازی‌های آنلاین:** به دلیل نیاز به تاخیر کم و ارسال سریع داده‌ها
- **پروتکل‌های شبکه:** DNS، DHCP
- **ارتباطات زمان واقعی:** VoIP

### TLS (Transport Layer Security)
#### توضیحات کلی
TLS پروتکلی برای ایجاد ارتباطات امن و رمزگذاری شده بین دو سیستم است. این پروتکل در لایه انتقال عمل کرده و نسخه بهبود یافته SSL (Secure Sockets Layer) است.

#### ویژگی‌ها
- **رمزگذاری:** تمامی داده‌های انتقالی بین کلاینت و سرور رمزگذاری می‌شوند تا از دسترسی غیرمجاز جلوگیری شود.
- **احراز هویت:** کلاینت و سرور می‌توانند یکدیگر را با استفاده از گواهینامه‌های دیجیتال (Certificates) احراز هویت کنند.
- **یکپارچگی داده‌ها:** با استفاده از توابع هش (Hash Functions) از تغییر داده‌ها در حین انتقال جلوگیری می‌شود.
- **قابلیت تنظیم:** می‌توان تنظیمات مختلفی را برای الگوریتم‌های رمزگذاری، هش و احراز هویت انتخاب کرد.

#### فرآیند هندشیک TLS
۱. **Client Hello:** کلاینت یک پیام شامل نسخه‌های پشتیبانی شده TLS، الگوریتم‌های رمزنگاری و داده‌های تصادفی ارسال می‌کند.
2. **Server Hello:** سرور با ارسال پیام حاوی انتخاب نسخه TLS، الگوریتم رمزنگاری و داده‌های تصادفی پاسخ می‌دهد.
3. **Certificate:** سرور گواهینامه دیجیتال خود را برای احراز هویت ارسال می‌کند.
4. **Server Key Exchange:** در صورت نیاز، سرور اطلاعاتی را برای تبادل کلید رمزنگاری ارسال می‌کند.
5. **Client Key Exchange:** کلاینت یک کلید رمزنگاری موقت ایجاد و ارسال می‌کند.
6. **Finished Messages:** هر دو طرف پیام‌های نهایی را ارسال کرده و ارتباط امن برقرار می‌شود.

#### کاربردها
- **وبسایت‌های امن:** HTTPS
- **ایمیل امن:** SMTPS، IMAPS، POP3S
- **VPNها:** برای ایجاد تونل‌های امن
- **برنامه‌های انتقال فایل امن:** FTPS، SFTP

### مقایسه TCP، UDP و TLS
- **TCP vs UDP:**
  - **قابلیت اطمینان:** TCP قابل اعتماد است؛ UDP سریع‌تر اما غیرقابل اعتماد.
  - **اتصال:** TCP اتصال‌محور؛ UDP بدون اتصال.
  - **کاربردها:** TCP برای انتقال داده‌هایی که نیاز به اطمینان و ترتیب دارند؛ UDP برای برنامه‌های زمان واقعی و سرعت بالا.

- **TLS:**
  - **امنیت:** برای اضافه کردن لایه امنیتی به پروتکل‌های دیگر مانند HTTP (به HTTPS)، SMTP (به SMTPS) و ...
  - **استفاده:** می‌تواند بر روی هر پروتکل دیگری که در لایه انتقال عمل می‌کند، اعمال شود تا امنیت را فراهم کند.

این توضیحات جامع به شما درک بهتری از نحوه عملکرد TCP، UDP و TLS و کاربردهای آنها در توسعه و مدیریت سیستم‌های شبکه و امنیت می‌دهد.
