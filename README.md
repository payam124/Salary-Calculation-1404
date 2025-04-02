# Salary-Calculation-1404
محاسبات حقوق و مالیات و بیمه 1404

# Salary and Tax Calculation (1404 Iran)

# اکسل محاسبه افزایش حقوق و کسورات بیمه و مالیات دستمزد در سال 1404

## لینک دانلود

https://github.com/payam124/Salary-Calculation-1404/releases/tag/v0.9


## مقدمه

یکی از مسایلی که اغلب بین کارفرما و کارمندان چالش ایجاد می‌کند، مسال حقوق دستمزد و کسورات آن است. شاید این مسیر برای خیلی از کارمندان و کارآفرینان و صاحبان کسب و کار آشنا باشد: در ابتدای راه، یک پرداختی‌ای انجام می‌دهند. بعد کم کم متوجه بیمه تامین اجتماعی و الزامات آن می‌شوند (البته احتمالا در سالهای اخیر اغلب آگاه هستند). بعد یک حقوق پایه و بیمه و مالیات رد می‌شود و ما بقی حقوق به شکل‌های غیر رسمی پرداخت می‌شود. کم کم پی بازرس بیمه و مالیات به شرکت می‌خورد و به مرور تمامی پرداختی‌های پرسنل به طور رسمی و پس از کسر کسورات بیمه و مالیات پرداخت می‌شود.

در این مسیر اما آنچه مهم است این است که کارمندان با پولی که در پایان ماه در حسابشان دریافت می‌کنند زندگی می‌کنند. برای همین اغلب از سمت پرسنل تمایل به توافق بر روی یک عدد ثابت خالص است در صورتیکه از سمت کارفرما و مخصوصا تیم‌های مالی تمایل به عقد قرارداد به صورت ناخالص است.

موضوع بیمه و مخصوصا مالیات از جمله مسایلی هستند که فرمول محاسباتی آنها خیلی سرراست نیست تابع خیلی متغیرها هست. حتی با ثابت کردن بسیاری از آنها،‌ باز هم اینقدر فرمول ساده‌این نمی‌شود که در اکسل با چند تا جمع و تفریق و ضرب و تقسیم به دست بیاید. 

همین مساله یکی پاشه آشیل‌های سست شدن دیوار اعتماد بین کارفرما و کارمندان است. کارفرما نمی‌تواند به سادگی تعهد دریافتی ثابت و مشخص را به کارمند بدهد، کارمند نیز در اثر فراز و نشیب‌های کسورات اغلب کلنگ بدبینی‌اش غلبه می‌کند و بر پیکیر دیوار اعتماد نواخته می‌شود. حالا خدا نکند که کارفرما سهوا یکبار هم اشتباه بکند. دیگر واویلا می‌شود.

این اکسل به قصد کمک به مدیران و کارمندانی ایجاد شده‌است که به دنبال شفافیت هستند. تلاش شده‌است بر اساس اصولی که در محاسبیه حقوق و دستمزد وجود دارد ساختاری ایجاد کند که بتوان تخمینی از حقوق و دستمزد و کسورات یک فرد در طول سال داشت و در صورت وقوع اختلاف فاحش بتواند آن‌را ریشه یابی کرد.

## دلایل پیچیده بودن محاسبات

