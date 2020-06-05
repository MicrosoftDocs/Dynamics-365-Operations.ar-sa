---
title: إنشاء تكوينات ER في RCS وتحميلها إلى المستودع العمومي
description: يشرح هذه الموضوع كيفية إنشاء تكوين التقارير الإلكترونية (ER) في خدمات Microsoft Regulatory Configuration Services (RCS) وتحميلها إلى المستودع العمومي.
author: JaneA07
manager: AnnBe
ms.date: 05/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 0e194a8b777f984412d81e315f92ab4bb8a3b0c9
ms.sourcegitcommit: 204cec8ca2a6c4474d21dbcd408e369131a47856
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/13/2020
ms.locfileid: "3371229"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a>إنشاء تكوينات ER في Regulatory Configuration Services (RCS) وتحميلها إلى المستودع العمومي

[!include [banner](../includes/banner.md)]

يمكنك استخدام خدمات Microsoft Regulatory Configuration Services (RCS) لتصميم تكوينات التقارير الإلكترونية (ER) ثم نشرها بحيث يمكن استخدامها في المؤسسة الخاصة بك.

توضح الإجراءات التالية كيفية قيام مستخدم بدور مسؤول النظام أو مطور التقارير الإلكترونية بإنشاء إصدار مشتق من تكوين ER تم تكوينه في مثيل RCS، ثم تحميل التكوين المشتق إلى المستودع العمومي. 

قبل إكمال هذه الإجراءات، يجب أن تستكمل أولا المتطلبات الأساسية التالية:

- الوصول إلى مثيل RCS.
- إنشاء موفر تكوين نشط. لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

يجب أيضا التأكد من أنه تم توفير بيئة RCS لشركك.

1. في تطبيق Finance and Operations، انتقل إلى **إدارة المؤسسات** \> **مساحات العمل** \> **التقارير الإلكترونية**.
2. في حالة عدم توفير بيئة RCS للشركة الخاصة بك، حدد **Regulatory services - التكوين الخارجي**، واتبع الإرشادات لتوفير بيئة.

إذا تم بالفعل توفير بيئة RCS لشركك، استخدم عنوان URL للصفحة للوصول إليه عن طريق تحديد خيار تسجيل الدخول.

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a>إنشاء إصدار مشتق من تكوين في RCS

1. في مساحة عمل **التقارير الإلكترونية**، تحقق من أن لديك موفر تكوين نشط لمؤسسك. 
2. حدد **تكوينات إعداد التقارير‬**.
3. حدد التكوين الذي ترغب في اشتقاق إصدار جديد منه. يمكن استخدام حقل عامل التصفية فو الشجرة لتضييق البحث.
4. حدد **إنشاء تكوين** \> **مشتق من الاسم**.
5. أدخل اسمًا ووصفًا، ثم حدد **إنشاء التكوين** لإنشاء إصدار مشتق جديد.
6. حدد التكوين المشتق حديثا، وأضف وصفًا للإصدار، ثم حدد **موافق**. يتم تغيير حالة التكوين إلى **مكتمل**.

![إصدار التكوين الجديد في RCS](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_CompleteConfig.JPG)

> [!NOTE]
> عند تغيير حالة التكوين، قد تستلم رسالة خطأ خاصة بالتحقق من الصحة تتعلق بالتطبيقات المتصلة. لإيقاف تشغيل التحقق من الصحة، في جزء الإجراءات في علامة التبويب **التكوينات**، حدد **معلمات المستخدم**، ثم قم بتعيين الخيار **تخطي التحقق من الصحة عند تغير حالة التكوين وتغير العنوان الأساسي** إلى **نعم** 

## <a name="upload-a-configuration-to-the-global-repository"></a>تحميل تكوين إلى المستودع العمومي

لمشاركه التكوين الجديد أو المشتق مع مؤسستك، يمكنك تحميله إلى المستودع العمومي.

1. حدد الإصدار المكتمل من التكوين، ثم حدد **تحميل إلى المستودع**.
2. حدد الخيار **عمومي (Microsoft)**، ثم حدد **تحميل**.

    ![خيارات التحميل إلى المستودع](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Upload_to_GlobalRepo_options.JPG)

3. في مربع رسالة التأكيد، حدد **نعم**. 
4. قم بتحديث وصف الإصدار كما هو مطلوب، ثم حدد **موافق**. 

يتم تحديث حالة التكوين إلى **مشاركة**، ويتم تحميل التكوين إلى المستودع العمومي. ومن هناك، يمكنك التعامل معه بالطرق التالية:

- استيراده إلى مثيل Dynamics 365 الخاص بك. لمزيد من المعلومات، راجع [ (ER)استيراد التكوينات من RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).
- مشاركته مع جهة خارجية أو مؤسسة خارجية، راجع [RCS مشاركة تكوينات التقارير الإلكترونية (ER) مع المؤسسات الخارجية](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/rcs-global-share-configuration.md)

![إصدار تكوين نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي لـ Contoso في المستودع العمومي](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/RCS_Config_upload_GlobalRepo.JPG)
