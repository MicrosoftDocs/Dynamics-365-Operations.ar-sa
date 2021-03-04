---
title: مشاركة تكوينات ER في RCS/المستودع العمومي مع المؤسسات الخارجية
description: يشرح هذه الموضوع كيفية مشاركة تكوينات التقارير الإلكترونية (ER) في خدمات Microsoft Regulatory Configuration Services (RCS)/المستودع العمومي مباشرة مع مؤسسات خارجية.
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
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
ms.openlocfilehash: 04c46824123906eccbfff18a03974c8043729e0a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440008"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a>مشاركة تكوينات التقارير الإلكترونية (ER) في خدمات Regulatory Configuration Services (RCS)/المستودع العمومي مع مؤسسات خارجية.

[!include [banner](../includes/banner.md)]

يمكنك استخدام خدمات Microsoft Regulatory Configuration Services (RCS) لمشاركة تكوينات التقارير الإلكترونية (ER) ثم نشرها إلى مؤسسات خارجية.

توضح الإجراءات التالية كيف يمكن لمستخدم RCS مشاركه إصدار من تكوين ER الذي تم تكوينه في مثيل RCS مع مؤسسة خارجية. قبل إكمال هذه الإجراءات، يجب أن تستكمل أولا المتطلبات الأساسية التالية:

- الوصول إلى مثيل RCS.
- إنشاء موفر تكوين نشط. لمزيد من المعلومات، راجع [إنشاء موفري التكوين ووضع علامة عليهم كنشطين](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
- إنشاء إصدار جديد من تكوين ER وتحميله. لمزيد من المعلومات، راجع [إنشاء إصدار جديد من تكوين التقارير الإلكترونية (ER) وتحميله](rcs-global-repo-upload.md).

يجب أيضا التأكد من أنه تم توفير بيئة RCS لشركك.

1. في تطبيق Finance and Operations، انتقل إلى **إدارة المؤسسات** \> **مساحات العمل** \> **التقارير الإلكترونية**.
2. في حالة عدم توفير بيئة RCS للشركة الخاصة بك، حدد **Regulatory services - التكوين الخارجي**، واتبع الإرشادات لتوفير بيئة.

إذا تم بالفعل توفير بيئة RCS لشركك، استخدم عنوان URL للصفحة للوصول إليه عن طريق تحديد خيار تسجيل الدخول.

## <a name="verify-the-configuration-that-you-want-to-share"></a>التحقق من التكوين الذي تريد مشاركته

اتبع الخطوات التالية للتحقق من تحميل التكوين الذي ترغب في مشاركته بالفعل إلى المستودع العمومي.

1. في مساحة عمل **التقارير الإلكترونية**، حدد **المستودعات** الخاصة بموفر التكوين.

    ![موفرو التكوين](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_config_provider.JPG)

2. حدد **المستودع االعمومي** \> **فتح**.
3. ابحث عن التكوين الذي تريد مشاركته. يمكن استخدام حقل عامل التصفية لتضييق البحث. إذا لم تتمكن من العثور على التكوين في المستودع العمومي، فاتبع الخطوات الواردة في [إنشاء إصدار جديد من تكوين التقارير الإلكترونية (ER) وتحميله](rcs-global-repo-upload.md).

## <a name="share-er-configurations-with-external-organizations"></a>مشاركة تكوينات ER مع المؤسسات الخارجية

بعد إنشاء تكوين تحت موفر التكوين الخاص بك، يمكنك مشاركته مباشرة مع المؤسسات الخارجية باستخدام علامة التبويب السريعة **مشاركة مع** في صفحة **مستودع التكوين العمومي**.

1. في مساحة عمل **التقارير الإلكترونية**، حدد **المستودعات** الخاصة بموفر التكوين.
2. حدد **المستودع االعمومي** \> **فتح**. 
3. تحديد التكوين الذي تريد مشاركته
4. في علامة التبويب السريعة **مشاركة مع**، حدد **المؤسسة**.

    ![علامة التبويب السريعة مشاركة مع](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_org.JPG)

5. في مربع الحوار، أدخل اسم المجال للمؤسسة الخارجية، ثم حدد **موافق**.

    ![مربع الحوار "مشاركة إصدار التكوين مع مؤسسة خارجية"](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_form.JPG)

تتم مشاركة التكوين مع المؤسسة الخارجية ويكون متوفرا لهذه المؤسسة في المستودع العمومي. ومن هناك، يمكن استيرادها إلى مثيل المؤسسة لـ RCS أو إلى مثيلات تطبيقات Finance and Operations.

![مشاركة التكوين مع مؤسسة خارجية](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/Janeaug_RCSdocs/articles/finance/localizations/media/1_RCS_Repo_for_Share_with_test.com)

6. لإلغاء مشاركة تكوين تمت مشاركته مسبقًا مع مؤسسة خارجية، حدد التكوين وانقر فوق **إلغاء المشاركة**، ثم حدد **موافق**


[!INCLUDE[footer-include](../../includes/footer-banner.md)]