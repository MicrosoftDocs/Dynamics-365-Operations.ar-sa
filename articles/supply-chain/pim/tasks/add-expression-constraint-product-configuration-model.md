---
title: إضافة قيد تعبير إلى نموذج تكوين منتج
description: يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77e8b991a2615a8f5d238acc4655f231edb6ca98
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/29/2021
ms.locfileid: "7569639"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a>إضافة قيد تعبير إلى نموذج تكوين منتج

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إضافة تعبير قيد جديد إلى نموذج تكوين منتج. ويُظهر كيفية إصدار أمر رسمي بوجوب يجب تطبيق حماية الزاوية على مكبر صوت إذا قام المستخدم بتحديد شبكة أمامية معدنية. يستخدم الإجراء المكون مكبر الصوت المتطور في شركة العرض التوضيحي USMF.

## <a name="create-an-expression-constraint"></a>قم بإنشاء قيد تعبير

1. انتقل إلى **إدارة معلومات المنتج \> المنتجات \> نماذج تكوين المنتجات**.
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
    * يستخدم هذا المثال نموذج مكبر الصوت المتطور.  
4. في القائمة، حدد الارتباط في الصف المحدد.
5. قم بتوسيع قسم **القيود**.
6. حدد **إضافة**.
7. حدد **إنشاء**.
8. في الحقل **الاسم**، اكتب قيمة.

## <a name="enter-expression"></a>إدخال تعبير

1. حدد **تحرير التعبير**.
    * إذا قمت بإلغاء تأمين واجهة المستخدم في تسجيل المهمة في هذه المرحلة، يمكنك استخدام IntelliSense وقائمة من الرموز لإنشاء تعبير القيد.  
2. في حقل **ConstraintBody**، أدخل 'Implies[FrontGrill=="Metal", CornerProtection] '.
    * يوضح منطق التعبير هذا: إذا كانت الشبكة الأمامية معدنية، فيجب تحديد خيار حماية الزاوية.  
3. حدد **التحقق من الصحة**.
    * يتم تشغيل دالة التحقق من الصحة من خلال تعبير القيد وتتحقق من وجود أخطاء في بناء الجملة.  
4. حدد **إغلاق**.
5. حدد **موافق**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]