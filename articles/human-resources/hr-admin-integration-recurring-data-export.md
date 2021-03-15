---
title: إنشاء تطبيق تصدير بيانات متكررة
description: يوضح هذا المقال كيفية إنشاء تطبيق Microsoft Azure Logic الذي يقوم بتصدير البيانات من Microsoft Dynamics 365 Human Resources على جدول متكرر.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 97972d2179c42e9d2d672cbebb75643ef0a02a62
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111312"
---
# <a name="create-a-recurring-data-export-app"></a>إنشاء تطبيق تصدير بيانات متكررة

يوضح هذا المقال كيفية إنشاء تطبيق Microsoft Azure Logic الذي يقوم بتصدير البيانات من Microsoft Dynamics 365 Human Resources على جدول متكرر. يستفيد البرنامج التعليمي من واجهة برمجة تطبيقات REST لحزمة Human Resources' DMF لتصدير البيانات. بعد تصدير البيانات، يحفظ تطبيق logic حزمة البيانات المصدرة إلى Microsoft OneDrive إلى مجلد Business.

## <a name="business-scenario"></a>سيناريو الأعمال

في أحد سيناريوهات العمل النموذجية لعمليات تكامل Microsoft Dynamics 365، يجب تصدير البيانات إلى نظام نهائي على جدول متكرر. يظهر هذا البرنامج التعليمي كيفية تصدير كافة سجلات العمال من Microsoft Dynamics 365 Human Resources وحفظ قائمة العمال في OneDrive لمجلد Business.

> [!TIP]
> تمثل البيانات المُحددة التي يتم تصديرها في هذا البرنامج التعليمي ووجهة البيانات المُصدرة أمثلة فقط. يُمكنك تغييرها بسهولة لتلبي احتياجات أعمالك.

## <a name="technologies-used"></a>التقنيات المستخدمة

يستخدم هذا البرنامج التعليمي التقنيات التالية:

