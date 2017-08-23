---
title: "إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬"
description: "يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة."
author: aolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.2.0
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 05fd7ce5293b3a300aabc073a6e492c5804d1897
ms.contentlocale: ar-sa
ms.lasthandoff: 08/03/2017

---

# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬

[!include[banner](../includes/banner.md)]

يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة. تتضمن مساحة عمل المدير المالي علامة التبويب **نظرة عامة** وعلامة التبويب **مالي**. يتم إجراء نسخ احتياطي للتقارير على علامتي التبويب باستخدام مقياسين: LedgerActivityMeasure وBudgetActivityMeasure. في Microsoft Dynamics 365 for Finance and Operations, Enterprise edition تحديث يوليو 2017، توجد علاقة بين هذين المقياسين والكيان DimensionCombinationEntity. لذلك، يمكنك تحديد الأبعاد.

1. في Finance and Operations، في صفحة **متجر الكيانات**، قم بتحديث المقياسين **LedgerActivityMeasure**و**BudgetActivityMeasure**.
2. في Microsoft Visual Studio، افتح مستكشف التطبيق، وابحث عن **LedgerCFO**.
3. ضمن **الموارد**، افتح **LedgerCFOWorkspacePBIX‎**.
4. عندما يفتح المورد في Microsoft Power BI Desktop، حدد **الحصول على البيانات**، وحدد **قاعدة بيانات SQL Server**، ثم حدد **اتصال**.
5. أدخل اسم الخادم، ثم أدخل **AxDW** كقاعدة بيانات. حدد **DirectQuery**، ثم حدد **موافق**.
6. ابحث عن **LedgerActivityMeasure\_DimensionCombination** وحدده، ثم حدد **تحميل**.

    > [!TIP]
    > في قائمة **الحقول**، أعد تسمية جدول **الأبعاد المالية**، لتسهيل التعرف عليه.

7. حدد **إدارة العلاقات**، ثم حدد **جديد**.
8. في الحقل الأول، حدد **أنشطة دفتر الأستاذ العام**، ثم حدد **LedgerDimension‎**.
9. في الحقل الثاني، حدد **LedgerActivityMeasure\_DimensionCombination** (أو **الأبعاد المالية** إذا أعدت تسمية الجدول). حدد الرأس  **DimensionCombinationRECID**.
10. في حقل **العلاقة الأساسية‬**، حدد **من عديد إلى واحد**.
11. قم بتغيير قيمة **اتجاه التصفية المتقاطع** إلى **فردي**.
12. حدد الخيارين **تنشيط هذه العلاقة** و**افتراض التكامل المرجعي**، وحدد **OK**، ثم حدد **إغلاق**.

    [![إنشاء علاقة](./media/Create-relationship.png)](./media/Create-relationship.png)

13. في قائمة **الحقول**، من المفترض أن ترى الجدول والأبعاد المالية المتوفرة. اسحب الأبعاد المالية المطلوبة إلى عوامل التصفية على مستوى التقرير.
14. ‏‏قم بحفظ التغييرات التي قمت بإجرائها.
15. في شجرة مكونات البرنامج (AOT)، انقر بزر الماوس الأيمن فوق المشروع، ثم حدد **مزامنة**.
16. أنشئ مشروعك، ثم افتح التطبيق لعرض النتائج.

    [![مساحة عمل مكتملة](./media/workspace.png)](./media/workspace.png)

