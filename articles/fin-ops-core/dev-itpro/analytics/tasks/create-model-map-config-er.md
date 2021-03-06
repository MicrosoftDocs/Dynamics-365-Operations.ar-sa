---
title: إنشاء تكوينات لتعيين نماذج التقارير الإلكترونية
description: استخدم هذا الإجراء لتصميم تكوين جديد لتعيين نموذج التقارير الإلكترونية، واستخدم وظائف التقارير الإلكترونية المدمجة لإجراء حسابات مجمعة فعالة.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 23bc3a525be9f65b7e5100114d02f6b79a286fb5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682059"
---
# <a name="create-electronic-reporting-er-model-mapping-configurations"></a>إنشاء تكوينات لتعيين نماذج التقارير الإلكترونية

[!include [banner](../../includes/banner.md)]

استخدم هذا الإجراء لتصميم تكوين جديد لتعيين نموذج التقارير الإلكترونية، واستخدم وظائف التقارير الإلكترونية المدمجة لإجراء حسابات مجمعة فعالة. في هذا الإجراء، ستقوم بإنشاء تكوين لشركة نموذجية، وهي Litware, Inc. 

تم إنشاء هذا الإجراء للاستخدامات مع الدور المعين سواء كان مسؤول النظام أو مطور التقارير الإلكترونية.

يمكن إتمام هذه الخطوات باستخدام أي مجموعة بيانات. لإكمال هذه الخطوات، يجب أولاً إكمال الخطوات المذكورة في الإجراء "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط".

1. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
    * تأكد من وجود موفر التكوين للشركة النموذجية "Litware, Inc." ومن وضع علامة عليه كنشط. إذا لم تشاهد موفر التكوين هذا، فيجب أولاً إكمال الخطوات المذكورة في الإجراء، "إنشاء موفر تكوين ووضع علامة عليه على أنه نشط‬".  
2. انقر فوق "تكوينات إعداد التقارير‬".
3. انقر فوق "إظهار عوامل التصفية".
4. في حقل "الاسم"، أدخل قيمة عامل التصفية "نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي" واستخدم عامل التصفية "يبدأ بـ".
    * طبّق عامل التصفية هذا للبحث عن تكوين نموذج بيانات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي. قد يكون هذا النموذج موجودًا في شجرة التكوينات. إذا كان موجودًا، فيمكنك تخطي المهمة الفرعية التالية.   

## <a name="get-the-intrastat-model-configuration-provided-by-microsoft"></a>الحصول على تكوين نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي الذي توفره Microsoft
1. قم بإغلاق الصفحة.
2. قم بإغلاق الصفحة.
3. انتقل إلى إدارة المؤسسة > مساحات العمل‬ > إعداد التقارير الإلكتروني‬.
4. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * حدد لوحة "موفر Microsoft".  
5. انقر فوق "المستودعات".
    * انقر فوق "المستودعات‬" على لوحة موفر Microsoft.  
6. انقر فوق "إظهار عوامل التصفية".
7. في حقل "نوع الاسم"، أدخل قيمة عامل التصفية "موارد" واستخدم عامل التصفية "يحتوي". 
8. انقر فوق "فتح".
9. في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".
10. انقر فوق "استيراد".
11. انقر فوق نعم.
    * لقد قمت باستيراد تكوين نموذج التقارير الإلكترونية الذي يحتوي على نموذج البيانات الذي ستستخدمه لاستكشاف كيفية استخدام وظائف التقارير الإلكترونية الجديدة.  
12. قم بإغلاق الصفحة.
13. قم بإغلاق الصفحة.
14. انقر فوق "تكوينات إعداد التقارير‬".

## <a name="add-a-new-model-mapping-configuration"></a>إضافة تكوين تعيين نموذج جديد
1. في الشجرة، حدد "نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".
2. انقر فوق "إنشاء تكوين" لفتح مربع حوار الإسقاط‬.
3. في الحقل "جديد"، أدخل "تعيين النموذج استنادًا إلى نموذج بيانات نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".
4. في حقل "الاسم"، اكتب "تعيين نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي".
    * تعيين نموذج نظام جمع المعلومات التجارية بين دول الاتحاد الأوروبي  
5. وانقر فوق إنشاء تكوين.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]