- **[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – مصدر البيانات الرئيسية للعمال الذين سوف يتم تصديرهم.
- **[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** - التقنية التي توفر خدمات التنسيق والجدولة للتصدير المتكرر.

    - **[الموصلات](https://docs.microsoft.com/azure/connectors/apis-list)** – التقنية المستخدمة لربط تطبيق logic بنقاط النهاية المطلوبة.

        - [HTTP مع موصل Azure AD](https://docs.microsoft.com/connectors/webcontents/)
        - موصل [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness)

- **[واجهة برمجة تطبيقات REST لحزمة DMF](../dev-itpro/data-entities/data-management-api.md)** - التقنية المستخدمة لتشغيل التصدير ومراقبة تقدمه. 
- **[OneDrive for Business](https://onedrive.live.com/about/business/)** - وجهة العاملين المُصدرين.

## <a name="prerequisites"></a>المتطلبات الأساسية

قبل البدء في التدريب في هذا البرنامج التعليمي، يجب أن يكون لديك العناصر التالية:

- بيئة Human Resources التي لها أذونات على مستوى المسؤول في البيئة
- [اشتراك Azure](https://azure.microsoft.com/free/) لاستضافة تطبيق logic.

## <a name="the-exercise"></a>التمرين

في نهاية هذا التدريب، سوف يكون لديك تطبيق logic متصل ببيئة Human Resources الخاصة بك وحساب OneDrive for Business. سوف يقوم تطبيق logic بتصدير حزمة البيانات من Human Resources، والانتظار حتى اكتمال التصدير وتنزيل حزمة البيانات المصدرة وحفظ حزمة البيانات في مجلد OneDrive for Business الذي قمت بتحديده.

سوف يشبه تطبيق logic المكتمل الرسم التوضيحي التالي.

![نظرة عامة على تطبيق logic](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a>الخطوة 1: إنشاء مشروع تصدير بيانات في Human Resources

في Human Resources، قم بإنشاء مشروع تصدير بيانات الذي سوف يقوم بتصدير العمال. قم بتسمية المشروع **تصدير العمال** ، وتأكد أن خيار **إنشاء حزمة البيانات** إلى **نعم**. أضف كيان واحد (**العامل**) إلى المشروع وحدد التنسيق المراد تصديره للمشروع. (يتم استخدام Microsoft Excel في هذا البرنامج التعليمي.)

![تصدير مشروع بيانات العاملين](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> تذكر اسم مشروع تصدير البيانات. سوف تحتاج إليه عند إنشاء تطبيق logic في الخطوة التالية.

### <a name="step-2-create-the-logic-app"></a>الخطوة 2: إنشاء تطبيق logic

تتضمن مجموعة التجارب إنشاء تطبيق logic.

1. في مدخل Azure ، قم بإنشاء تطبيق logic.

    ![صفحة إنشاء تطبيق logic.](media/integration-logic-app-creation-1.png)

2. في Logic Apps Designer ابدأ بتطبيق logic فارغ.
3. أضف [مشغل جدول متكرر](https://docs.microsoft.com/azure/connectors/connectors-native-recurrence) لتشغيل تطبيق logic كل 24 ساعة (أو وفقًا لجدول من اختيارك).

    ![مربع حوار التكرار](media/integration-logic-app-recurrence-step.png)

4. الاتصال بواجهة برمجية تطبيقات حزمة DMF REST [ExportToPackage](../dev-itpro/data-entities/data-management-api.md#exporttopackage) لجدولة تصدير حزمة بياناتك.

    1. استخدم إجراء **استدعاء طلب HTTP** من HTTP مع موصل Azure AD.

        - **عنوان URL للمورد الأساسي** - عنوان URL لبيئة Human Resources الخاصة بك (لا تقم بتضمين معلومات المسار/مساحة الاسم.)
        - **عنوان URL لـ Azure AD Resource:** `http://hr.talent.dynamics.com`

        > [!NOTE]
        > لا توفر خدمة Human Resources موصل بعد التي تكشف جميع واجهات برمجيات التطبيقات التي تتألف منها واجهة بمرجية تطبيقات REST لحزمة DMF، مثل **ExportToPackage**. بدلًا من ذلك، يجب استدعاء واجهات برمجيات التطبيقات باستخدام طلبات HTTPS الأولية من خلال HTTP مع موصل Azure AD. يستخدم هذا الموصل Azure Active Directory (Azure AD) للمصادقة والتخويل لـ Human Resources.

        ![HTTP مع موصل Azure AD](media/integration-logic-app-http-aad-connector-step.png)

    2. قم بتسجيل الدخول إلى بيئة Human Resources من خلال HTTP مع موصل Azure AD.
    3. قم بإعداد طلب **POST** HTTP لاستدعاء واجهة برمجة التطبيقات REST لحزمة DMF **ExportToPackage**.

        - **الأسلوب:** POST
        - **عنوان URL للطلب:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage
        - **نص الطلب:**

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![استدعاء إجراء طلب HTTP](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > قد تحتاج إلى إعادة تسمية كل خطوة بحيث تكون أكثر نفعًا من الاسم الافتراضي، **استدعاء طلب HTTP**. على سبيل المثال، يُمكن إعادة تسمية هذه الخطوة **ExportToPackage**.

5. [تهيئة](https://docs.microsoft.com/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) متغير لتخزين حالة تخزين طلب **ExportToPackage**.

    ![تهيئة إجراء متغير](media/integration-logic-app-initialize-variable-step.png)

6. انتظر حتى يتم **نجاح** تنفيذ حالة تصدير البيانات.

    1. إضافة [حلقة حتى](https://docs.microsoft.com/azure/logic-apps/logic-apps-control-flow-loops#until-loop) تتكرر حتى تصبح قيمة متغير **ExecutionStatus** هي **تم بنجاح**.
    2. قم بإضافة إجراء **تأخير** ينتظر خمس ثوان قبل القيام بالاستقصاء لحالة التنفيذ الحالية للتصدير.

        ![حاوية حلقة حتى](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > قم بتعيين عدد الحد إلى **15** للانتظار لمدة 75 ثانية بحد أقصى (15 تكرار * 5 ثواني) حتى اكتمال التصدير. إذا استغرقت عملية التصدير وقتًا إضافيًا، فقم بتعديل عدد الحد على النحو المناسب.        

    3. أضف إجراء **استدعاء طلب HTTP** لاستدعاء واجهة برمجية التطبيق REST لحزمة DMF [GetExecutionSummaryStatue](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) ، وتعيين متغير **ExecutionStatue** إلى نتيجة استجابة **GetExecutionSummaryStatus** 

        > لا يقوم هذا النموذج بالتحقق من الأخطاء. يُمكن أن تُرجع واجهة برمجة تطبيق **GetExecutionSummaryStatus‎** الحالات الطرفية غير الناجحة (أي، الحالات الأخرى بخلاف **تم بنجاح**). لمزيد من المعلومات، راجع [وثائق API](../dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).

        - **الأسلوب:** POST
        - **عنوان URL للطلب:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus
        - **نص الطلب:** body('Invoke\_an\_HTTP\_request')?['value']

            > [!NOTE]
            > قد تحتاج إلى إدخال قيمة **نص الطلب** إما في طريقة عرض الكود أو في مُحرر الوظيفة في المصمم.

        ![استدعاء إجراء طلب HTTP 2](media/integration-logic-app-get-execution-status-step.png)

        ![تعيين الإجراء المتغير](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > سوف تختلف القيمة للإجراء **تعيين المتغير** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) عن القيمة لقيمة نص **استدعاء طلب HTTP 2** حتى لو كان المصمم سوف يعرض القيم بالطريقة نفسها.

7. الحصول على عنوان URL للتنزيل للحزمة المُصدرة.

    - قم بإضافة إجراء **استدعاء طلب HTTP** لاستدعاء واجهة برمجة تطبيقات DMF REST [GetExportedPackageUrl](../dev-itpro/data-entities/data-management-api.md#getexportedpackageurl).

        - **الأسلوب:** POST
        - **عنوان URL للطلب:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl
        - **نص الطلب:** {"executionId": body('GetExportedPackageURL')?['value']}

        ![إجراء GetExportedPackageURL ](media/integration-logic-app-get-exported-package-step.png)

8. تنزيل الحزمة المُصدرة.

    - ثم بإضافة طلب HTTP لـ **GET** ([إجراء موصل HTTP](https://docs.microsoft.com/azure/connectors/connectors-native-http) مضمن) لتنزيل الحزمة من عنوان URL الذي تم إرجاعه في الخطوة السابقة.

        - **الأسلوب:** GET
        - **عنوان URL:** body('Invoke\_an\_HTTP\_request\_3').value

            > [!NOTE]
            > قد تحتاج إلى إدخال قيمة **عنوان URL** إما في طريقة عرض الكود أو في مُحرر الوظيفة في المصمم.

        ![إجراء HTTP GET](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > لا يتطلب هذا الطلب أي مصادقة إضافية، لأن عنوان URL الذي تقوم واجهة برمجة التطبيقات **GetExportedPackageUrl‎** بإرجاعه يتضمن الرمز المميز لتوقيعات الوصول المشترك الذي يمنح الوصول لتنزيل الملف.

9. احفظ الحزمة التي تم تنزيلها باستخدام موصل [OneDrive for Business](https://docs.microsoft.com/azure/connectors/connectors-create-api-onedriveforbusiness).

    - إضافة إجراء OneDrive For Business[إنشاء ملف](https://docs.microsoft.com/connectors/onedriveforbusinessconnector/#create-file).
    - قم بالتوصيل إلى حساب OneDrive for Business الخاص بك، حسب الحاجة.

        - **مسار المجلد:** مجلد من اختيارك
        - **اسم الملف:** worker\_package.zip
        - **محتوى الملف:** النص من الخطوة السابقة (محتوى ديناميكي)

        ![إنشاء إجراء ملف](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a>الخطوة 3: اختبار تطبيق logic

لاختبار تطبيق logic الخاص بك، حدد زر **تشغيل** في المصمم. سوف ترى أن خطوات تطبيق logic بدأت في التشغيل. بعد 30 إلى 40 ثانية، يجب أن ينهي تطبيق logic التشغيل، وينبغي أن يتضمن مجلد OneDrive for Business ملف حزمة جديد يحتوي على العاملين المُصدرين.

في حالة الإبلاغ عن فشل أي خطوة، حدد الخطوة الفاشلة في المصمم، وتحقق من حقول **الإدخالات** و **الاخراجات** الخاصة بها. قم بالتصحيح وعدّل الخطوة حسب الحاجة لتصحيح الأخطاء.

يُبين الرسم التوضيحي التالي كيف يبدو Logic Apps Designer عندما يتم تشغيل كافة خطوات تطبيق logic بنجاح.

![تشغيل تطبيق logic بنجاح](media/integration-logic-app-successful-run.png)

## <a name="summary"></a>ملخص

في هذا البرنامج التعليمي، تعلمنا كيفية استخدام تطبيق logic لتصدير البيانات من Human Resources وحفظ البيانات المُصدرة إلى مُجلد OneDrive for Business. يمكنك تعديل خطوات هذا البرنامج التعليمي حسب الحاجة ليناسب احتياجات الأعمال الخاصة بك.




[!INCLUDE[footer-include](../includes/footer-banner.md)]