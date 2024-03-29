---
title: وحدات دفع طرفية مخصصة ومطالبات لطابعة ودرج الأوراق النقدية
description: يوفر هذا المقال معلومات حول القدرة على تقديم وحدة دفع طرفية مخصصة ومطالبة للمستخدم لتحديد درج الأوراق النقدية وطابعة إيصالات.
author: BrianShook
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7c010448e43bbfb1f949508ce1b62bd07f3107e1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874911"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>وحدات دفع طرفية مخصصة ومطالبات لطابعة ودرج الأوراق النقدية

[!include [banner](includes/banner.md)]

يوفر هذا المقال معلومات حول القدرة على تقديم وحدة دفع طرفية مخصصة ومطالبة للمستخدم لتحديد درج الأوراق النقدية وطابعة إيصالات.

## <a name="overview"></a>نظرة عامة

يبحث بائعو التجزئة العصريون عن طرق لتنظيم تجربة السداد مع الخروج‬ داخل المتجر. لا تساهم الاتجاهات الحديثة التي تعتمد السداد مع الخروج من دون أعمال ورقية عبر الدفعات الإلكترونية في إضفاء السلاسة على تجربة الشراء فحسب بل أيضًا تؤدي إلى تقليل الحاجة إلى وجود عناصر مكمّلة من أجهزة طرفية متوفرة لكل موظف في المتجر.

يدعم Microsoft Dynamics 365 Commerce هذه الاتجاهات من خلال تمكين سيناريو حيث يتضمن جهاز نقطة البيع (POS) وحدة دفع طرفية مخصصة معينة إليه في كل الأوقات، ولكن ليس لديه درج نقدي أو طابعة إيصالات خاصة به. عندما يحتاج موظفو المتجر إلى طباعة إيصال أو استلام دفعة نقدية، تتم مطالبتهم بتحديد محطة أجهزة تم فيها تكوين تلك الأجهزة.

## <a name="key-terms"></a>المصطلحات الأساسية

| المدة | ‏‏الوصف |
|---|---|
| سجل | الكيان المستخدم لتكوين مثيل سجل نقطة البيع. |
| جهاز | تمثيل المثيل الفعلي لسجل نقطة البيع وتطبيق نقطة البيع الحديثة الذي تم تعيينه له. |
| محطة أجهزة مخصصة | منطق عمل محطة الأجهزة المبني في نقطة البيع الحديثة لنظام التشغيل Windows ونقطة البيع الحديثة لتطبيقات Android. |
| منفذ بدء الدرج (d/k) | أسلوب تقليدي لتوصيل درج الأوراق النقدية بطابعة الإيصالات. |
| الأجهزة الطرفية للشبكة | دعم مضمن لمحطات الدفع الطرفية وطابعات الإيصالات وأدراج الأوراق النقدية الممكّنة لاستخدام الشبكة. |

## <a name="supported-pos-clients-and-devices"></a>عملاء وأجهزة نقطة البيع المعتمدة

يتم دعم الوظيفة التي ورد وصفها في هذا المقال من قبل نقطة البيع الحديثة لنظام التشغيل Windows ونقطة البيع الحديثة لعملاء نقطة البيع في Android.

تدعم هذه الوظيفة محطات الدفع الطرفية وطابعات الإيصالات الممكّنة لاستخدام الشبكة.‬ يمكنك توفير دعم درج الأوراق النقدية عن طريق توصيل درج الأوراق النقدية بطابعة الإيصالات الممكّنة لاستخدام الشبكة عبر منفذ d/k.

يتوفر الدعم الجاهز لهذه الوظيفة من قبل [موصل دفع Dynamics 365 لـ Adyen‎](./dev-itpro/adyen-connector.md?tabs=8-1-3). ومع ذلك، قد يتم دعم موصلات دفع أخرى عبر مجموعه تطوير برنامج Commerce (SDK) للدفعات. تتضمن طابعات الإيصالات المدعومة طابعات الإيصالات الممكّنة لاستخدام الشبكة من Star Micronics وEpson.

لإعداد طابعات إيصالات Star Micronics، استخدم الأداة المساعدة Star Micronics Printer لتكوين الجهاز بحيث يمكن استخدامه عبر الشبكة. ستوفر هذه الأداة المساعدة أيضًا عنوان IP الخاص بالجهاز.

لإعداد طابعات إيصالات Epson، استخدم الأداة المساعدة Epson ePOS-Print لإعداد الجهاز لاستخدام بروتوكولات الشبكة.

لمزيد من المعلومات حول كيفية إعداد الأجهزة الطرفية للشبكة، راجع [نظرة عامة حول دعم الأجهزة الطرفية للشبكة](./dev-itpro/network-peripherals.md).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>إعداد وحدة دفع طرفية مخصصة ومطالبة لطابعة ودرج الأوراق النقدية

### <a name="set-up-hardware-profiles"></a>إعداد ملفات تعريف الأجهزة

