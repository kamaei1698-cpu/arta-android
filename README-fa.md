# Arta Android Native

نسخه Android بومی برای اجرای Arta آفلاین.

## قابلیت‌ها
- اجرای آفلاین فایل اصلی Arta داخل WebView امن
- IndexedDB و DOM Storage برای نگهداری دائمی داده‌های Arta
- انتخاب فایل از Android و پشتیبانی از input file
- درخواست دسترسی دوربین برای فیلدهای capture
- ذخیره فایل‌های تولیدشده Blob در Downloads/Arta از طریق MediaStore
- اشتراک‌گذاری متن از طریق Android Share Sheet
- RTL و رابط فارسی
- بدون دسترسی اینترنت در Manifest

## Build
در Android Studio پروژه را باز کنید و Gradle Sync سپس Build > Build APKs را بزنید.

> این محیط Android SDK/Gradle Wrapper آماده ندارد؛ بنابراین APK باینری در این محیط کامپایل نشده است.

## ساخت APK بدون نصب Android Studio (با GitHub Actions)

این پروژه فایل Workflow دارد تا GitHub بتواند APK آزمایشی را بسازد:

1. در GitHub یک مخزن جدید بسازید.
2. محتویات پوشه `ArtaAndroidNative` را در مخزن بارگذاری کنید؛ ZIP را ابتدا Extract کنید.
3. وارد زبانه **Actions** شوید و Workflow با نام **Build Arta Android APK** را انتخاب کنید.
4. روی **Run workflow** بزنید.
5. پس از سبز شدن اجرای Build، از بخش **Artifacts** فایل `Arta-Android-debug-APK` را دانلود کنید.
6. ZIP دریافت‌شده را باز کنید؛ فایل `app-debug.apk` داخل آن است.

این خروجی Debug برای نصب و آزمایش است؛ برای انتشار عمومی باید نسخه Release را با کلید امضای اختصاصی امضا کرد.
