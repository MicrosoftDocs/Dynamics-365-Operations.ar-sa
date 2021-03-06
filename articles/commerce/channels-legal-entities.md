---
title: إنشاء كيانات قانونية
description: يصف هذا الموضوع كيفية إنشاء كيانات قانونيه في Microsoft Dynamics 365 Commerce، يجب إنشاؤها وتكوينها قبل إنشاء القنوات.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 9491feb004366a02155225bfb323773e130f3dc9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993593"
---
# <a name="create-legal-entities"></a>إنشاء كيانات قانونية


[!include [banner](includes/banner.md)]

يصف هذا الموضوع كيفية إنشاء كيانات قانونيه في Microsoft Dynamics 365 Commerce، يجب إنشاؤها وتكوينها قبل إنشاء القنوات.

## <a name="overview"></a>نظرة عامة

الكيان القانوني هو مؤسسة لديها هيكل قانوني مسجَّل أو مشرَّع. يمكن إدخال الكيانات القانونية في العقود القانونية ويجب عليها إعداد كشوف حساب تقوم بالإبلاغ عن أدائها.

الشركة هي نوع من الكيانات القانونية. وفي الوقت الحالي، تعتبر الشركات النوع الوحيد من الكيانات القانونية التي يمكنك إنشاؤها، ويقترن كل كيان قانوني بمعرّف شركة. يوجد هذا الاقتران لأن بعض المناطق الوظيفية في البرنامج تستخدم معرف شركة أو *DataAreaId*، في نماذج بياناتها. في هذه المجالات الوظيفية، تستخدم الشركات كحد لأمن البيانات. يمكن للمستخدمين الوصول إلى البيانات فقط للشركة التي قاموا حاليًا بتسجيل الدخول إليها. 

عند إنشاء قناة، يجب تحديد الكيان القانوني الذي تنتمي اليه القناة.

## <a name="create-a-new-legal-entity"></a>إنشاء كيان قانوني جديد

لإنشاء كيان قانوني جديد في Dynamics 365 Commerce، اتبع هذه الخطوات:

1. في جزء التنقل، انتقل إلى  **الوحدات \> إعداد المراكز الرئيسية ‬ \> الكيانات القانونية**.
1. في جزء الإجراءات، حدد **جديد**. يظهر الجزء **كيان قانوني جديد** إلى اليسار.
1. في حقل **الاسم**، أدخل قيمة.
1. أدخل قيمة في حقل **الشركة**.
1. في الحقل **البلد/المنطقة**، أدخل قيمة أو حددها.
1. حدد **موافق**. 

   ![إنشاء كيان قانوني](media/legal-entities.png)

1. في القسم **عام**، أدخل المعلومات العامة التالية حول الكيان القانوني: 
   1. أدخل اسم بحث، إذا كان إدخال اسم البحث مطلوبًا. اسم البحث هو اسم بديل يمكن استخدامه للبحث عن هذا الكيان القانوني. 
   1. حدد ما إذا كان يتم استخدام هذا الكيان القانوني كشركة توحيد أم لا.
   1. حدد ما إذا كان يتم استخدام هذا الكيان القانوني كشركة استبعاد أم لا. 
   1. حدد **اللغة الافتراضية** للكيان. 
   1. حدد **المنطقة الزمنية** للكيان.
1. في قسم **العناوين**، حدد **تحرير** لإدخال معلومات العنوان، مثل اسم الشارع ورقمه والرمز البريدي والمدينة.
1. في القسم **معلومات جهة الاتصال**، أدخل معلومات أساليب الاتصال، مثل عناوين البريد الإلكتروني وعناوين URL وأرقام الهاتف.
1. في القسم **إعداد التقارير التشريعية**، أدخل أرقام التسجيل التي يتم استخدامها لإعداد التقارير التشريعية.
1. في القسم **أرقام التسجيل**، أدخل أي معلومات مطلوبة من قبل الكيان القانوني.
1. في المقطع **معلومات الحساب البنكي**، أدخل الحسابات البنكية وأرقام التوجيه الخاصة بالكيان القانوني.
1. في قسم **التجارة الخارجية واللوجستيات**، أدخل معلومات الشحن الخاصة بالكيان القانوني.
1. في القسم **التسلسلات الرقمية**، يمكنك عرض التسلسلات الرقمية المقترنة بالكيان القانوني. سيكون هذا فارغًا عند البدء.
1. في قسم **صورة لوحة المعلومات**، قم بتغيير أو عرض صورة الشعار وصورة لوحة المعلومات المرتبطة بالكيان القانوني.
1. في القسم **التسجيل الضريبي**، أدخل أرقام التسجيل التي يتم استخدامها لإبلاغ هيئات الضرائب.
1. في القسم **ضريبة 1099**، أدخل معلومات ضريبة 1099 للكيان القانوني.
1. في قسم **معلومات الضريبة**، أدخل معلومات الضريبة للكيان القانوني.
1. حدد **حفظ**.

تعرض الصورة التالية تفاصيل مثال عن كيان قانوني.

![القسم العام للكيان القانوني](media/legal-entities-general.png)
   
## <a name="additional-resources"></a>الموارد الإضافية

[نظرة عامة المؤسسات والتدرجات الهرمية للمؤسسات](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[تخطيط التدرج الهرمي للمؤسسات](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[التدرجات الهرمية للمؤسسات](channels-org-hierarchies.md)

[نظرة عامة على القنوات](channels-overview.md)

[المتطلبات الأساسية‬ لإعداد قناة](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]