- مالیات پلکانی است. تا یک عددی، هیچ مالیاتی وجود ندارد، از یک عددی به بالا، هرچه درآمد بیشتر شود،‌ به مازاد درامد، مالیات بیشتری تعلق می‌گیرد.
- مالیات و معافیت‌های آن موضوع “سالانه” است. یعنی قرار است کل حقوق مزایای شما در طول یکسال معیار قرار بگیرد و در تعرفه‌های پلکانی مالیاتی برود و بعد از در نظر گرفتن معافیت‌ها، مالیات محاسبه شود. اما دریافتی‌های افراد ماهانه هست. در فرمول‌های ارایه شده در سیستم‌های مالی تلاش می‌شود که اگر کسی حقوق ثابتی در طول سال دارد، مالیات ثابتی هم در طول سال از او کسر شود. اما مشخصا مسایلی مثل پاداش، اضافه کار و …، می‌تواند این نظم را به هم بزند. (البته در نهایت باید وقتی کل سال در نظر گرفته می‌شود، همه چیز درست باشد. فقط بحث تقدم و تاخر کسر مالیات وجود خواهد داشت)
- تفاوت ماه 31 روزه، 30 روزه و 29 روزه. بر خلاف تصور رایج، شما روی حقوق ماهانه توافق نمی‌کنید. در سیستم‌های اصولی، شما روی حقور “روزانه” یا ماه بر مبنای 30 روز حقوق تفاوت می‌کنید. البته ممکن است برخی شرکت‌ها هم مثلا اگر وعده حقوق ماهانه X را داده باشند،‌ مبنای سال را 12X می‌گذارند و سپس تقسیم بر 365 (یا 366) روز می‌کنند و بعد حقوق ماهانه را محاسبه می‌کنند. توجه داشته باشید که شما در ایران برای تمام روزهای ماه حقوق می‌گیرید. چه تعطیل، چه غیر تعطیل. همین مساله 29 الی 31 روز می‌تواند تا 6 درصد تفاوت بین حقوق دو ماه (و مالیات و کسورات متعلقه) ایجاد کند.
- فرمول‌های اعمال مالیات برای دریافتی‌های یکباره (مزایای غیر مستمر) مانند پاداش، اضافه کاری با دریافتی‌های مستمر متفاوت است. نه اینکه در نتیجه یکسال تفاوت داشته باشد. ولی قانونگذار اینگونه فرض می‌کند که اگر مثلا شما در ماه 1  یک پاداش 100 میلیون می‌گیرید، قرار نیست هر ماه 100 میلیون پاداش بگیرید. در نتیجه فرض می‌کند این 100 میلیون یک مزیت “غیر مستمر” است و سعی می‌کند به نحوی به آن نگاه کند که انگار این 100 میلیون را شما در طول 12 ماه می‌گیرید و مالیات آن را سر کشن می‌کند و نرم‌افزارها به نحوی عمل می‌کنند که این مالیات در طول ماه‌های مختلف پرداخت شود. در صورتیکه اگر قرار باشد شما به صورت ثابت از ماه 1 هر ماه 100 میلیون پاداش بگیرید (مزایای مستمر) نرم‌افزارهای محاسبه حقوق و دستمزد، این را در نظر می‌گیرند و به نحوی مالیات از شما کسر می‌کنند که یک دفعه این 100 میلیون‌ها همه برای ماه آخر نمانند. حالا تصور کنید که یک شرکتی در قالب مزایای غیر مستمر، هر ماه به شما 100 میلیون پاداش بدهد! ماه اول شما خیلی خوشحال هستید. چون مالیات کمی از شما کم می‌شود. اما وقتی به آخر سال می‌رسید، هر ماه میزان مالیات شما بیشتر می‌شود. در نهایت شما مالیات بیشتری نمی‌دهید. همانقدر که باید بدهید می‌دهید. ولی اول سال چون سیستم فکر می‌کرده شما فقط قرار است یکبار این پاداش را بگیرید، همه معافیت‌ها و براکت‌های پایین مالیات را برای آن استفاده کرده و شما دچار یک خوشخیالی کاذب شدید.
- اخیرا اداره مالیات بحث تجمیع درامد را هم پیش کشیده است. یعنی اگر شما از دو جا حقوق می‌گیرید، حقوق هر دو جا تجمیع می‌شود و در نرخ پلکانی می‌رود و توجه باید داشته باشید که شما تنها یک معافیت مالیاتی در سال دارید. این هم نکته مهمی است که برای برخی مشکل و ابهام ایجاد خواهد کرد.
    - همین موضوع یکی از دلایلی مهمی است که به نظر من توافق سر حقوق خالص را تقریبا بی معنی می‌کند مگر اینکه کارفرما راضی باشد بی برو برگرد، حدود 37 + 23 درصد بیشتر بپردازد. چرا؟ فرض کنید کارمند در جای دیگری کار می‌کند. آنجا ممکن است 1 میلیون تومان در ماه حقوق بگیرد. یا 100 میلیون تومان در ماه. در حالت اول، حتی هنوز مقداری معافیت مالیاتی دارد. در حالت دوم، تمام معافیت مالیاتی و پله‌های 10، 15، 20 و 25 درصد مالیات را مصرف کرده و در پله 30 درصد است. تازه هزینه 30 درصد بیمه هم هست که 7 درصد سهم کارمند و 23 درصد سهم کارفرما است. خلاصه اینگونه است که همه چیز پیچیده می‌شود. کارفرما اگر به دو نیروی مشابه بخواهد پرداختی خالص 50 میلیون تومان را وعده بدهد، یکی برایش

