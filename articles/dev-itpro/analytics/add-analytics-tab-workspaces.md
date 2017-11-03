---
title: "إضافة التحليلات إلى مساحات العمل باستخدام Power BI المدمج"
description: "يوضح هذا الموضوع كيفية تضمين تقرير Power BI في علامة تبويب \"التحليلات\" في مساحة عمل."
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations, Platform
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.intro: Platform update 8
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: fc8102d945faf9ad533f57ec1a45b0e0dc344963
ms.openlocfilehash: d36abbf7c08c56d84ed83dbec1bfa33f30b47ef5
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a>إضافة التحليلات إلى مساحات العمل باستخدام Power BI المدمج

[!include[banner](../includes/banner.md)]

> [!NOTE]
> يتم دعم هذه الميزة في Dynamics 365 for Finance and Operations (الإصدار 7.2 والإصدارات اللاحقة).

# <a name="introduction"></a>مقدمة
يوضح هذا الموضوع كيفية تضمين تقرير Microsoft Power BI في علامة تبويب **التحليلات** في مساحة عمل. بالنسبة إلى المثال الذي تم تقديمه هنا، سنقوم بتوسيع مساحة عمل **إدارة الحجز** في تطبيق إدارة الأسطول لتضمين مساحة عمل تحليلية على علامة تبويب **التحليلات**.

# <a name="prerequisites"></a>المتطلبات الأساسية
+ الوصول إلى بيئة مطور تقوم بتشغيل تحديث النظام الأساسي 8 أو الإصدارات الأحدث.
+ تقرير تحليلي (ملف pbix.) تم إنشاؤه باستخدام Microsoft Power BI Desktop"، وله نموذج بيانات مصدره قاعدة بيانات مخزن الكيانات.

# <a name="overview"></a>نظرة عامة
سواء قمت بتوسيع مساحة عمل تطبيق موجودة أو بتقديم مساحة عمل جديدة خاصة بك، يمكنك استخدام طرق العرض التحليلية المضمنة لتقديم عروض ثاقبة وتفاعلية لبيانات عملك. تتكون عملية إضافة علامة تبويب مساحة عمل تحليلية من أربع خطوات.

1. إضافة ملف pbix. كمورد Dynamics 365.
2. تحديد علامة تبويب مساحة عمل تحليلية.
3. تضمين مورد pbix. في علامة تبويب مساحة العمل.
4. اختياري: إضافة ملحقات لتخصيص طريقة العرض.

> [!NOTE]
> للحصول على مزيد من المعلومات حول كيفية إنشاء تقارير تحليلية، راجع [بدء استخدام Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/). تعتبر هذه الصفحة مصدرًا رائعًا للحصول على معلومات دقيقة من شأنها مساعدتك في إنشاء حلول تتعلق بإعداد تقارير تحليلية مقنعة.

# <a name="add-a-pbix-file-as-a-resource"></a>إضافة ملف pbix. كمورد
قبل أن تبدأ، يجب إنشاء تقرير Power BI الذي ستقوم بتضمينه في مساحة العمل أو الحصول عليه. للحصول على مزيد من المعلومات حول كيفية إنشاء تقارير تحليلية، راجع [بدء استخدام Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).
 
اتبع هذه الخطوات لإضافة ملف pbix. كمنتج لمشروع Visual Studio.

1. أنشئ مشروعًا جديدً في النموذج المناسب.
2. في "مستكشف الحلول"، حدد المشروع وانقر بزر الماوس الأيمن فوقه، ثم حدد **إضافة** > **صنف جديد**.
3. في **إضافة صنف جديد**، تحت **منتجات Operations**، حدد قالب **المورد**.
4. أدخل اسمًا سيتم استخدامه للإشارة إلى التقرير في بيانات تعريف X++، ومن ثم انقر فوق **إضافة**.

    ![مربع الحوار "إضافة صنف جديد"](media/analytical-workspace-add.png)

5. ابحث عن ملف pbix. الذي يحتوي على تعريف التقرير التحليلي، ثم انقر فوق **فتح**.

    ![حدد مربع حوار "ملف المورد"](media/analytical-workspace-select-resource.png)
  
والآن بعد أن قمت بإضافة ملف pbix. كمورد Dynamics 365، يمكنك تضمين التقارير في مساحات العمل وإضافة الارتباطات المباشرة باستخدام عناصر القائمة.

# <a name="add-a-tab-control-to-an-application-workspace"></a>إضافة عنصر تحكم علامة تبويب إلى مساحة عمل التطبيق
في هذا المثال، سنقوم بتوسيع مساحة عمل **إدارة الحجز** في نموذج إدارة الأسطول عن طريق إضافة علامة تبويب **التحليلات** إلى تعريف النموذج **FMClerkWorkspace**.
 
يبين الرسم التوضيحي التالي الشكل الذي يتخذه النموذج **FMClerkWorkspace‎** في المصمم في Microsoft Visual Studio.

![نموذج FMClerkWorkspace قبل التغييرات](media/analytical-workspace-definition-before.png)

اتبع هذه الخطوات لتوسيع تعريف النموذج لمساحة عمل **إدارة الحجز**.

