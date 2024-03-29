---
title: ترحيل عمليات الوصول والإرسالات إلى نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي
description: توفر هذه المقالة مثالاً يوضح كيفية ترحيل عمليات الوصول والإرسالات الخاصة بنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.
author: AdamTrukawka
ms.date: 08/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: b6d46efd477f526c4bec3515086e10aa8172c579
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280676"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>ترحيل عمليات الوصول والإرسالات إلى نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي

[!include [banner](../includes/banner.md)]

توفر هذه المقالة مثالاً يوضح كيفية ترحيل عمليات الوصول والإرسالات الخاصة بنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. يستخدم المثال الكيان القانوني لشركة **ITCO**.

## <a name="setup"></a>الإعداد

1. استيراد أحدث إصدار من تكوينات التقارير الإلكترونية التالية :

    - نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي
    - تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي
    - نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (IT)

    ابحث عن مزيد من التفاصيل في [تنزيل تكوينات التقارير الإلكترونية من المستودع العمومي لخدمة التكوين](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. في Microsoft Dynamics 365 Financeـ حدد التسلسلات الرقمية التالية على أنها مستمرة: **Gene\_397** و **Acco\_16403** و **Gene\_407** و **PUR\_EU**.

    1. انتقل إلى **إدارة المؤسسة** > **التسلسلات الرقمية** > **التسلسلات الرقمية**.
    2. في الشبكة، حدد أحد رموز التسلسل الرقمي.
    3. في جزء الإجراءات، حدد **تحرير**.
    4. في علامة التبويب السريعة **عام**، في قسم **الإعداد**، قم بتعيين الخيار **المستمر** إلى **نعم**.
    5. في جزء الإجراءات، حدد **حفظ**.

3. قم بتعيين عنوان مستودعز

    1. انتقل إلى **إدارة المستودعات** &gt; **إعداد** &gt; **مستودع** &gt; **مستودعات**.
    2. في القائمة، حدد المستودع **11**.
    3. في علامة التبويب السريعة **العنوان**، حدد **إضافة**.
    4. في مربع الحوار **جديد** **عنوان**، في حقل **الاسم** **أو** **الوصف**، أدخل **رئيسي**.
    5. في حقل **البلد/المنطقة**، حدد **ITA (إيطاليا)**.
    6. في حقل **المدينة**، حدد **Aprilia**.
    7. حدد **موافق**.

4. إعداد أكواد الحركات.

    1. انتقل إلى **ضريبة** > **الإعداد** > **التجارة الخارجية** > **أكواد الحركة**.
    2. حدد **جديد**، ثم قم بإعداد كود حركة لنقل الممتلكات.

        - أدخل **1** في الحقل **كود الحركة**.
        - في حقل **الاسم**، أدخل **نقل الملكية**.

    3. حدد **جديد**، ثم قم بإعداد كود حركة للمرتجعات.

        - أدخل **2** في الحقل **كود** **الحركة**.
        - في حقل **الاسم**، أدخل **إرجاع البضائع**.

5.  إعداد محددات التجارة الخارجية.

    1. انتقل إلى **الضريبة** > **الإعداد** > **التجارة الخارجية** > **معلمات التجارة الخارجية**.
    2. في علامة التبويب **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**، في علامة التبويب السريعة **عام**، في حقل **رمز** **الحركة**، حدد **1**.
    3. في حقل **إشعار الدائن**، حدد **2**.
    4. في حقل **فترة الإبلاغ عن المبيعات**، حدد **شهر**.
    5. في حقل **فترة الإبلاغ عن المشتريات**، حدد **شهر**.
    6. في علامة التبويب السريعة **إعداد التقارير الإلكتروني**، في حقل **تعيين تنسيق الملف**، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (IT)**.
    7. في حقل **تعيين تنسيق التقارير**، حدد **تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    8. في علامة التبويب السريعة **تدرج هرمي لرمز السلع**، في حقل **التسلسل الهرمي للفئة**، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    9. على علامة التبويب السريعة **القيمة الإحصائية**، قم بتعيين الخيار **طباعة وتصدير البيانات الإحصائية** إلى **نعم**.
    10. في علامة التبويب **خصائص البلد/المنطقة**، تحقق من وجود الأسطر التالية.

        | **الطرف/البلد/المنطقة** | **كود نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي** | **عملة** | **نوع البلد/المنطقة** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | يورو          | داخلي                |
        | SMR                      | SM                 | يورو          | محلي خاص        |

    11. على شريط الأدوات، حدد **جديد** لإنشاء السطر التالي.

        | **الطرف/البلد/المنطقة** | **كود نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي** | **عملة** | **نوع البلد/المنطقة** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | كرونا دانمركية          | الاتحاد الأوروبي                      |

6. إعداد أرقام الإعفاء الضريبي.

    1. انتقل إلى **الضريبة** > **الإعداد** > **ضريبة المبيعات** > **أرقام الإعفاء الضريبي**.
    2. في جزء الإجراءات، حدد **جديد** لإنشاء الأسطر التالية.

        | **البلد/المنطقة** | **رقم الإعفاء الضريبي** | **اسم الشركة** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | مورد الاتحاد الأوروبي        |
        | DNK                | DK0987654321          | التقارير الإلكترونية للعملاء      |

7. قم بتعيين عنوان المورد.

    1. انتقل إلى **الحسابات الدائنة** &gt; **الموردون** &gt; **كافة الموردين**.
    2. في الشبكة، حدد **مورد UE**.
    3. في علامة التبويب السريعة **العناوين**، حدد **إضافة**.
    4. في مربع الحوار **عنوان جديد**، في حقل **الاسم أو الوصف**، أدخل **ألمانيا**.
    5. في حقل **البلد أو المنطقة** حدد **DEU**.
    6. حدد **موافق** لإنشاء العنوان الجديد.
    7. في علامة التبويب السريعة **الفاتورة والتسليم**، في قسم **ضريبة المبيعات**، في حقل **رقم الإعفاء الضريبي**، حدد **الكل**، ثم حدد **DE1234567890**.
    8. في جزء الإجراءات، حدد **حفظ**.

8. قم بتعيين عناوين العملاء.

    1. انتقل إلى **الحسابات المدينة** > **العملاء** > **جميع العملاء**.
    2. في الشبكة، حدد **ITCO-000001**.
    3. في علامة التبويب السريعة **العناوين**، حدد **تحرير**.
    4. في مربع الحوار **عنوان جديد**، في حقل **الاسم أو الوصف**، أدخل **سان مارينو**.
    5. في حقل **البلد أو المنطقة** حدد **SMR**.
    6. حدد **موافق** لإنشاء العنوان الجديد.
    7. في علامة التبويب السريعة **الفاتورة والتسليم**، في قسم **الفاتورة**، في حقل **حساب المورد**، حدد **ITCO-0000001**.
    8. في حقل **مجموعة التسلسلات الرقمية**، حدد **IT\_VENDOM**.
    9. حدد **حفظ** في جزء الإجراءات وأغلق الصفحة.
    10. في صفحة **جميع العملاء**، في الشبكة، حدد **ITCO-000002**.
    11. في علامة التبويب السريعة **العناوين**، حدد **إضافة**.
    12. في مربع الحوار **عنوان جديد**، في حقل **الاسم أو الوصف**، أدخل **الدانمرك**.
    13. في حقل **البلد أو المنطقة** حدد **DNK**.
    14. حدد **موافق** لإنشاء العنوان الجديد.
    15. في علامة التبويب السريعة **الخصائص السكانية للمبيعات**، في حقل **العملة**، حدد **DKK**.
    16. في علامة التبويب السريعة **الفاتورة والتسليم**، في قسم **ضريبة المبيعات**، في حقل **مجموعة ضريبة المبيعات**، حدد **IT\_PUREU**.
    17. في حقل **رقم الإعفاء الضريبي**، حدد **الكل**، ثم حدد **DK0987654321**.
    18. في جزء الإجراءات، حدد **حفظ**.

9. إعداد التدرج الهرمي للفئات.

    1. انتقل إلى **إدارة معلومات المنتج** > **الإعداد** > **الفئات والسمات** > **التدرجات الهرمية للفئات**.
    2. في الشبكة ، حدد **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    3. في جزء الإجراءات، حدد **عقدة الفئة الجديدة‬**.
    4. في حقل **الاسم**، أدخل **‏الخدمة**.
    5. في حقل **الكود**، أدخل **123456**.
    6. في جزء الإجراءات، حدد **حفظ**.

10. إعداد المنتجات.

    1. انتقل إلى **إدارة معلومات المنتج** > **المنتجات** > **المنتجات الصادرة**.
    2. في الشبكة ، حدد **ITEM**.
    3. في علامة التبويب السريعة **الشراء**، في قسم **الإدارة**، في حقل **المورد**، حدد **ITCO-000001**.
    4. في علامة التبويب السريعة **التجارة الخارجية**، في قسم **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**، في حقل **المجتمع**، حدد **\[100 200 30\] المتحدث**.
    5. في قسم **المنشأ**، في حقل **البلد/المنطقة**، حدد **DEU**.
    6. في حقل **المنطقة/المحافظة**، حدد **BE**.
    7. في علامة التبويب السريعة **إدارة المخزون**، في قسم **صافي القياسات**، في حقل **صافي الوزن**، أدخل **5**.
    8. في جزء الإجراءات، حدد **حفظ**.
    9. في صفحة **المنتجات الصادرة**، في الشبكة، حدد **عنصر الخدمة**.
    10. في علامة التبويب السريعة **التجارة الخارجية**، في قسم **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**، في حقل **المجتمع**، حدد **\[123456\] الخدمة**.
    11. في جزء الإجراءات، حدد **حفظ**.

11. إعداد طرق النقل.

    1. انتقل إلى **الضريبة** > **الإعداد** > **التجارة الخارجية** > **طريقة النقل**.
    2. في جزء الإجراءات، حدد **جديد** لإنشاء طرق النقل التالية.

        | **النقل** | **‏‏الوصف** |
        |---------------|-----------------|
        | 1             | طريق            |
        | 2             | الجو             |

12. إعداد طريقة التسليم.

    1. انتقل إلى ‏‫**التدبير والتوريد‬** > **الإعداد** > **التوزيع** > **أوضاع التسليم**.
    2. في جزء الإجراء، حدد **جديد**.
    3. في حقل **طريقة التسليم**، أدخل **1**.
    4. في حقل **الوصف**، أدخل **الشاحنة**.
    5. من علامة التبويب السريعة **التجارة الخارجية**، في حقل **النقل**، حدد **1 طريق**.
    6. في جزء الإجراءات، حدد **حفظ**.

13. إعداد شروط التسليم.

    1. انتقل إلى **الحسابات الدائنة** > **الإعداد** > **شروط الدفع**.
    2. في القائمة، حدد  **CFR**.
    3. في علامة التبويب السريعة **عام**، في حقل **رمز نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**، حدد **1**.

## <a name="post-arrivals-for-intrastat"></a>ترحيل عمليات الوصول لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي

### <a name="purchase-goods-by-using-a-purchase-order"></a>شراء السلع باستخدام أمر شراء

يوضح هذا الجزء من المثال كيفية استخدام أمر شراء لشراء سلع (أصناف) من دول الاتحاد الأوروبي.

1. انتقل إلى **الحسابات الدائنة** > **أوامر الشراء** > **جميع أوامر الشراء**.
2.  في جزء الإجراء، حدد **جديد**.
3.  في مربع الحوار **إنشاء أمر شراء**، في حقل **حساب المورد**، حدد **مورد UE**.
4.  في علامة التبويب السريعة **إدارة**، في حقل **اللغة**، حدد **ذلك**.
5.  حدد **موافق**.
6.  في طريقة عرض **الرأس**، على علامة التبويب السريعة **التجارة** **الخارجية**، تحقق من تعيين حقل **رمز الحركة** إلى **1**.
7.  تحقق من تعيين حقل **مقاطعة المنشأ/الوجهة** إلى **RM**.
8.  في علامة التبويب السريعة **تسليم**، في قسم **التسليم**، في حقل **طريقة التسليم**، حدد **1**.
9.  في حقل **شروط التسليم**، حدد **CFR**.
10. في طريقة عرض **البنود**، في علامة التبويب السريعة **بنود أمر الشراء**، في حقل **رقم الصنف**، حدد **صنف**.
11. في حقل **الموقع** ، حدد **1**.
12. في حقل **المستودع**، حدد **11**.
13. في حقل **كمية**، أدخل **10**.
14. في الحقل **سعر الوحدة**، أدخل **100**.
15. في علامة التبويب **إعداد**، في قسم **ضريبة المبيعات**، في حقل **مجموعة ضريبة مبيعات الصنف**، حدد **22%EU**.
16. في جزء الإجراءات، في علامة تبويب **الشراء** في مجموعة **الإجراءات**، حدد **تأكيد**.
17. في جزء الإجراءات، في علامة التبويب **الفاتورة**، في المجموعة **إنشاء**، حدد **فاتورة**.
18. في جزء الإجراء، حدد **النموذج الافتراضي**.
19. في حقل **الكمية الافتراضية للبنود**، حدد **الكمية المطلوبة**، ثم حدد **موافق**.
20. في علامة التبويب السريعة **رأس فاتورة المورد**، في قسم **تعريف الفاتورة**، في حقل **الرقم**، أدخل **0001**.
21. في قسم **تواريخ الفواتير**، في حقل **تاريخ الفاتورة**، حدد **7/9/2021**.
22. في جزء الإجراء، حدد **ترحيل** لترحيل الفاتورة.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>خدمات الشراء باستخدام فاتورة مورد

يوضح هذا الجزء من المثال كيفية استخدام فاتورة المورد لشراء الخدمات من دول الاتحاد الأوروبي.

1. انتقل إلى **الحسابات الدائنة** > **الفواتير** > **دفتر يومية الفواتير**.
2. في جزء الإجراء، حدد **جديد**.
3. في حقل **الاسم**، حدد **VEND\_EUINV**.
4. في جزء الإجراءات، حدد **البنود**.
5. في حقل **‏التاريخ**، أدخل **7/9/2021**.
6. في حقل **نوع الحساب**، حدد **المورد**.
7. في حقل **الحساب**، حدد **مورد UE**.
8. في حقل **تاريخ الفاتورة**، حدد **7/9/2021**.
9. في حقل **الفاتورة**، أدخل **ITA-0004**.
10. في حقل **الائتمان**، أدخل **120000**.
11. في حقل **نوع** **الحساب المقابل**، حدد **دفتر الأستاذ**.
12. في حقل **الحساب المقابل**، حدد **110130**.
13. في حقل **مجموعة ضرائب المبيعات**، حدد **IT\_PUREU**.
14. في حقل **مجموعة ضرائب مبيعات الأصناف**، حدد **22%EU**.
15. في علامة التبويب **التجارة الخارجية**، اتبع الخطوات التالية:

    1. في حقل **كود الحركة**، حدد **1**.
    2. في حقل **النقل**، حدد **2 Air**.
    3. في حقل **السلعة**، حدد **\[123456\] الخدمة**.
    4. في حقل **البلد أو المنطقة** حدد **ITA**.
    5. في حقل **المنطقة/المحافظة**، حدد **LAZ**.
    6. في حقل **مقاطعة المنشأ/الوجهة**، حدد **LT**


16. في جزء الإجراءات، حدد **ترحيل**.
17. إنشاء إعلان نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لعمليات الوصول.

    1. انتقل إلى **الضريبة** > **الإقرارات‬** > **التجارة الخارجية** > **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    2. في جزء الإجراءات، حدد **تحويل**.
    3. في مربع الحوار **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نقل)**، قم تعيين الخيار **فاتورة المورد** إلى **نعم**.
    4. حدد **موافق** لنقل الحركات، ثم مراجعة دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

   ![صفحة دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، علامة التبويب نظرة عامة.](media/ita_intrastat_journal_vendor_invoice.png)