## شیوه استفاده از فایل اکسل

- شما می‌توانید در خانه‌های سبزرنگ اطلاعات خودتان را وارد کنید و فایل حقوق و مزایای و کسورات احتمالی ماهانه شما را محاسبه کند
- شما می‌توانید برای ماه 30 روزه و 31 روزه و 29 روزه محاسبات را انجام دهید.
- اطلاعات پایه برای محاسبات در کاربرگ “اطلاعات پایه” قرار داده شده‌است.

## منطق‌های کلی استفاده شده

- مبنای اصلی بر حقوق 30 روزه و سال 365 روزه لحاظ شده است.
- فرض شده است که دریافتی‌های شما در طول سال یکنواخت است. لذا اگر شما برای خود اضافه کاری معادل 50 ساعت لحاظ می‌کنید، فرض این سیستم این است که هر ماه قرار است 50 ساعت اضافه کار داشته باشید
- حقوق و دستمزد مشمول مالیات، جمع کل مزایای منهای دو هفتم بیمه پرداختی است. این موضوع بر اساس ماده 137 قانون مالیات‌های مستقیم و بند ۲ بخشنامه 4385/211/19418 مورخ 1383/11/07 سازمان امور مالیاتی است. این موضوع اغلب از نگاه افرادی که می‌خواهند خود سهم مالیات را حساب کنند به دور می‌ماند
- بیمه تامین اجتماعی سقف دارد. حداکثر میزانی حق بیمه معادل بیمه 7 برابر حقوق پایه است و اگر حقوق شما بیشتر از آن باشه، دیگر از شما بیمه کسر نخواهد شد.

## مجوز استفاده

- این فایل تحت لیسانس GPL 3.0 منتشر می‌شود.
- لطفا در انتشار به مرجع آن  https://github.com/payam124/Salary-Calculation-1404  ارجاع دهید
- استفاده تجاری بدون کسب اجازه مجاز نیست
- برای گزارش مشکلات از طریق باز کردن Issue‌ در GitHub‌ اقدام کنید.


# Excel Sheet for Calculating Salary Increases and Deductions for the Year 1404 (2025)

## Download Link

https://github.com/payam124/Salary-Calculation-1404/releases/tag/v0.9

## Introduction

One of the most common points of tension between employers and employees is the matter of salary payments and related deductions. Many employees, entrepreneurs, and business owners are familiar with the following journey: Initially, salaries are paid with little formal structure. Gradually, they learn about social security insurance and its requirements (though most people are already aware of these in recent years). Eventually, a base salary is declared, insurance and tax deductions are applied, and the remaining amount is often paid informally. Then comes the insurance or tax inspector’s visit, and over time, all payments must be formalized, with proper deductions applied.