1. افتح مصمم النماذج لتوسيع تعريف التصميم.
2. في تعريف التصميم، حدد العنصر العلوي المسمى **تصميم | نمط: تشغيلي في مساحة العمل**.
3. انقر بزر الماوس الأيمن، ثم حدد **جديد** > **علامة التبويب** لإضافة عنصر تحكم جديد مسمى **FormTabControl1**.
4. في مصمم النماذج، حدد **FormTabControl1**.
5. انقر بزر الماوس الأيمن، ثم حدد **صفحة علامة تبويب جديدة** لإضافة صفحة علامة تبويب جديدة.
6. أعد تسمية صفحة علامة التبويب باسم ذي مغزى، مثل **مساحة عمل**.
7. في مصمم النماذج، حدد **FormTabControl1**.
8. انقر بزر الماوس الأيمن، ثم حدد **صفحة علامة تبويب جديدة**.
9. أعد تسمية صفحة علامة التبويب باسم ذي مغزى، مثل **تحليلات**.
10. في مصمم النماذج، حدد **التحليلات (صفحة علامة التبويب)**.
11. عيّن خاصية **التسمية التوضيحية** إلى **التحليلات**.
12. انقر بزر الماوس الأيمن فوق عنصر التحكم، ثم حدد **جديد** > **مجموعة** لإضافة عنصر تحكم مجموعة نماذج جديدة.
13. أعد تسمية مجموعة النماذج باسم ذي مغزى، مثل **powerBIReportGroup**.
14. في مصمم النماذج، حدد **PanoramaBody (علامة التبويب)**، ثم قم بسحب عنصر التحكم إلى علامة تبويب **مساحة العمل**.
15. في تعريف التصميم، حدد العنصر العلوي المسمى **تصميم | نمط: تشغيلي في مساحة العمل**.
16. انقر بزر الماوس الأيمن، ثم حدد **إزالة النقش**.
17. انقر بزر الماوس الأيمن مرة أخرى، ثم حدد **إضافة نمط** > **مساحة عمل مبوبة**.
18. نفّذ عملية إنشاء للتحقق من التغييرات التي أجريتها.
 
يبين الرسم التوضيحي التالي الشكل الذي يتخذه التصميم بعد تطبيق هذه التغييرات.

![FMClerkWorkspace بعد التغييرات](media/analytical-workspace-definition-after.png)

والآن بعد أن قمت بإضافة عناصر تحكم النموذج التي سيتم استخدامها لتضمين تقرير مساحة العمل، يجب تحديد حجم عنصر التحكم الأصل بحيث يستوعب التخطيط. بشكل افتراضي، سوف تظهر في التقرير الصفحة **"جزء عوامل تصفية"** والصحفة **علامة التبويب**. ومع ذلك، يمكنك تغيير كيفية ظهور عناصر التحكم هذه بما يتناسب مع المستخدم المستهدف للتقرير.
 
> [!NOTE]
> بالنسبة إلى مساحات العمل المضمنة، نوصي باستخدام الملحقات لإخفاء الصفحتين **"جزء عوامل تصفية"** و**علامة التبويب**، لتوفير التناسق.
 
لقد أتممت الآن مهمة توسيع تعريف نموذج التطبيق. للحصول على مزيد من المعلومات حول كيفية استخدام الملحقات لإجراء التخصيصات، راجع  [التخصيص: تراكب الطبقات والملحقات](../extensibility/customization-overlayering-extensions.md).

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a>إضافة منطق تسلسل العمل X++ لتضمين عنصر تحكم العارض
اتبع هذه الخطوات لإضافة منطق تسلسل العمل الذي يقوم بتهيئة عنصر تحكم العارض المضمن في مساحة عمل **إدارة الحجز**.

1. افتح مصمم النماذج **FMClerkWorkspace** لتوسيع تعريف التصميم.
2. اضغط F7 للوصول إلى التعليمات البرمجية خلف تعريف التعليمات البرمجية.
3. أضف التعليمات البرمجية X++ التالية.

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. نفّذ عملية إنشاء للتحقق من التغييرات التي أجريتها.

لقد أتممت الآن مهمة إضافة منطق تسلسل العمل لتهيئة عنصر تحكم عارض التقرير المضمن. يبين الرسم التوضيحي التالي الشكل الذي تتخذه مساحة العمل بعد تطبيق هذه التغييرات.

![تقرير مضمن في مساحة العمل](media/analytical-workspace-final.png)

> [!NOTE]
> يمكنك الوصول إلى طريقة العرض التشغيلية الموجودة باستخدام علامات تبويب مساحة العمل تحت عنوان الصفحة.

# <a name="reference"></a>المرجع

## <a name="pbireporthelperinitializereportcontrol-method"></a>أسلوب PBIReportHelper.initializeReportControl
يوفر هذا المقطع معلومات حول فئة المساعد التي تُستخدم لتضمين تقرير Power BI (مورد pbix.) في عنصر تحكم مجموعة النماذج.

### <a name="syntax"></a>بناء الجملة
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a>المحددات

| الاسم | ‏‏الوصف |
|---|---|
| resourceName | اسم مورد pbix. |
| formGroupControl | عنصر تحكم مجموعة النماذج لتطبيق عنصر تحكم تقرير Power BI عليه. |
| defaultPageName | اسم الصفحة الافتراضية |
| showFilterPane | قيمة منطقية تشير إلى ما إذا كان يجب عرض جزء عامل التصفية (**true**) أو إخفاؤه (**false**). |
| showNavPane | قيمة منطقية تشير إلى ما إذا كان يجب عرض جزء التنقل (**true**) أو إخفاؤه (**false**). |
| defaultFilters | عوامل التصفية الافتراضية لتقرير Power BI. |

