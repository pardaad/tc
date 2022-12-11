# راهنمای API وب‌سایت TRADERSCOMBAT

## بخش اول - بروزرسانی اطلاعات حساب معامله‌گران

### پارامترها

مقدار APIkey خود را در Header درخواست به API ارسال کنید و سایر پارامترهای زیر را در Body درخواست ارسال کنید.

نکته ۱: برای امنیت اطلاعات می‌توانید اطلاعات را به صورت encode شده ارسال کنید.

نکته ۲: ارسال مقدار accountNumber الزامی است ولی سایر موارد اختیاری هستند.

<table dir="rtl" align="center">
<tr><th>نام پارامتر</th><th>فرمت مقدار</th><th>توضیحات</th></tr>
<tr><td>accountNumber</td><td>number</td><td>اکانت نامبر</td></tr>
<tr><td>startChalenge</td><td>Datetime Y-m-d H:i:s</td><td>تاریخ شروع چلنج</td></tr>
<tr><td>initialBalance</td><td>number</td><td>بالانس اولیه حساب</td></tr>
<tr><td>currentBalance</td><td>number</td><td>بالانس فعلی حساب</td></tr>
<tr><td>todayBalance</td><td>number</td><td>بالای ابتدای روز حساب</td></tr>
<tr><td>accountEquity</td><td>number</td><td>اکوییتی حساب</td></tr>
<tr><td>floatingProfitLoss</td><td>number</td><td>عدد سود یا ضرر فعلی حساب</td></tr>
<tr><td>todayProfit</td><td>number</td><td>سود یا ضرر امروز حساب که داخل بالانس نشسته</td></tr>
<tr><td>profitAverage</td><td>number</td><td>میانگین عددی سود معاملات</td></tr>
<tr><td>lossAverage</td><td>number</td><td>میانگین عددی ضرر معاملات</td></tr>
<tr><td>winRate</td><td>number</td><td>وین ریت معاملات</td></tr>
<tr><td>daysOfTrades</td><td>number</td><td>تعداد روز معاملاتی</td></tr>
<tr><td>currentTodayDrawdown</td><td>number</td><td>دراداون فعلی روزانه حساب</td></tr>
<tr><td>currentInitialDrawdown</td><td>number</td><td>دراداون فعلی کلی حساب</td></tr>
<tr><td>maxTodayDrawdown</td><td>number</td><td>ماکزیمم دراداون روزانه</td></tr>
<tr><td>maxInitialDrawdown</td><td>number</td><td>ماکزیمم دراداون کلی حساب</td></tr>
</table>

### پاسخ‌های دریافتی از API

<table dir="rtl" align="center">
<tr><th>کد دریافتی</th><th>توضیحات</th><th>Status</th></tr>
<tr><td>0</td><td>مقدار ApiKey وارد نشده یا اشتباه است</td><td>403</td></tr>
<tr><td>1</td><td>عملیات بروزرسانی اطلاعات با موفقیت انجام شد</td><td>201</td></tr>
<tr><td>2</td><td>مقدار accountNumber ارسال نشده است</td><td>400</td></tr>
<tr><td>3</td><td>مقدار accountNumber در وب‌سایت برای هیچ کاربری ثبت نشده است یا اشتباه است</td><td>400</td></tr>
<tr><td>4</td><td>یکی از مقادیر ارسالی با فرمت اشتباه ارسال شده است، پارامترهایی که مقادیر آنها با فرمت اشتباه ارسال می‌شوند به صورت یک آرایه در پاسخ به درخواست ارسال می‌شوند.</td><td>400</td></tr>
</table>
