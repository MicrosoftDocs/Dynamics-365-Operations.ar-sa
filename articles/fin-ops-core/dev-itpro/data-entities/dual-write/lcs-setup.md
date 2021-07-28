---
title: إعداد الكتابة المزدوجة من Lifecycle Services
description: يوضح هذا الموضوع كيفيه اعداد اتصال ثنائي الكتابة من Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e604e1491bbafa041fa3f52ad0f8b454c63d47de
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359353"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>إعداد الكتابة المزدوجة من Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

يوضح هذا الموضوع كيفية تمكين الكتابة المزدوجة من Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>المتطلبات الأساسية

يجب إكمال تكامل Power Platform كما هو موضح في الموضوعات التالية:

+ [Power Platform التكامل - التمكين أثناء نشر البيئة](../../power-platform/overview.md#enable-during-environment-deployment)
+ [Power Platform التكامل - الإعداد بعد نشر البيئة](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a>إعداد الكتابة المزدوجة لبيئات Dataverse الجديدة

اتبع هذه الخطوات لإعداد الكتابة المزدوجة من الصفحة **تفاصيل بيئة** LCS:

1. في الصفحة **تفاصيل البيئة**، قم بتوسيع القسم **تكامل Power Platform**.

2. حدد الزر **تطبيق الكتابة المزدوجة**.

    ![تكامل Power Platform.](media/powerplat_integration_step2.png)

3. راجع البنود والشروط، ثم حدد **تكوين**.

4. حدد **موافق** للمتابعة.

5. يمكنك مراقبة التقدم عن طريق تحديث صفحة تفاصيل البيئة بشكل دوري. يستغرق الإعداد عادة 30 دقيقة أو أقل.  

6. عند اكتمال الإعداد، تقوم رسالة بإعلامك في حالة نجاح العملية أو إذا فشلت. وفي حالة فشل الإعداد، يتم عرض رسالة خطأ مرتبطة. يجب إصلاح أية أخطاء قبل الانتقال إلى الخطوة التالية.

7. حدد **ارتباط إلى بيئة Power Platform** لإنشاء ارتباط بين Dataverse وقواعد البيانات الحالية الخاصة بالبيئة. يستغرق هذا عادة أقل من 5 دقائق.

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="الربط ببيئة Power Platform .":::

8. عند اكتمال الارتباط، يتم عرض ارتباط تشعبي. استخدم الارتباط لتسجيل الدخول إلى منطقة إدارة الكتابة المزدوجة في البيئة Finance and Operations. ومن هناك، يمكنك إعداد تعيينات الكيانات.

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a>إعداد الكتابة المزدوجة لبيئة Dataverse موجودة

لإعداد الكتابة الزدوجة لبيئة Dataverse موجودة، يجب عليك إنشاء [بطاقة دعم Microsoft](../../lifecycle-services/lcs-support.md). يجب أن تتضمن التذكرة:

+ معرف بيئة Finance and Operations الخاص بك.
+ اسم البيئة الخاصة بك من Lifecycle Services.
+ معرف مؤسسة Dataverse أو معرف بيئة Power Platform من مركز مسؤول Power Platform. في البطاقة الخاصة بك، اطلب أن يكون المُعرف هو المثيل المستخدم لتكامل Power Platform.

> [!NOTE]
> لا يمكنك إلغاء ارتباط البيئات باستخدام LCS. لإلغاء ارتباط بيئة، افتح مساحة عمل **تكامل البيانات** في بيئة Finance and Operations، ثم حدد **إلغاء الارتباط**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
