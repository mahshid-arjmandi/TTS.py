# TTS.py
با اجرا کردن این دو فایل
۱.متن به هر زبانی داده شود به زبان فارسی صدا شنیده خواهد شد.(چون گفتار سیستم پیش فرض فارسی هست)

مثال:
-متن: Bonjour
صدایی که می شنوید :
سلام

۲.متن به زبان فارسی داده شود و کاربر نوع زبان گفتار را انتخاب کند متن به زبان گفتار مدنظر کاربر شنیده میشه 
مثال: 
متن -سلام 
کاربر تمایل دارد پاسخش به فرانسه شنیده بشه در نتیجه Bonjour پخش میشه.



۳.
متن به هر زبانی داده شود و کاربر نوع زبان گفتار را انتخاب کند متن به زبان گفتار مدنظر کاربر شنیده می شود .
مثال :فرض کنید کاربر متن به زبان فرانسه وارد کرده و تمایل دارد پاسخش به زبان انگلیسی باشد.
-متن: Bonjour
صدایی که می شنوید: Hello
۴‌.متن به هر زبانی داده شود و کاربر نوع زبان گفتار را انتخاب نکند یا اشتباه انتخاب کند متن به زبان فارسی شنیده می شود.
مثال
متن-hello

کاربر نوع زبان گفتار را اشتباه انتخاب کرده 
صدایی که پخش می شود: سلام

@sasankolahi

لازم است فایل های زیر
main.py

textToSpeech.py

playing_anonymized_sound.py

audio_conversion.py

audio_anonymization.py

anonymize_voice_Main.py

voice_processing(1).py



در یک پوشه ذخیره شوند در ادامه لازم هست فایل ها به ترتیب 
در محیط pycharm ،اجرا شوند .
main.py

textToSpeech.py

playing_anonymized_sound.py

audio_conversion.py

audio_anonymization.py

anonymize_voice_Main.py

voice_processing(1).py



در یک پوشه ذخیره شوند در ادامه لازم هست فایل ها به ترتیب 
در محیط pycharm ،اجرا شوند .

برای استفاده لطفا مرحله ها رو کامل انجام بدید 
1. مراجعه به لینک ذکر شده و دانلود فایل زیپ ffmpeg 

https://github.com/BtbN/FFmpeg-Builds/releases/download/latest/ffmpeg-n7.1-latest-win64-lgpl-7.1.zip

2.بعد از دانلود و استخراج فایل ZIP ffmpeg، مراحل زیر را دنبال کنید: 
آ) استخراج فایل ZIP 
فایل ZIP را باز کنید و تمام محتویات آن را در یک پوشه مشخص (مثلاً C:\ffmpeg) استخراج کنید.


ب) تنظیم PATH در ویندوز 
برای این که ویندوز بتواند ffmpeg را شناسایی کند، باید مسیر آن را به متغیر محیطی PATH اضافه کنید: 

پ) پنجره تنظیمات سیستم را باز کنید: 
روی دکمه Start کلیک کنید، سپس Control Panel را جستجو کنید و باز کنید. 
یا می‌توانید روی دکمه Windows کلیک راست کنید و System را انتخاب کنید.

ت) بر روی "Advanced system settings" کلیک کنید: 
در سمت چپ پنجره، گزینه Advanced system settings را انتخاب کنید.

س)روی دکمه "Environment Variables" کلیک کنید: 
در بخش System Properties، دکمه Environment Variables را بزنید.

ش) متغیر Path را ویرایش کنید: 
در بخش System variables، متغیر Path را پیدا کنید و روی آن دوبار کلیک کنید یا Edit را بزنید. 
سپس New را بزنید و مسیر پوشه bin را که داخل پوشه ffmpeg قرار دارد، وارد کنید. مثلاً: 
C:\ffmpeg\bin

ص) تغییرات را ذخیره کنید: 
روی OK کلیک کنید تا تمام پنجره‌ها بسته شوند.


بررسی نصب 
برای اطمینان از این که ffmpeg به درستی نصب شده است، مراحل زیر را انجام دهید: 
1. Command Prompt را باز کنید: 
روی دکمه Start کلیک کنید و cmd را جستجو کنید و باز کنید.

