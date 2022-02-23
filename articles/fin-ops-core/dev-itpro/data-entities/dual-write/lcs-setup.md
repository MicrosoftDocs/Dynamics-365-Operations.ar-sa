---
title: إعداد الكتابة المزدوجة من Lifecycle Services
description: يشرح هذا الموضوع كيفية إعداد اتصال كتابة مزدوجة بين بيئة Finance and Operations جديدة وبيئة Dataverse جديدة من Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683513"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>إعداد الكتابة المزدوجة من Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يشرح هذا الموضوع كيفية إعداد اتصال كتابة مزدوجة بين بيئة Finance and Operations جديدة وبيئة Dataverse جديدة من Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب أن تكون مسؤولاً لإعداد اتصال كتابة مزدوجة.

+ يجب أن يكون لديك حق الوصول إلى المستأجر.
+ يجب أن تكون مسؤولاً في بيئات Finance and Operations وبيئات Dataverse.

## <a name="set-up-a-dual-write-connection"></a>إعداد اتصال كتابة مزدوجة

اتبع هذه الخطوات لإعداد اتصال الكتابة المزدوجة.

1. في LCS، انتقل إلى المشروع..
2. حدد **تكوين** لنشر بيئة جديدة.
3. حدد الإصدار. 
4. حدد المخطط. إذا توفر مخطط واحد فقط، فسيتم تحديده بشكل تلقائي.
5. أكمل الخطوات الأولى في معالج **إعدادات النشر**.
6. على علامة التبويب **Dataverse**، اتبع إحدى الخطوات التالية:

    - إذا تم تزويد بيئة Dataverse للمستأجر، فيمكنك تحديدها.

        1. عيّن الخيار **تكوين Dataverse** إلى **نعم**.
        2. في حقل **البيئات المتوفرة**، حدد البيئة التي تريد دمجها مع بيانات Finance and Operations. تتضمن القائمة كافة البيئات حيث تملك امتيازات إدارية.
        3. حدد خانة الاختيار **أوافق** للإشارة إلى موافقتك على الأحكام والشروط.

        ![علامة التبويب Dataverse عند تزويد بيئة Dataverse للمستأجر](../dual-write/media/lcs_setup_1.png)

    - إذا لم تتوفر بيئة Dataverse لدى المستأجر، فسيتم تزويد بيئة.

        1. عيّن الخيار **تكوين Dataverse** إلى **نعم**.
        2. أدخل اسمًا لبيئة Dataverse.
        3. حدد المنطقة لنشر البيئة فيها.
        4. حدد لغة البيئة وعملتها الافتراضية.

            > [!NOTE]
            > لا يمكنك تغيير اللغة والعملة لاحقًا.

        5. حدد خانة الاختيار **أوافق** للإشارة إلى موافقتك على الأحكام والشروط.

        ![علامة التبويب Dataverse عندما لا تتوفر بيئة Dataverse لدى المستأجر](../dual-write/media/lcs_setup_2.png)

7. أكمل الخطوات المتبقية في معالج **إعدادات النشر**.
8. بعد ان تصبح حالة البيئة **منشورة**، افتح صفحة تفاصيل البيئة. يعرض القسم **معلومات بيئة Dataverse** أسماء بيئة Finance and Operations وبيئة Dataverse المرتبطتين.

    ![قسم معلومات بيئة Dataverse](../dual-write/media/lcs_setup_3.png)

9. يجب أن يقوم مسؤول بيئة Finance and Operations بتسجيل الدخول إلى LCS وتحديد **ارتباط إلى CDS للتطبيقات** لإكمال الارتباط. تعرض صفحة تفاصيل البيئة معلومات الاتصال بالمسؤول.

    بعد إكمال الارتباط، يتم تحديث الحالة إلى **إكمال ربط البيئة بنجاح**.

10. لفتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations والتحكم في القوالب المتوفرة، حدد **ارتباط إلى CDS للتطبيقات**.

    ![الزر "ارتباط إلى CDS للتطبيقات" في قسم معلومات بيئة Dataverse](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> لا يمكنك إلغاء ارتباط البيئات باستخدام LCS. لإلغاء ارتباط بيئة، افتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations، ثم حدد **إلغاء الارتباط**.
