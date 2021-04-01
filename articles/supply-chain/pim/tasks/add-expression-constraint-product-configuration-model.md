---
title: إضافة قيد تعبير إلى نموذج تكوين منتج
description: يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 81026d8622d3f03b3b87747800f4845cda823569
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5256149"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>إضافة قيد تعبير إلى نموذج تكوين منتج

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج. ويُظهر كيفية إصدار أمر رسمي بوجوب يجب تطبيق حماية الزاوية على مكبر صوت إذا قام المستخدم بتحديد شبكة أمامية معدنية. يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.


## <a name="create-an-expression-constraint"></a>قم بإنشاء قيد تعبير
1. انقر فوق "تعريف نموذج متغير المنتج"ز
2. انقر فوق "نماذج تكوين المنتجات".
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * يستخدم هذا المثال نموذج مكبر الصوت المتطور.  
4. في القائمة، انقر فوق الارتباط في الصف المحدد.
5. قم بتوسيع القسم "القيود".
6. وانقر فوق إضافة.
7. انقر فوق "إنشاء".
8. في حقل "الاسم"، اكتب قيمة.

## <a name="enter-expression"></a>إدخال تعبير
1. انقر فوق "تحرير التعبير".
    * إذا قمت بإلغاء تأمين واجهة المستخدم في تسجيل المهمة في هذه المرحلة، يمكنك استخدام IntelliSense وقائمة من الرموز لإنشاء تعبير القيد.  
2. في الحقل "ConstraintBody"، أدخل "Implies[FrontGrill=="Metal", CornerProtection]".
    * يوضح منطق التعبير هذا: إذا كانت الشبكة الأمامية معدنية، فيجب تحديد خيار حماية الزاوية.  
3. انقر فوق "التحقق من الصحة‬".
    * يتم تشغيل دالة التحقق من الصحة من خلال تعبير القيد وتتحقق من وجود أخطاء في بناء الجملة.  
4. انقر فوق "إغلاق".
5. انقر فوق "موافق".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]