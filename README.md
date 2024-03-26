<p align="center">
  <a href="https://github.com/WhyMan1/marzban-singbox-template/tree/master/singbox" target="_blank" rel="noopener noreferrer">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://sing-box.sagernet.org/assets/icon.svg">
      <img width="160" height="160" src="https://sing-box.sagernet.org/assets/icon.svg">
    </picture>
  </a>
</p>
<h1 align="center"/>sing-box config example for <a href="https://github.com/Gozargah/Marzban">Marzban</a></h1>

## فهرست مطالب
- [مقدمه](#مقدمه)
- [ویژگی‌ ها](#ویژگی-ها)
- [مراحل نصب](#مراحل-نصب)
- [لینک دانلود sing-box](#لینک-دانلود-sing-box)

# مقدمه
سینگ باکس یک پروکسی مبتنی بر قوانین است که به شما این امکان را می‌دهد که تنظیمات مربوط به برنامه از قبیل DNS و مسیریابی و ... را از سمت سرور انجام دهید. در این template از سمت سرور، سینگ باکس  را به گونه‌ای تنظیم شده است که اتصال به سایت‌های ایرانی به صورت مستقیم انجام شود.
از مهم ترین ویژگی کلاینت sing-box پشتیبانی از پلتفرم های مختلف مانند اندروید، iOS، macOS و ... می باشد.

# ویژگی ها
- وصل شدن به سریع ترین کانفیگ
- وصل شدن مستقیم به وب‌سایت‌های ایرانی هنگامی که فیلترشکن روشن است
- بلاک کردن تبلیغات
و ...

# مراحل نصب
1. دانلود فایل template
```sh
sudo wget -N -P /var/lib/marzban/templates/singbox/ https://raw.githubusercontent.com/nasiriscript/marzban-singbox-template/master/singbox/default.json
sudo wget -N -P /var/lib/marzban/templates/singbox/ https://raw.githubusercontent.com/nasiriscript/marzban-singbox-template/master/singbox/mux_conf.json
```
2. دستورات زیر رو تو ترمینال سرورتون بزنید:
```sh
sudo nano /opt/marzban/.env
```
و مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` قرار بدین
```sh
CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
SINGBOX_SUBSCRIPTION_TEMPLATE="singbox/default.json"
SINGBOX_MUX_CONFIGURATION = "singbox/mux_conf.json"
```

3. ری استارت مرزبان
```sh
marzban restart
```

## بروزرسانی
برای بروزرسانی تمپلیت فقط کافیست مرحله ۱ را تکرار کنید.

# لینک دانلود sing-box
- Android:
   - [SFA AppCenter](https://install.appcenter.ms/users/nekohasekai/apps/sfa/distribution_groups/publictest)
   - [SFA Github](https://github.com/SagerNet/sing-box/releases)
   - [SFA Google Play](https://play.google.com/store/apps/details?id=io.nekohasekai.sfa)
- iOS:
  - [SFI](https://apps.apple.com/us/app/sing-box/id6451272673)
- macOS：
  - [SFM](https://apps.apple.com/us/app/sing-box/id6451272673)

# حمایت از من

<a href="https://nowpayments.io/donation?api_key=WE3KFT5-2VKMNSF-N1P4YQ6-24N82ZA&source=lk_donation&medium=referral" target="_blank">
  <img src="https://nowpayments.io/images/embeds/donation-button-black.svg" alt="Crypto donation button by NOWPayments">
</a>