18. راجع علامة التبويب **عام** لأمر الشراء.

    ![تفاصيل بند دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لأمر الشراء](media/ita_intrastat_journal_purchase_order_line_details.png)

19. راجع علامة التبويب **عام** لفاتورة المورد.

    ![تفاصيل بند دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لفاتورة المورد](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. إنشاء بيانات تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لعمليات الوصول.

    1. في جزء الإجراءات، حدد **إخراج** > **تقرير**.
    2. في مربع الحوار **تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**، في قسم **التاريخ**، في حقل **من التاريخ**، حدد **7/1/2021**.
    3. في حقل **‏إلى التاريخ**، حدد **7/31/2021**.
    4. في قسم **خيارات التصدير**، قم بتعيين الخيارين **إنشاء ملف** و **إنشاء تقرير** إلى **نعم**.
    5. في حقل **اسم الملف**، أدخل **ملف عمليات الوصول**.
    6. في حقل **اسم ملف التقرير**، أدخل **تقرير عمليات الوصول**.
    7. في حقل **الاتجاه**، حدد **عمليات الوصول**.
    8. في الحقل **‏‫الرقم المرجعي**، أدخل **123456**.
    9. حدد **موافق**  لإنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي وملف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي، ومراجعتهما.

    يبين الرسم التوضيحي التالي مثالاً على تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

    ![تقرير عمليات وصول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.](media/ita_intrastat_arrivals_report.png)

    يبين الرسم التوضيحي التالي مثالاً على ملف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

    ![ملف عمليات وصول نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>ترحيل الإرسالات لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي

### <a name="sell-goods-by-using-a-sales-order"></a>بيع السلع باستخدام أمر مبيعات

يوضح هذا الجزء من المثال كيفية استخدام أمر مبيعات لبيع سلع (أصناف) من دول الاتحاد الأوروبي.

1. انتقل إلى **الحسابات المدينة** > **الأوامر** > **كافة أوامر المبيعات**.
2. في جزء الإجراء، حدد **جديد**.
3. في مربع الحوار **إنشاء أمر مبيعات**، في حقل **حساب العميل**، حدد **ITCO-000002**.
4. حدد **موافق**.
5. في طريقة عرض **الرأس**، على علامة التبويب السريعة **التسليم**، في قسم **معلومات التسليم المتنوعة** في حقل **طريقة التسليم**، حدد **1 شاحنة**.
6. في حقل **شروط التسليم**، حدد **CFR**.
7. في طريقة عرض **البنود**، في علامة التبويب السريعة **بنود أمر المبيعات**، في حقل **رقم الصنف**، حدد **ITEM**.
8. في حقل **كمية**، أدخل **50**.
9. في حقل **الموقع** ، حدد **1**.
10. في حقل **المستودع**، حدد **11**.
11. في الحقل **سعر الوحدة**، أدخل **250**.
12. في علامة التبويب السريعة **تفاصيل البنود**، في علامة التبويب **إعداد**، في قسم **ضريبة المبيعات**، في حقل **مجموعة ضرائب مبيعات الأصناف**، حدد **22%EU**.
13. في جزء الإجراءات، حدد **حفظ**.
14. في جزء الإجراء، في علامة التبويب **فاتورة**، في مجموعة **الإنشاء**، حدد **الفاتورة** لإنشاء الفاتورة للأمر.
15. في مربع الحوار **ترحيل الفاتورة**، في علامة التبويب السريعة **المعلمات**، في القسم **المعلمة**، في الحقل **الكمية**، حدد **الكل**.
16. في علامة التبويب السريعة **إعداد**، في حقل **تاريخ** **الفاتورة**، حدد **7/9/2021**.
17. حدد **موافق**.
18. راجع البنود في دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

    1. انتقل إلى **الضريبة** > **الإقرارات‬** > **التجارة الخارجية** > **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    2. في جزء الإجراءات، حدد **تحويل**.
    3. في مربع الحوار **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نقل)**، قم تعيين الخيار **فاتورة العميل** إلى **نعم**.
    4. حدد **موافق** لنقل الحركات، وراجع دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. يتم وضع علامة على حركة إشعار الدائن كتصحيح وتتميز بمبلغ الفاتورة السالب.

        ![صفحة دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي](media/ita_intrastat_journal_sales_order.png)

        ![تفاصيل بند دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لأمر المبيعات](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>إرجاع السلع باستخدام إشعار دائن

يوضح هذا الجزء من المثال كيفية استخدام إشعار دائن لإرجاع سلع (أصناف) من دول الاتحاد الأوروبي (EU).

1. انتقل إلى **الحسابات المدينة** > **الأوامر** > **كافة أوامر المبيعات**.
2. في جزء الإجراء، حدد **جديد**.
3. في مربع الحوار **إنشاء أمر مبيعات**، في حقل **حساب العميل**، حدد **ITCO-000002**.
4. حدد **موافق**.
5. في طريقة عرض **الرأس**، على علامة التبويب السريعة **التسليم**، في قسم **معلومات التسليم المتنوعة** في حقل **طريقة التسليم**، حدد **1 شاحنة**.
6. في حقل **شروط التسليم**، حدد **CFR**.
7. من علامة التبويب السريعة **التجارة الخارجية**، في حقل **كود الحركة**، حدد **2**.
8. في علامة التبويب **البنود**، في علامة التبويب السريعة **بنود أمر المبيعات**، في حقل **رقم الصنف**، حدد **ITEM**.
9. في حقل **الكمية**، أدخل **-10**.
10. في حقل **الموقع** ، حدد **1**.
11. في حقل **المستودع**، حدد **11**.
12. في الحقل **سعر الوحدة**، أدخل **250**.
13. في علامة التبويب السريعة **تفاصيل البنود**، في علامة التبويب **إعداد**، في قسم **ضريبة المبيعات**، في حقل **مجموعة ضرائب مبيعات الأصناف**، حدد **22%EU**.
14. في قسم **أمر الإرجاع**، في حقل **معرف شحنة الإرجاع**، حدد مجموعة الشحنة التي قمت بإنشائها سابقًا.
15. في جزء الإجراءات، حدد **حفظ**.
16. في جزء الإجراء، في علامة التبويب **فاتورة**، في مجموعة **الإنشاء**، حدد **الفاتورة** لإنشاء الفاتورة للأمر.
17. في علامة التبويب السريعة **المعلمات**، في قسم **المعلمة**، في حقل **الكمية**، حدد **الكل**.
18. في مربع الحوار **ترحيل الفاتورة**، في علامة التبويب السريعة **إعداد**، في حقل **تاريخ** **الفاتورة**، حدد **7/9/2021**.
19. انقر فوق **موافق** لترحيل الفاتورة.
20. راجع البنود في دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

    1. انتقل إلى **الضريبة** > **الإقرارات‬** > **التجارة الخارجية** > **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    2. في جزء الإجراءات، حدد **تحويل**.
    3. في مربع الحوار **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نقل)**، قم تعيين الخيار **فاتورة العميل** إلى **نعم**.
    4. حدد **موافق** لنقل الحركات، وراجع دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. يتم وضع علامة على حركة إشعار الدائن كتصحيح وتتميز بمبلغ الفاتورة السالب.

    ![إشعار دائن دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي](media/ita_intrastat_journal_credit_note.png)

    ![تفاصيل بند دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لإشعار الدائن](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>بيع السلع لسان مارينو باستخدام أمر مبيعات

يوضح هذا الجزء من المثال كيفية استخدام أمر مبيعات لشراء سلع (أصناف) لسان مارينو.

1. انتقل إلى **الحسابات المدينة** > **الأوامر** > **كافة أوامر المبيعات**.
2. في جزء الإجراء، حدد **جديد**.
3. في مربع الحوار **إنشاء أمر مبيعات**، في حقل **حساب العميل**، حدد **ITCO-000001**.
4. حدد **موافق**.
5. في طريقة عرض **الرأس**، على علامة التبويب السريعة **التسليم**، في قسم **معلومات التسليم المتنوعة** في حقل **طريقة التسليم**، حدد **1**.
6. في حقل **شروط التسليم**، حدد **CFR**.
7. في علامة التبويب **البنود**، في علامة التبويب السريعة **بنود أمر المبيعات**، في حقل **رقم الصنف**، حدد **ITEM**.
8. في حقل **كمية**، أدخل **30**.
9. في حقل **الموقع** ، حدد **1**.
10. في حقل **المستودع**، حدد **11**.
11. في الحقل **سعر الوحدة**، أدخل **200**.
12. في جزء الإجراءات، حدد **حفظ**.
13. في جزء الإجراء، في علامة التبويب **فاتورة**، في مجموعة **الإنشاء**، حدد **الفاتورة** لإنشاء الفاتورة للأمر.
14. في علامة التبويب السريعة **المعلمات**، في قسم **المعلمة**، في حقل **الكمية**، حدد **الكل**.
15. في مربع الحوار **ترحيل الفاتورة**، في علامة التبويب السريعة **إعداد**، في حقل **تاريخ** **الفاتورة**، حدد **7/9/2021**.
16. انقر فوق **موافق** لترحيل الفاتورة.
17. راجع البنود في دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

    1. انتقل إلى **الضريبة** > **الإقرارات‬** > **التجارة الخارجية** > **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    2. في جزء الإجراءات، حدد **تحويل**.
    3. في مربع الحوار **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي (نقل)**، قم تعيين الخيار **فاتورة العميل** إلى **نعم**.
    4. حدد **موافق** لنقل الحركات، وراجع دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

   ![دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لسان مارينو](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![تفاصيل بند دفتر يومية نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لسان مارينو](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. إنشاء إعلان نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي للإرسالات.

    1. انتقل إلى **الضريبة** &gt; **الإقرارات‬** &gt; **التجارة الخارجية** &gt; **نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**.
    2. في جزء الإجراءات، حدد **إخراج** &gt; **تقرير**.
    3. في مربع الحوار **تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي**، في قسم **التاريخ**، في حقل **من التاريخ**، حدد **7/1/2021**.
    4. في حقل **‏إلى التاريخ**، حدد **7/31/2021**.
    5. في قسم **خيارات التصدير**، قم بتعيين الخيارين **إنشاء ملف** و **إنشاء تقرير** إلى **نعم**.
    6. في حقل **اسم الملف**، أدخل **ملف الإرسالات**.
    7. في حقل **اسم ملف التقرير**، أدخل **تقرير الإرسالات**.
    8. في حقل **الاتجاه**، حدد **الإرسالات**.
    9. في الحقل **‏‫الرقم المرجعي**، أدخل **98754**.
    10. حدد **موافق**  لإنشاء تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي وملف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

        يبين الرسم التوضيحي التالي مثالاً على تقرير مطبوع لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

        ![تقرير نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي](media/ita_intrastat_report_for_dispatches.png)

        يبين الرسم التوضيحي التالي مثالاً على ملف مطبوع لنظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي.

        ![ملف نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي للإرسالات](media/ita_intrastat_file_for_dispatches.png)
