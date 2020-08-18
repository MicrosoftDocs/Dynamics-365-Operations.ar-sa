---
title: إزالة مثيل
description: ينقلك هذا المقال عبر عملية إزالة بيئة إنتاج أو بيئة إصدار تجريبي جديدة لتطبيق Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a384801060b2b684f7908daaac2311edd27c773a
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621370"
---
# <a name="remove-an-instance"></a>إزالة مثيل

ينقلك هذا المقال عبر عملية إزالة بيئة إنتاج أو بيئة إصدار تجريبي جديدة لتطبيق Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>إزالة بيئة محرك أقراص اختبار

يتم توفير محركات أقراص اختبارات Human Resources باستخدام سياسة انتهاء صلاحية مدتها 60 يومًا. ومع ذلك، يتوفر لمالكي بيئات محركات أقراص الاختبار خيار إنهاء الخدمة التجريبية الخاصة بها بواسطة إكمال الخطوات التالية. 

1. الانتقال إلى مركز إدارة [Power Apps ](https://admin.businessplatform.microsoft.com/).
2. حدد **بيئات**.
3. حدد بيئة الإصدار التجريبي، ذات نمط تسمية مماثل للنمط التالي: TestDrive - alias@domain
4. حدد **حذف** وقم بتأكيد القرار. 

ستتم إزالة بيئة محرك أقراص الاختبار الموجودة. عندما تتم إزالتها، يمكنك تسجيل الاشتراك في بيئة محرك أقراص اختبار جديدة. 

## <a name="remove-a-production-environment"></a>إزالة بيئة إنتاج

يفترض هذا المقال أنك قمت بشراء Human Resources من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP). 

نظرًا لأن هناك بيئة Human Resources واحدة مشمولة ضمن بيئة Power Apps واحدة، هناك خياران ينبغي أخذهما بعين الاعتبار. الخيار الأول يتضمن إزالة بيئة Power Apps بالكامل، والثاني يتضمن إزالة Human Resources فقط. والخيار الأول هو المفضل عند قيامك بإنشاء بيئة Power Apps صراحةً بغرض توفير Human Resources، وقد بدأت التنفيذ للتو، أو لم يكن لديك أي عمليات تكامل قائمة. والخيار الثاني مناسب إذا كان لديك بيئة Power Apps محددة معبأة بالبيانات الغنية التي يتم جمعها في Power Apps وPower Automate.

> [!Important]
> قبل إزالة بيئة Power Apps، تأكد من عدم استخدامه لعمليات تكامل البيانات الغنية خارج نطاق Human Resources. كما تجدر الإشارة إلى أنه لا يمكن إزالة بيئات Power Apps الافتراضية. 

لإزالة بيئة Power Apps بأكملها، بما في ذلك Human Resources والتطبيقات والتدفقات المرتبطة:

1. الانتقال إلى مركز إدارة [Power Apps ](https://admin.businessplatform.microsoft.com/).
2. حدد **بيئات**.
3. حدد البيئة المُراد إزالتها.
4. حدد **حذف** وقم بتأكيد القرار. 
5. انتظر حتى تكتمل عملية الحذف.
6. قم بتسجيل الدخول إلى [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (‏LCS‏) باستخدام الحساب الذي استخدمته للاشتراك في Human Resources. 
7. حدد مشروع Human Resources الذي يحتوي على البيئة. 
8. في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**. 
9. حدد المثيل المراد إزالته. 
10. حدد **إزالة مثيل** وقم بتأكيد قرارك.  

لإزالة بيئة Human Resources من بيئة Power Apps موجودة، أكمل الخطوات التالية. لاحظ أن الحاجة إلى تضمين الدعم والاتصال بفريق عمليات تطوير Human Resources مؤقتة إلى أن يتم تمكين هذه الميزة في LCS مباشرةً.

1. اتصل بدعم لبدء طلب إزالة.
2. سيبدأ فريق الدعم طلب إزالة مع فريق عمليات تطوير Human Resources. 
3. تابع بعد ظهور كلمة لك تفيد بأنه تمت إزالة البيئة.
4. قم بتسجيل الدخول إلى LCS باستخدام الحساب الذي استخدمته للاشتراك في Human Resources. 
5. حدد مشروع Human Resources الذي يحتوي على البيئة. 
6. في مشروع LCS، حدد تجانب **"إدارة تطبيق Human Resources**. 
7. حدد المثيل الذي ترغب في إزالته، والذي يجب تمييزه بحالة النشر **فشل**.
8. حدد **إزالة مثيل** وقم بتأكيد قرارك. 

## <a name="recover-a-soft-deleted-environment"></a>استرداد بيئة محذوفة بشكل مبدئي

إذا قمت بحذف بيئة Power Apps من بيئة Human Resources المتصلة بها، ستكون حالة بيئة Human Resources في Lifecycle Services **محذوفة مبدئيًا** . في هذه الحالة، سيتعذر على المستخدمين الاتصال بـ Human Resources.

لاستعاده البيئة:

1. اتبع الإرشادات في [استرداد بيئة Power Apps](/power-platform/admin/recover-environment.md).

2. اتصل بالدعم لاستعاده بيئة Human Resources. لمزيد من المعلومات، راجع [الحصول على الدعم](hr-admin-troubleshooting-support.md).

> [!Warning]
> يتم حفظ بيئات Power Apps لسبعة أيام فقط بعد الحذف. يجب استرداد البيئة خلال فترة السبعة أيام.