What truly matters along this path is that employees live based on the **net salary** they receive at the end of the month. That’s why employees usually prefer to agree on a fixed **net** amount, while employers—especially finance teams—prefer to define **gross** salary contracts.

Insurance and tax calculations are complex and depend on many variables. Even after fixing most of those variables, the formula isn't simple enough to be calculated with basic addition, subtraction, multiplication, or division in Excel.

This complexity can undermine the trust between employer and employee. Employers can’t easily guarantee a fixed, clear take-home amount. Meanwhile, employees may grow skeptical and lose trust due to fluctuations in deductions—especially if there's ever an unintentional error on the employer’s side.

This Excel sheet is designed to help managers and employees who seek transparency. It tries to model the actual rules around salary, insurance, and tax calculations in a way that makes it easier to estimate monthly deductions and identify the cause of any large discrepancies.

## Why Salary Calculations Are Complex

- **Taxes are progressive**: There's no tax on income below a certain threshold. As income increases, higher tax rates apply to the excess amount.
- **Tax exemptions are based on annual income**: While salaries are paid monthly, tax brackets and exemptions are calculated annually. Financial systems try to evenly distribute annual tax over monthly payments, assuming a stable income. However, bonuses and overtime disrupt this pattern. (Eventually, everything balances out over the year, but early months may have low tax deductions that increase later.)
- **Months have different lengths (29, 30, or 31 days)**: Contrary to popular belief, salary agreements are often based on a **daily** rate or a 30-day month. Some companies instead base salaries on a fixed annual amount (e.g., 12 × monthly salary divided by 365), meaning that month length can cause up to a **6%** difference in pay and deductions.
- **Different rules apply to one-time vs. recurring payments**: For example, a one-time bonus of 100 million Toman in Month 1 is taxed under the assumption that this is not a recurring benefit. So tax is calculated as if this amount is distributed over 12 months. If that same bonus continues monthly, payroll software eventually adjusts the tax accordingly. Initially, this can cause **false optimism** about take-home pay, followed by disappointment as tax deductions increase.
- **Income aggregation rule**: Recently, tax authorities have enforced a rule that combines income from multiple employers to determine the tax bracket. Each person only gets one annual tax exemption. This can create significant confusion and higher tax for those with multiple jobs.
    - Because of this, agreeing on a fixed **net** salary can be meaningless unless the employer is willing to **consistently** cover roughly **37% + 23%** extra. Why? Suppose the employee earns 1 million at another job, or 100 million. In the first case, they still have some tax exemption left. In the second, their exemption is already used up, and they’re in the highest tax bracket. Add the 30% insurance cost (7% from the employee, 23% from the employer), and things get very complex. If two employees are promised a net salary of 50 million, the gross cost for the employer could vary significantly.

## How to Use the Excel Sheet

- Fill in the green cells with your information to calculate your monthly salary, benefits, and deductions.
- The file supports calculations for 29-day, 30-day, and 31-day months.
- Base data used in calculations can be found in the **"Base Info"** worksheet.

## General Assumptions

- Calculations assume a 30-day salary month and a 365-day year.
- It is assumed that your income is consistent throughout the year. For instance, if you enter 50 hours of overtime, the sheet assumes you’ll work 50 hours of overtime every month.
- **Taxable salary** is calculated as total benefits minus **2/7 of your insurance contribution**, based on Article 137 of the Direct Tax Code and clause 2 of circular 4385/211/19418 dated 2005-01-27 from the Tax Authority. This is often overlooked when individuals try to calculate their own taxes.
- **Social security insurance has a cap**: It is only deducted from salaries up to **7× the base wage**. Any income beyond that is not subject to further insurance deductions.

## License

- This file is released under the **GPL 3.0** license.
- Please credit the original source: https://github.com/payam124/Salary-Calculation-1404
- **Commercial use is not allowed** without permission.
- To report issues, please open an **Issue** on GitHub.