تحتاج إلى نوعين من أنواع ملفات تعريف الأجهزة. يتم تعيين الأول إلى السجل. ويتم تعيين الثاني إلى محطة الأجهزة على مستوى المتجر، ويُستخدم لتجميع طابعات الإيصالات وأدراج الأوراق النقدية التابعة للشبكة بشكل منطقي.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>إعداد ملف تعريف الأجهزة للسجل

لإعداد ملف تعريف الأجهزة المعين إلى السجل، اتبع الخطوات التالية.

1. في Dynamics 365 Commerce، ابحث عن **ملف تعريف الأجهزة**.
2. حدد **جديد**.
3. قم بتعيين رقم ملف تعريف الأجهزة، وأدخل وصفًا. سيتم تعيين ملف تعريف الأجهزة هذا إلى السجل بحد ذاته. وبالتالي، سيكون إدخال وصف مثل **مخصص مع الاحتياطي** كافيًا.
4. على علامات التبويب السريعة لمختلف أنواع الأجهزة، يمكنك إعداد أنواع الأجهزة التالية.

    | جهاز | النوع | اسم الجهاز | تفاصيل إضافية |
    |---|---|---|---|
    | الطابعة | الشبكة | *أي* | اسم الجهاز حساس لحالة الأحرف. يجب أن يكون **معرف ملف تعريف الإيصال** هو نفسه **معرف ملف تعريف الإيصال** المعيّن إلى طابعة الشبكة التي تم إعدادها في ملف تعريف الأجهزة المعيّن إلى محطة الأجهزة على مستوى القناة. |
    | ‏‏درج الأوراق النقدية | الشبكة | *أي* | اسم الجهاز حساس لحالة الأحرف. عيّن الخيار **استخدام الورديات المشتركة** إلى **نعم**. |
    | خدمة EFT | Adyen | غير قابل للتطبيق | للحصول على معلومات حول كيفية إعداد موصل الدفع Adyen الجاهز، راجع [موصل دفع Dynamics 365 لـ Adyen‬](./dev-itpro/adyen-connector.md?tabs=8-1-3). يمكن دعم موصلات دفع أخرى عبر [مجموعه تطوير برنامج Commerce ‏(SDK) للدفعات](./dev-itpro/end-to-end-payment-extension.md). |
    | لوحة PIN | الشبكة | **MicrosoftAdyenDeviceV001** | بلا. |

5. في Dynamics 365 Commerce، ابحث عن **السجلات**.
6. حدد سجلاً من خلال تحديد رقم السجل، ثم حدد **تحرير**.
7. عيّن ملف تعريف الأجهزة الذ أنشأته للتوّ إلى السجل الذي يجب أن يستخدم محطة دفع طرفية مخصصة. يجب ان يستخدم الجهاز الذي يتم تعيينه إلى هذا السجل إما نقطة البيع الحديثة لنظام التشغيل Windows أو نقطة البيع الحديثة لتطبيق Android.
8. حدد **حفظ**.
9. في جزء الإجراءات، على علامة تبويب **السجلات**، حدد **تكوين عناوين IP‬**.
10. على علامة التبويب السريعة **لوحة PIN**، أدخل عنوان IP لوحدة الدفع الطرفية. للحصول على معلومات حول كيفية الحصول على عنوان IP لوحدة الدفع الطرفية باستخدام موصل Adyen، راجع [موصل دفع Dynamics 365 لـ Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3).
11. حدد **حفظ**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>إعداد ملف تعريف أجهزة لطابعة الإيصالات ودرج الأوراق النقدية

لإعداد ملف تعريف أجهزة يُستخدم لجمع طابعة الإيصالات ودرج الأوراق النقدية على الشبكة، اتبع هذه الخطوات.

1. في Dynamics 365 Commerce، ابحث عن **ملف تعريف الأجهزة**.
2. حدد **جديد**.
3. قم بتعيين رقم ملف تعريف الأجهزة، وأدخل وصفًا. سيتم استخدام ملف تعريف الأجهزة هذا لجمع طابعة الإيصالات ودرج الأوراق النقدية. وبالتالي، سيكون إدخال وصف مثل **طابعة الإيصالات ودرج الأوراق النقدية على الشبكة** كافيًا.
4. على علامات التبويب السريعة لمختلف أنواع الأجهزة، يمكنك إعداد أنواع الأجهزة التالية.

    | جهاز | النوع | ‏‏الوصف | تفاصيل إضافية |
    |---|---|---|---|
    | الطابعة | الشبكة | **Epson** أو **Star** | اسم الجهاز حساس لحالة الأحرف. يجب أن يكون **معرف ملف تعريف الإيصال** هو نفسه **معرف ملف تعريف الإيصال** المعيّن إلى طابعة الشبكة التي تم إعدادها في ملف تعريف الأجهزة المعيّن إلى السجل. |
    | ‏‏درج الأوراق النقدية | احتياطي | **Epson** أو **Star** | اسم الجهاز حساس لحالة الأحرف. عيّن الخيار **استخدام الورديات المشتركة** إلى **نعم**. |

