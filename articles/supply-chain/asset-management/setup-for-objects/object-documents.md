---
title: مستندات الأصل
description: يشرح هذا المقال مستندات الأصول في إدارة الأصول.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2e8d72dc938c43e266c6b7c39329f827c56607a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899458"
---
# <a name="asset-documents"></a>مستندات الأصل

[!include [banner](../../includes/banner.md)]

 

يشرح هذا المقال مستندات الأصول في إدارة الأصول.

في إدارة الأصول، يمكنك إعداد المستندات بحيث تكون مرتبطة تلقائيًا بأنواع الوظائف أو الشركات المصنعة للأصول أو أنواع الأصول أو الأصول، على سبيل المثال. تكون هذه الوظيفة مفيدة عند إصدار نسخ مستندات محدثة. وفي هذه الحالة، يجب عليك فقط وضع المستند المحدّث في الموقع القياسي الذي تستخدمه لمستندات Supply chain Management، وإرفاق المستند بسجل مستند الأصل الذي قمت بإنشائه. بعد ذلك، يمكن الوصول إلى المستند المحدث من بنود قائمة **كل الأصول** و **الأصول‏‎ النشطة** و **أصولي النشطة** و **جميع أوامر العمل** و **وظائف أوامر العمل النشطة**. تستخدم عملية إرفاق المستندات بسجل مستندات الأصول النظام القياسي للتعامل مع المستندات.

**مثال 1:** قد يصف مستند يرتبط بنوع وظيفة إجراءً لنوع الوظيفة هذا.

**مثال 2:** قد يكون مستند يرتبط بمجموعة من نوع أصل وشركة مصنعة ونموذج الدليل القياسي لنموذج الشركة المصنعة للأصل المحدد.

## <a name="create-asset-document-relation"></a>إنشاء علاقة مستندات الأصول

1. حدد **إدارة الأصول** \> **إعداد** \> **مستندات الأصول**.
2. حدد **جديد** لإنشاء سجل مستند الأصل.
3. وفقًا لمستوى التحديد المطلوب لعلاقة المستند، قم بإجراء تحديدات ذات صلة في حقل أو أكثر من الحقول التالية: **نوع الأصل** و **الشركة المصنعة** و **النموذج‏‎** و **الأصل‏‎** و **فئة نوع المهمة** و **نوع المهمة** و **متغير نوع المهمة** و **متطلبات المهمة‬**. تعتمد الخيارات المتوفرة في الحقلين **متغير نوع المهمة** و **متطلبات المهمة** على تحديدك في حقل **نوع المهمة**.

    > [!NOTE]
    > عندما يبحث النظام عن مستندات يجب أن تكون ذات صلة بأصل أو أمر عمل، تقوم "إدارة الأصول" بمراجعة كافة سجلات مستندات الأصول للتحقق من وجود تطابق محتمل. وهي تتحقق دائمًا من المجموعة الأكثر تحديدًا أولاً. وبعبارة أخرى، تقوم إدارة الأصول أولاً بالتحقق من تطابق في حقل **متطلبات المهمة** . إذا لم يتم العثور على تطابق، فهي تتحقق من وجود تطابق لحقل **متغير نوع المهمة**. إذا لم يتم العثور على تطابق، فهي تتحقق من وجود تطابق لحقل **نوع المهمة**. كما ترى في تخطيط الصفحة **مستندات الأصول**، يعني هذا السلوك أنه، للعثور على المجموعة الأكثر تحديدًا، تقوم إدارة الأصول بالتحقق من كل سجل من اليسار إلى اليمين للحصول على تطابق. قد تكون عدة مستندات ذات صلة بأصل أو أمر عمل. يمكنك تحرير مستوى الخدمة على طلب صيانة أو أمر عمل كما تحتاج.

4. حدد **المرفقات**. تظهر صفحة **مُعالجة المستندات** القياسية.
5. قم بإعداد المستندات أو الملاحظات التي يجب إرفاقها بسجل مستند الأصل. بعد إرفاق المستندات، يعرض حقل **المرفقات** عدد المستندات المرتبطة بالسجل.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]