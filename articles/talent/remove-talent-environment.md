---
title: "إزالة بيئات Talent"
description: "يوضح لك هذا الموضوع عملية إزالة محرك أقراص اختبار أو بيئة إنتاج جديدة لـ Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 5080f1ec182b8cbdf281967185a1afeb9887f682
ms.contentlocale: ar-sa
ms.lasthandoff: 08/08/2018

---
# <a name="remove-talent-environments"></a>إزالة بيئات Talent

[!include [banner](includes/banner.md)]

يوضح لك هذا الموضوع عملية إزالة محرك أقراص اختبار أو بيئة إنتاج جديدة لـ Microsoft Dynamics 365 for Talent.

## <a name="removing-a-test-drive-environment"></a>إزالة بيئة محرك أقراص اختبار

يتم توفير محركات أقراص اختبارات Talent باستخدام سياسة انتهاء صلاحية مدتها 60 يومًا. ومع ذلك، يتوفر لمالكي بيئات محركات أقراص الاختبار خيار إنهاء الخدمة التجريبية الخاصة بها بواسطة إكمال الخطوات التالية. 

1. انتقل إلى [مركز إدارة PowerApps](https://admin.businessplatform.microsoft.com/).
2. حدد **بيئات**.
3. حدد بيئة محرك أقراص الاختبار الذي يحتوي على نمط تسمية مشابه لما يلي: TestDrive - alias@domain
4. حدد **حذف** وقم بتأكيد القرار. 

ستتم إزالة بيئة محرك أقراص الاختبار الموجودة. عندما تتم إزالتها، يمكنك تسجيل الاشتراك في بيئة محرك أقراص اختبار جديدة. 

## <a name="removing-a-production-environment"></a>إزالة بيئة إنتاج

يفترض هذا الموضوع أنك قمت بشراء Talent من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP). 

نظرًا لأن هناك بيئة Talent واحدة "مشمولة" ضمن بيئة PowerApps واحدة، هناك خياران ينبغي أخذهما بعين الاعتبار. الخيار الأول يتضمن إزالة بيئة PowerApps بالكامل، والثاني يتضمن إزالة Talent فقط. والخيار الأول هو المفضل عند قيامك بإنشاء بيئة PowerApps صراحةً بغرض توفير Talent، وقد بدأت التنفيذ للتو، أو لم يكن لديك أي عمليات تكامل قائمة. والخيار الثاني مناسب إذا كان لديك بيئة PowerApps محددة معبأة بالبيانات الغنية التي يتم جمعها في PowerApps والتدفقات.

> [!Important]
> قبل إزالة بيئة PowerApps، تأكد من عدم استخدامه لعمليات تكامل البيانات الغنية خارج نطاق Talent. كما تجدر الإشارة إلى أنه لا يمكن إزالة بيئات PowerApps الافتراضية. 

لإزالة بيئة PowerApps بأكملها، بما في ذلك Talent والتطبيقات والتدفقات المرتبطة:

1. انتقل إلى [مركز إدارة PowerApps](https://admin.businessplatform.microsoft.com/).
2. حدد **بيئات**.
3. حدد البيئة المُراد إزالتها.
4. حدد **حذف** وقم بتأكيد القرار. 
5. انتظر حتى تكتمل عملية الحذف.
6. قم بتسجيل الدخول إلى [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (‏LCS‏) باستخدام الحساب الذي استخدمته للاشتراك في Talent. 
7. حدد "مشروع Talent" الذي يحتوي على البيئة. 
8. في مشروع LCS، حدد تجانب **"إدارة تطبيق Talent**. 
9. حدد المثيل المراد إزالته. 
10. حدد **إزالة مثيل** وقم بتأكيد قرارك.  

لإزالة بيئة Talent من بيئة PowerApps موجودة، أكمل الخطوات التالية. لاحظ أن الحاجة إلى تضمين الدعم والاتصال بفريق عمليات تطوير Talent مؤقتة إلى أن يتم تمكين هذه الميزة في LCS مباشرةً.

1. اتصل بدعم لبدء طلب إزالة.
2. سيبدأ فريق الدعم طلب إزالة مع فريق عمليات تطوير Talent. 
3. تابع بعد ظهور كلمة لك تفيد بأنه تمت إزالة البيئة.
4.  قم بتسجيل الدخول إلى LCS باستخدام الحساب الذي استخدمته للاشتراك في Talent. 
5. حدد "مشروع Talent" الذي يحتوي على البيئة. 
6. في مشروع LCS، حدد تجانب **"إدارة تطبيق Talent**. 
7. حدد المثيل الذي ترغب في إزالته، والذي يجب تمييزه بحالة النشر **فشل**.
8. حدد **إزالة مثيل** وقم بتأكيد قرارك. 


