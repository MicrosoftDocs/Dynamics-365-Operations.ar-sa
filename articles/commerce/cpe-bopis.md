---
title: تكوين BOPIS (الشراء عبر الإنترنت والاستلام في المتجر) في بيئة تقييم Dynamics 365 Commerce
description: يوضح هذا المقال كيف تكون الشراء عبر الإنترنت والانتقاء في المتجر (BOPIS) في بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.
author: BrianShook
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 379537fd490be98497b6e7c5cdfbc33798fe28ad
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861956"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-evaluation-environment"></a>تكوين BOPIS (الشراء عبر الإنترنت والاستلام في المتجر) في بيئة تقييم Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

يوضح هذا المقال كيفية تكوين الشراء عبر الإنترنت والانتقاء في المتجر (BOPIS) في بيئة تقييم Microsoft Dynamics 365 Commerce بعد توفيرها.

## <a name="prerequisite"></a>المتطلب الأساسي

استكمل الإجراءات في هذا المقال فقط بعد توفير بيئة تقييم Commerce وتكوينها. لمزيد من المعلومات حول توفير وتكوين البيئة الخاصة بك، راجع [توفير بيئة تقييم Dynamics 365 Commerce](provisioning-guide.md) و[تكوين بيئة تقييم Dynamics 365 Commerce](./cpe-post-provisioning.md).

بعد توفير بيئة معاينة Commerce وتكوينها من البداية إلى النهائية، يمكنك استخدام هذا المقال لتكوين سيناريوهات BOPIS.

## <a name="configure-the-pos"></a>تكوين نقطة البيع (POS)

### <a name="configure-modern-pos"></a>تكوين Modern POS

تحتاج سيناريوهات BOPIS التي تتضمن الدفع ببطاقة ائتمان إلى محطة أجهزة. ويتم دمج محطة الأجهزة في Modern POS لعملاء Windows وAndroid. إذا كنت تستخدم Cloud POS أو Modern POS لـ iOS، فيجب إقران عميل نقطة البيع (POS) مع محطة أجهزة مشتركة. يشرح هذا المقال كيفية تكوين BOPIS لعملاء Windows وAndroid. للحصول على مزيد من المعلومات حول كيفية إعداد محطة أجهزة مشتركة، راجع [تكوين محطة أجهزة Retail وتثبيتها](./retail-hardware-station-configuration-installation.md).

1. انتقل إلى **Retail and Commerce \> إعداد قناة \> إعداد POS \> السجلات**.
2. حدد السجل **SANFRAN-5**، ثم حدد **تحرير**.
3. قم بتغيير القيمة لحقل **ملف تعريف الجهاز** من **HW002** إلى **HW001**، ثم حدد **حفظ**.
4. لمزامنة التغييرات، انتقل إلى **Retail and Commerce \> تكنولوجيا معلومات Retail and Commerce \> جدول التوزيع**.
5. حدد جدول التوزيع **1090**، ثم في جزء الإجراء، حدد **تشغيل الآن**.
6. حدد **نعم** ثم **موافق** لبدء مزامنة البيانات. 

### <a name="install-modern-pos"></a>تثبيت Modern POS

1. انتقل إلى **Retail and Commerce \> إعداد قناة \> إعداد POS \> الأجهزة**.
2. حدد الجهاز **SANFRANCIS-5**.
3. في جزء الإجراء، حدد **تنزيل**، ثم حدد **ملف التكوين**.
4. حدد **تنزيل**، ثم حدد **Retail Modern POS**. 
5. عند تنزيل ملف **ModernPOSSetup.exe**، حدد **فتح ملف**.

    ![فتح ملف.](./dev-itpro/media/PAYMENTS/openfile.png)

6. حدد **التالي** للانتقال خلال عملية التثبيت. عند استكمال عملية التثبيت، حدد **إغلاق**.

### <a name="activate-modern-pos"></a>تنشيط Modern POS