5. حدد **حفظ**.

### <a name="set-up-hardware-stations"></a>إعداد محطات الأجهزة

تحتاج إلى محطتي أجهزة. سيتم تعيين الأولى إلى السجل. وسيتم تحديد الثانية كلما دعت الحاجة إلى طباعة إيصال أو فتح درج الأوراق النقدية.

#### <a name="register-a-hardware-station"></a>تسجيل محطة أجهزة

1. في Dynamics 365 Commerce، ابحث عن **جميع المتاجر**.
2. حدد متجرًا عن طريق تحديد قيم **معرف قناة البيع بالتجزئة**، ثم حدد **تحرير**.
3. على علامة التبويب السريعة **محطات الأجهزة**، حدد **إضافة**.
4. عيّن حقل **نوع محطة الأجهزة** إلى **مخصص**.
5. ادخل وصفًا، ولكن دون تعيين أي قيم أخرى لمحطة الأجهزة هذه. سيتم استخدام محطة الأجهزة هذه للتسجيل في كافة الأوقات. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>إعداد مخطة أجهزة لطابعة الإيصالات ودرج الأوراق النقدية

1. في Dynamics 365 Commerce، ابحث عن **جميع المتاجر**.
2. حدد متجرًا عن طريق تحديد قيم **معرف قناة البيع بالتجزئة**، ثم حدد **تحرير**.
3. على علامة التبويب السريعة **محطات الأجهزة**، حدد **إضافة**.
4. عيّن حقل **نوع محطة الأجهزة** إلى **مخصص**.
5. أدخل وصفًا. سيتم استخدام محطة الأجهزة هذا لطابعة الإيصالات ودرج الأوراق النقدية.
6. في الحقل **ملف تعريف الأجهزة**، حدد ملف تعريف الأجهزة‏‎‎‏ الذي أنشأته في وقت سابق لطابعة الإيصالات ودرج الأوراق النقدية.
7. حدد **حفظ**.
8. مع استمرار تحديد محطة الاجهزة لطابعة الإيصالات ودرج الأوراق النقدية،، حدد **تكوين عناوين IP**.
9. احصل على عنوان IP للطابعة، وأدخله كعنوان IP لطابعة الإيصالات ودرج الأوراق النقدية.
10. حدد **حفظ**.
11. ابحث عن **جداول التوزيع**.
12. حدد جدول التوزيع **1090**، ثم حدد **تشغيل الآن**.
13. حدد جدول التوزيع **1070**، ثم حدد **تشغيل الآن**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>إعداد النظام للمطالبة بتحديد طابعة الإيصالات ودرج الأوراق النقدية كما هو مطلوب

1. في عميل نقطة بيع مدعوم، قم بإغلاق الوردية الحالية، إذا كانت هناك وردية مفتوحة.
2. سجل الدخول، ثم حدد **عمليات غير مرتبطة بالدرج‬‬‏‫**.
3. استخدم عملية **إدارة محطات الأجهزة** لتشغيل محطة أجهزة.
4. حدد محطة الأجهزة التي أنشأتها للسجل لجعله نشطًا.
5. سجل خروجك من نقطة البيع، ثم سجل دخولك مرة أخرى وافتح وردية.

ستكون الآن محطة الدفع الطرفية التي تم تعيينها إلى ملف تعريف الأجهزة نشطة دائمًا، وسيتم سؤالك إن كنت بحاجة إلى طابعة إيصالات أو درج أوراق نقدية.

يهتم عدد كبير من التجار ممن طلبوا هذه الميزة بتقليل الفاقد من خلال توفير الإيصالات بالبريد الإلكتروني والتشجيع على الدفع الإلكتروني. استنادًا إلى تكوين نقطة البيع، تتم مطالبة موظفي المتجر باختيار طابعة إيصالات أو درج أوراق نقدية فقط عندما يريد العميل الحصول على إيصال مادي أو عندما يريد الدفع نقدًا.

تتم مطالبة موظفي المتجر باختيار محطة أجهزة مرة واحدة فقط لكل حركة، إلا إذا كان من الضروري طباعة إيصال وتم استخدام مبلغ نقدي لتسديد الدفع، ولكن ملف تعريف الأجهزة هذا الذي تم اختياره في الأصل لا يتضمن الجهازين. وفي هذه الحالة، ستتم مطالبة موظف المتجر من جديد بتحديد محطة أجهزة يمكن استخدامها لإكمال الحركة.

## <a name="related-articles"></a>مقالات ذات صلة

- [إعداد تطبيق POS Hybrid في Android وiOS](./dev-itpro/hybridapp.md)
- [موصل دفع Dynamics 365 لـ Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)
- [نظرة عامة حول دعم الأجهزة الطرفية للشبكة‬](./dev-itpro/network-peripherals.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
