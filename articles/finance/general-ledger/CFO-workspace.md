---
title: إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬
description: يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 457c547947ce6182d03e7a8276b380bc08535bca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985102"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>إضافة الأبعاد المالية إلى مساحة عمل المدير المالي‬

[!include [banner](../includes/banner.md)]

يشرح هذا المقال كيفية إضافة الأبعاد المالية إلى مساحة عمل المدير المالي، بحيث يمكن استخدامها لتقارير دفتر الأستاذ والموازنة. تتضمن مساحة عمل المدير المالي علامة التبويب **نظرة عامة** وعلامة التبويب **مالي**. هناك مقياسان لدعم التقارير على علامتي التبويب: LedgerActivityMeasure وBudgetActivityMeasure. توجد علاقة بين هذين المقياسين والكيان DimensionCombinationEntity. لذلك، يمكنك تحديد الأبعاد.

1. في Finance، في صفحة **متجر الكيانات**، قم بتحديث المقياسين **LedgerActivityMeasure** و **BudgetActivityMeasure**.
2. في Microsoft Visual Studio، افتح مستكشف التطبيق، وابحث عن **LedgerCFO**.
3. ضمن **الموارد**، افتح **LedgerCFOWorkspacePBIX‎**.
4. عندما يفتح المورد في Microsoft Power BI desktop، حدد **الحصول على البيانات**، وحدد **قاعدة بيانات SQL Server**، ثم حدد **اتصال**.
5. أدخل اسم الخادم، ثم أدخل **AxDW** كقاعدة بيانات. حدد **DirectQuery**، ثم حدد **موافق**.
6. ابحث عن **LedgerActivityMeasure\_DimensionCombination** وحدده، ثم حدد **تحميل**.

    > [!TIP]
    > في قائمة **الحقول**، أعد تسمية جدول **الأبعاد المالية**، لتسهيل التعرف عليه.

7. حدد **إدارة العلاقات**، ثم حدد **جديد**.
8. في الحقل الأول، حدد **أنشطة دفتر الأستاذ العام**، ثم حدد **LedgerDimension‎**.
9. في الحقل الثاني، حدد **LedgerActivityMeasure\_DimensionCombination** (أو **الأبعاد المالية** إذا أعدت تسمية الجدول). حدد الرأس  **DimensionCombinationRECID**.
10. في حقل **العلاقة الأساسية‬**، حدد **من عديد إلى واحد**.
11. قم بتغيير قيمة **اتجاه التصفية المتقاطع** إلى **فردي**.
12. حدد الخيارين **تنشيط هذه العلاقة** و **افتراض التكامل المرجعي**، وحدد **OK**، ثم حدد **إغلاق**.

    [![إنشاء علاقة](./media/Create-relationship.png)](./media/Create-relationship.png)

13. في قائمة **الحقول**، من المفترض أن ترى الجدول والأبعاد المالية المتوفرة. اسحب الأبعاد المالية المطلوبة إلى عوامل التصفية على مستوى التقرير.
14. ‏‏قم بحفظ التغييرات التي قمت بإجرائها.
15. في شجرة مكونات البرنامج (AOT)، انقر بزر الماوس الأيمن فوق المشروع، ثم حدد **مزامنة**.
16. أنشئ مشروعك، ثم افتح التطبيق لعرض النتائج.

    [![مساحة عمل مكتملة](./media/workspace.png)](./media/workspace.png)