1. في سطح مكتب Windows، حدد زر **بدء**، ثم أدخل **Retail Modern POS**.
2. حدد تطبيق **Retail Modern POS** لبدء التنشيط.
3. حدد **التالي**. يحب أن تكون حقول **عنوان URL للخادم** و **معرف الجهاز** و **رقم التسجيل** مملوءة مسبقًا بالمعلومات من ملف التكوين الذي قمت بتنزيله في الإجراء السابق.
4. حدد **تنشيط**.
5. يظهر مربع حوار المصادقة. حدد الحساب الذي يستخدم عنوان البريد الإلكتروني الذي كان مرتبطًا في السابق بالعامل **000713 - Andrew Collette**.

    > [!NOTE]
    > إذا لم تكن قد قمت بربط عامل بهويتك، فسيكون التنشيط غير ناجح. في هذه الحالة، اتبع الخطوات تحت قسم "ربط عامل بهويتك" في المقال [تكوين بيئة تقييم Dynamics 365 Commerce](cpe-post-provisioning.md#associate-a-worker-with-your-identity).
    
6. عندما مطالبتك بالسماح للمؤسسة بإدارة الجهاز، حدد **هذا التطبيق فقط**.
7. عند استكمال عملية التنشيط، حدد **الشروع في العمل**.

### <a name="enable-bopis-in-modern-pos"></a>تمكين BOPIS في Modern POS

1. سجل الدخول إلى Modern POS باستخدام **000713** كمعرف مستخدم و **123** ككلمة المرور.
2. أثناء تشغيل الفيديو التقديمي للإرشادات التفصيلية، حدد خانتي اختيار في الزاوية السفلية اليسرى لمربع الحوار، ثم أغلق مربع الحوار.
3. إذا لم تتم مطالبتك بإغلاق الوردية، فقم بالتمرير إلى اليمين على صفحة **الترحيب**، وحدد **إغلاق الوردية**، ثم سجل مرة أخرى الدخول إلى نقطة البيع.
4. بعد أن تسجل الدخول، عند مطالبتك، حدد **تنفيذ عملية غير متعلقة بالدرج**.
5. في صفحة **الترحيب**، قم بالتمرير إلى اليمين، وحدد عملية **تحديد محطة الأجهزة**.
6. حدد **إدارة**، وقم بتعيين خيار **استخدام محطة الأجهزة** إلى **تشغيل**، ثم حدد **موافق**.
7. سجل خروجك من نقطة البيع، ثم سجل دخولك مرة أخرى.
8. بعد أن تسجل الدخول، حدد **فتح وردية جديدة**، ثم حدد **الدرج**.

## <a name="complete-a-bopis-scenario"></a>استكمال سيناريو BOPIS

### <a name="create-a-storefront-order-for-in-store-pickup"></a>إنشاء أمر واجهة متجر للانتقاء في المتجر

1. انتقل إلى عنوان URL الذي حددته في خطوة [تهيئة التجارة الإلكترونية](./provisioning-guide.md#initialize-e-commerce) أثناء تكوين البيئة.
2. حدد أحد العناصر، وحدد **إضافة إلى عربة التسوق**.
3. في صفحة حقيبة التسوق، حدد **التقاط هذا** لسطر الأمر الذي أضفته للتو.
4. في مربع حوار **تحديد متجر**، أدخل **سان فرانسيسكو**، ثم حدد زر **بحث**.
5. في قائمة النتائج، ابحث عن متجر سان فرانسيسكو وحدد **التقاط هنا**.
6. في صفحة حقيبة التسوق، حدد **سداد مع الخروج كضيف**. 

    > [!NOTE]
    > للمتابعة في عملية السداد مع الخروج، يجب أن تقبل إشعار ملفات تعريف الارتباط. يظهر هذا الإشعار كلافتة أعلى صفحة السداد مع الخروج.

7. بالنسبة لطريقة الدفع عبر بطاقة الائتمان، أدخل التفاصيل التالية:

    - **اسم حامل البطاقة:**: أدخل أي اسم.
    - **رقم البطاقة:** أدخل **4111-1111-1111-1111**.
    - **تاريخ انتهاء الصلاحية:** أدخل **10/20**.
    - **رمز قيمة التحقق من صحة بطاقة الائتمان (CVV):** أدخل **737**.

    > [!IMPORTANT]
    > لا تحاول أبدا، تحت أي ظرف من الظروف، استخدام معلومات بطاقة الائتمان الفعلية في موقع الاختبار.

8. تابع عملية السداد مع الخروج من خلال إدخال تفاصيل عنوان الفوترة، ثم حدد **حفظ واستمرار**.
9. عندما يكون الأمر جاهزًا للتقديم، حدد **سداد مع الخروج**.

### <a name="synchronize-online-orders-to-the-back-office"></a>مزامنة الأوامر على الإنترنت مع مكتب الدعم

لمزيد من المعلومات حول كيفية مزامنة الطلبات على الإنترنت، راجع [نشر المبيعات على الإنترنت والمدفوعات](./tasks/posting-online-sales-payments.md).

### <a name="pick-up-an-order-in-the-store"></a>التقاط أمر من المتجر

1. سجل الدخول إلى نقطة البيع.
2. في شاشة **الترحيب**، حدد **استيفاء الأمر**
3. في قائمة العناصر للالتقاط، حدد السطر من الأمر الذي تم تقديمه على الإنترنت.
4. أثناء تحديد سطر الأمر، حدد **التقاط**.

    تتم إضافة عنصر السطر إلى شاشة المعاملة، ويظهر **$0.00** كالرصيد المستحق.

5. حدد الرصيد المستحق بقية **$0.00**، أو حدد أي طريقة دفع لختام المعاملة.

## <a name="troubleshooting"></a>استكشاف الأخطاء وإصلاحها

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a>الطلبات على الإنترنت التي تم استردادها في نقطة البيع برصيد مستحق غير صفر

عند استرداد طلب للانتقاء في المتجر، إذا كان الرصيد المستحق ليس 0 (صفر)، تأكد من أنه يجري استخدام Modern POS، وأن محطة الأجهزة نشطة. في حالة استخدام Cloud POS أو Modern POS for iOS، تأكد من أن محطة الأجهزة نشطة. بعض أشكال محطات الأجهزة النشطة تكون مطلوبة لاسترداد المدفوعات التي تتم عبر الإنترنت.

### <a name="general-issues-with-payment-capture"></a>المشكلات العامة مع التقاط الدفع

مع كافة المشكلات العامة، يجب دائمًا أن تراجع سجلات الأحداث الخاصة بـ Modern POS محطة الأجهزة لـ Internet Information Services (IIS) كخطوة أولى. يمكنك العثور على هذه السجلات تحت العُقد التالية في سجل أحداث Windows:

- سجلات الخدمات والتطبيقات \> Microsoft \> Dynamics \> Commerce-ModernPOS
- سجلات الخدمات والتطبيقات \> Microsoft \> Dynamics \> Commerce-محطة الأجهزة

## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة على بيئة تقييم Dynamics 365 Commerce](cpe-overview.md)

[توفير بيئة تقييم Dynamics 365 Commerce](provisioning-guide.md)

[تكوين الميزات الاختيارية لبيئة تقييم Dynamics 365 Commerce](cpe-optional-features.md)

[الأسئلة الشائعة حول بيئة تقييم Dynamics 365 Commerce](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[مدخل Microsoft Azure](https://azure.microsoft.com/features/azure-portal)

[موقع ويب Dynamics 365 Commerce](https://aka.ms/Dynamics365CommerceWebsite)

[موصل مدفوعات Adyen](./dev-itpro/adyen-connector.md?tabs=8-1-3)

[حفظ وسائل الدفع عبر الإنترنت باستخدام موصل Adyen](./dev-itpro/adyen-connector-listpi.md)

[نظرة عامة على مدفوعات القنوات متعددة الاتجاهات](./omni-channel-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]