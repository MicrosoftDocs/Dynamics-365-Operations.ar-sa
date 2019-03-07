---
title: تكامل عميل Microsoft Project
description: التخطيط والاحتفاظ بجدول مشروع يمكن أن يكون معقدًا، لأن مديرو المشاريع بحاجة إلى استخدام الأدوات التي تساعدهم في إدارة هذه المهمة. يوفر التكامل مع عميل Microsoft Project الدعم لفتح وإدارة هيكل تنظيم عمل مشروع.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 48feb0182c623714b2acffafc42016c0471ba6c1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "317466"
---
# <a name="microsoft-project-client-integration"></a>تكامل عميل Microsoft Project

[!include [banner](../includes/banner.md)]

التخطيط والاحتفاظ بجدول مشروع يمكن أن يكون معقدًا، لأن مديرو المشاريع بحاجة إلى استخدام الأدوات التي تساعدهم في إدارة هذه المهمة. يوفر التكامل مع عميل Microsoft Project الدعم لفتح وإدارة هيكل تنظيم عمل مشروع. يستطيع مدير المشروع نشر أي تغييرات مرة أخرى إلى هيكل تنظيم عمل مشروع Finance and Operations.

> [!NOTE]
> إذا كنت تستخدم تحديث شهر يوليو لتطبيق Microsoft Dynamics 365 for Finance and Operations، فيجب تثبيت KB 4054797 و4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>تكوين الأداة الإضافية لعميل Microsoft Project
لتمكين التكامل مع عميل Microsoft Project، يلزم تثبيت الأداة الإضافية لـ Microsoft Dynamics 365 في تطبيق عميل Microsoft Project للمستخدم. يتم ذلك عن طريق فتح **مساحة عمل إدارة المشروع**.

•   انقر فوق **تكوين الأداة الإضافية لعميل المشروع** من قسم **الارتباطات** > **الإعداد** في مساحة العمل.

•   انقر فوق **فتح**، ثم انقر فوق **تشغيل** عند مطالبتك بذلك.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>فتح وتحرير مسودة هيكل تنظيم عمل موجودة في عميل Microsoft Project
إذا تم إنشاء هيكل تنظيم عمل لمشروع Finance and Operations بالفعل، يمكن فتح هيكل تنظيم العمل في تطبيق عميل Microsoft Project إذا كان هيكل تنظيم العمل بحالة مسودة. لفتحه من صفحة **المشروع**، انقر فوق الارتباط **فتح في Microsoft Project** من علامة التبويب **تخطيط**. يمكن أيضًا فتح هذه الصفحة من داخل تطبيق عميل Microsoft Project بالنقر فوق **فتح** على علامة التبويب **Microsoft Dynamics 365**. حدد **الكيان القانوني** و**المشروع‏‎** من القائمة.

> [!NOTE]
> إذا كنت تستخدم Internet Explorer كمستعرض، فستحتاج إلى النقر فوق **حفظ** للفتح يدويًا من الموقع الذي تم تنزيل الملف في. أو، انقر فوق **حفظ وفتح** لفتح الملف في عميل Microsoft Project. لا تعيد تسمية اسم الملف عند الحفظ.

قبل إجراء أي عمليات تحرير على الملف باستخدام عميل Microsoft Project، تحتاج إلى سحبه. انقر فوق **سحب** على علامة التبويب **Microsoft Dynamics 365**. سيؤدي ذلك إلى منع المستخدمين الآخرين من تحرير هيكل تنظيم العمل من داخل Finance and Operations في الوقت نفسه. لنشر هيكل تنظيم العمل بعد إتمام أي عمليات تحرير، انقر فوق **إيداع‏‎** على علامة التبويب **Microsoft Dynamics 365**.

إذا تمت بالفعل إضافة فريق مشروع للمشروع في Finance and Operations، فسيتم ملء قائمة الموارد بأعضاء الفريق. في حال عدم إضافة فريق المشروع إلى المشروع حتى الآن، فيمكنك تحديد الموارد وإنشاء الفريق في عميل Microsoft Project عن طريق النقر فوق الزر **الموارد** على علامة التبويب **Microsoft Dynamics 365**. 

ستتم مزامنة البيانات التالية مرة أخرى مع Finance and Operations كجزء من عملية الإيداع:

•   اسم المهمة

•   تاريخ البدء

•   تاريخ الانتهاء

•   العناصر السابقة

•   أسماء الموارد

•   الفئة

•   فئة المورد

•   ساعات العمل

•   الملاحظات

•   الأولوية

> [!NOTE]
> إذا قمت بإضافة أي أعمدة أخرى إلى ملف عميل Microsoft Project، فلن يتم حفظ للملف ولن يتم عرضه عند فتح الملف مرة أخرى.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>إنشاء هيكل تنظيم العمل لمشروع موجود باستخدام عميل Microsoft Project
لإنشاء هيكل تنظيم عمل جديد باستخدام عميل Microsoft Project، اتبع الخطوات التالية:


1.  افتح عميل Microsoft Project.

2.  على علامة التبويب **Microsoft Dynamics 365**، انقر فوق **فتح**.

3.  حدد **الكيان القانوني** للمشروع.

4.  حدد **المشروع**.

5.  انقر فوق **سحب** على علامة التبويب **Microsoft Dynamics 365**.

6.  عندما تصبح جاهزًا للنشر في Finance and Operations، انقر فوق **إيداع‏‎** على علامة التبويب **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>استبدال هيكل تنظيم العمل لمشروع موجود باستخدام عميل Microsoft Project
لإنشاء هيكل تنظيم عمل جديد باستخدام عميل Microsoft Project واستبدال هيكل تنظيم عمل موجود لمشروع موجود، اتبع الخطوات التالية:

1.  افتح عميل Microsoft Project.

2.  أنشئ الجدول في عميل Microsoft Project.

3.  على علامة التبويب **Microsoft Dynamics 365**، انقر فوق **حفظ التغييرات** > **استبدال مشروع موجود**.

4.  حدد **الكيان القانوني** للمشروع.

5.  حدد **المشروع**.

6.  وانقر فوق **موافق**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>إنشاء مشروع جديد من داخل عميل Microsoft Project


1.  افتح عميل Microsoft Project.

2.  أنشئ الجدول في عميل Microsoft Project.

3.  على علامة التبويب **Microsoft Dynamics 365**، انقر فوق **حفظ التغييرات** > **حفظ إلى مشروع جديد**.

4.  حدد **الكيان القانوني** للمشروع.

5.  قم بإدخال **معرف المشروع**، إذا لزم الأمر.

6.  أدخل **اسم المشروع**.

7.  حدد **نوع المشروع** و**مجموعة المشروع** و**معرف عقد المشروع**. بدلاً من ذلك، يمكنك إنشاء عقد مشروع جديد بالنقر فوق **جديد**.

8.  حدد **التقويم** المُراد استخدامه لإدارة الموارد.

11. وانقر فوق **موافق**.
