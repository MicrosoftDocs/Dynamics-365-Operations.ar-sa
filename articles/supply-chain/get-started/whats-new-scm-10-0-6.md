---
title: ما الجديد أو المتغير في الإصدار 10.0.6 من Dynamics 365 Supply Chain Management (نوفمبر 2019)
description: يصف هذا الموضوع الميزات الجديدة أو المتغيرة في الإصدار 10.0.6 من Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac1
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 319ba09184c087a194b664ca87076d57c6ba0c66
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201538"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>ما الجديد أو المتغير في الإصدار 10.0.6 من Dynamics 365 Supply Chain Management (نوفمبر 2019)

[!include [banner](../includes/banner.md)]

يصف هذا الموضوع الميزات الجديدة أو المتغيرة في الإصدار 10.0.6 من Microsoft Dynamics 365 Supply Chain Management. رقم بنية هذا الإصدار هو 10.0.234، وهو يتوفر كما يلي: بينما يقع تاريخ التوفر العام في نوفمبر، تكون الميزات الجديدة متوفرة للإصدار المبكر في أكتوبر. لمزيد من المعلومات حول الإصدار 10.0.6، راجع [موارد إضافية](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>كيان البيانات V2 لنماذج تكوين المنتجات

تم إطلاق الإصدار الثاني لكيان البيانات "نماذج تكوين المنتجات" (يسمى "نماذج تكوين المنتجات V2"). كما يجب أن يكون القالب الافتراضي "418-نماذج تكوين المنتجات" موجودًا بحيث يستخدم كيان البيانات الجديد "نماذج تكوين المنتج V2" في قوالب إطار العمل "استيراد/تصدير". لن يتم تحديث القالب تلقائيًا بحيث يمكنك تحميل القالب من الافتراضي يدويًا. ويقوم الكيان V2 بتصدير صف واحد كملف منفصل في مرفق بدلاً من تضمينه، لحل القيود على حجم كيان V1. 
 
ما الذي تحتاج إلى فعله للقيام بهذا التغيير؟
-    بمجرد إهمال الكيان V1، يجب البدء بالترحيل من V1 إلى V2. في حالة استخدام القالب "418-نماذج تكوين المنتج"، يمكنك النقر فوق الزر "تحميل القوالب الافتراضية" وإعادة تحميل القالب "418-نماذج تكوين المنتجات"
-    إذا كنت بحاجة إلى الاحتفاظ بالتوافق مع الأنظمة الموجودة، فيمكنك الآن متابعة استخدام القالب الموجود والكيان V1 (المهمل) حتى تقوم بنقل عمليات التكامل الخاصة بك إلى القالب الجديد. 

## <a name="feature-management-enhancements"></a>عمليات تحسين إدارة الميزات
تسمح إدارة الميزات الآن بتمكين كافة الميزات الجديدة افتراضيًا، وتتطلب التأكيد لتمكين ميزة ما، وتمكين كافة الميزات التي لم يتم تمكينها بالفعل. 


## <a name="purchase-agreement-responsible-party"></a>الطرف المسؤول عن اتفاقية الشراء
تتوفر لديك الآن القدرة على تحديد الجهات المسؤولة الأساسية والثانوية في نموذج تصنيف اتفاقية الشراء واتفاقيات الشراء الناتجة.  وهذا يوفر للمستخدم حق الوصول إلى الشخص الذي قام بالإشراف على الاتفاقيات.

## <a name="rfq-link-on-the-purchase-order-line"></a>ارتباط RFQ على سطر أمر الشراء
يمكنك إضافة ارتباط مرجعي من بنود أمر الشراء للرجوع إلى بنود RFQ المقابلة التي تم إنشاؤها منها، مما يسمح بسهولة بتوفير دعم مستند طلب عرض الأسعار للمستخدم.

## <a name="additional-resources"></a>الموارد الإضافية

### <a name="bug-fixes"></a>إصلاح الأخطاء
للحصول على معلومات حول إصلاحات الأخطاء المضمنة في كل تحديث من التحديثات التي تعد جزءًا من 10.0.6، قم بتسجيل الدخول إلى Lifecycle Services (LCS) وعرض [مقالة قاعدة المعارف](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>update 30 للنظام الأساسي
يتضمن Microsoft Dynamics 365 Supply Chain Management 10.0.6 التحديث Platform update 30. لمعرفة المزيد حول Platform update 30، راجع [ما الجديد أو المتغير في Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: خطة الموجة 2 لإصدار 2019
هل تتساءل عن الإمكانات القادمة والتي تم إصدارها حديثًا في أيٍّ من تطبيقات العمل أو النظام الأساسي الخاص بنا؟

راجع [Dynamics 365: خطة الموجة 2 لإصدار 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/). لقد التقطنا جميع التفاصيل بشكل شامل، ومن الأعلى إلى الأسفل، في مستند واحد يمكنك استخدامه للتخطيط.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>ميزات Supply Chain Management التي تمت ازالتها وإهمالها

يوضح الموضوع [الميزات التي تمت ازالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) الميزات التي تمت أو تتم جدولتها لإزالتها أو إهمالها لـ Supply Chain Management.

- لم تعد ميزة *تمت الإزالة* متوفرة في المنتج.
- لا توجد ميزة *المهملة* في التطوير النشط وقد يتم إزالتها في تحديثات مستقبلية.

قبل إزالة أي ميزة من المنتج، سيتم إعلان إشعار إهمال في الموضوع [الميزات التي تمت إزالتها أو إهمالها في Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 شهرًا قبل الإزالة.

بالنسبة للتغييرات الفاصلة التي تؤثر فقط على وقت التحويل البرمجي، ولكنها متوافقة ثنائيًا مع بيئة الاختبار المعزولة وبيئات الإنتاج، فسيكون وقت الإهلاك أقل من 12 شهرًا. بشكل عام، هذه هي التحديثات الوظيفية التي يجب إجراؤها للمحول البرمجي.