2. دستور زیر را وارد کنید: 
ffmpeg -version 
اگر نصب به درستی انجام شده باشد، اطلاعات نسخه ffmpeg نمایش داده می‌شود.
1. مراجعه به لینک ذکر شده و دانلود فایل زیپ ffmpeg 

https://github.com/BtbN/FFmpeg-Builds/releases/download/latest/ffmpeg-n7.1-latest-win64-lgpl-7.1.zip

2.بعد از دانلود و استخراج فایل ZIP ffmpeg، مراحل زیر را دنبال کنید: 
آ) استخراج فایل ZIP 
فایل ZIP را باز کنید و تمام محتویات آن را در یک پوشه مشخص (مثلاً C:\ffmpeg) استخراج کنید.


ب) تنظیم PATH در ویندوز 
برای این که ویندوز بتواند ffmpeg را شناسایی کند، باید مسیر آن را به متغیر محیطی PATH اضافه کنید: 

پ) پنجره تنظیمات سیستم را باز کنید: 
روی دکمه Start کلیک کنید، سپس Control Panel را جستجو کنید و باز کنید. 
یا می‌توانید روی دکمه Windows کلیک راست کنید و System را انتخاب کنید.

ت) بر روی "Advanced system settings" کلیک کنید: 
در سمت چپ پنجره، گزینه Advanced system settings را انتخاب کنید.

س)روی دکمه "Environment Variables" کلیک کنید: 
در بخش System Properties، دکمه Environment Variables را بزنید.

ش) متغیر Path را ویرایش کنید: 
در بخش System variables، متغیر Path را پیدا کنید و روی آن دوبار کلیک کنید یا Edit را بزنید. 
سپس New را بزنید و مسیر پوشه bin را که داخل پوشه ffmpeg قرار دارد، وارد کنید. مثلاً: 
C:\ffmpeg\bin

ص) تغییرات را ذخیره کنید: 
روی OK کلیک کنید تا تمام پنجره‌ها بسته شوند.


بررسی نصب 
برای اطمینان از این که ffmpeg به درستی نصب شده است، مراحل زیر را انجام دهید: 
1. Command Prompt را باز کنید: 
روی دکمه Start کلیک کنید و cmd را جستجو کنید و باز کنید.

2. دستور زیر را وارد کنید: 
ffmpeg -version 
اگر نصب به درستی انجام شده باشد، اطلاعات نسخه ffmpeg نمایش داده می‌شود.
راهنمای استفاده از کد main.py:

1. بعد از اینکه تمامی فایل های مربوط به مدل ترجمه را دانلود کردید .


2. تنظیم مسیر مدل: بعد از دانلود، مدل را در یک پوشه مشخص ذخیره کنید. سپس، مسیر این پوشه را پیدا کرده و آن را در قسمت model_path کد قرار دهید.

برای مثال راهنمای استفاده از کد main.py:

1. بعد از اینکه  تمامی فایل های مربوط به مدل ترجمه را دانلود کردید .


2. تنظیم مسیر مدل: بعد از دانلود، مدل را در یک پوشه مشخص ذخیره کنید. سپس، مسیر این پوشه را پیدا کرده و آن را در قسمت model_path کد قرار دهید.

برای مثال این 

model_path = r"E:\University\master\mbaheseVijeh\project_AI\Translate_\Translate_Models\models"

مسیری هست که من مدل رو در سیستمم ذخیره کردم.
بعد از اینکه ffmpeg با موفقیت نصب شد .

وارد pycharm 
بشین
از نوار بالا بر روی view کلیک کرده Tool Windows رو انتخاب کنید و بر روی گزینه Terminal کلیک کنید در ترمینال دستورات رو یکی یکی اجرا کنید

1.pip install edge_tts

2. pip install pydub

3. pip install --upgrade

4.pip install ffmpeg_python

5. pip install nest_asyncio

6. pip install pygame

🚫🚫7.pip install langdetect
🚫🚫8.pip install transformers 
🚫🚫9.pip install torch
🚫🚫10.pip install sentencepiece

