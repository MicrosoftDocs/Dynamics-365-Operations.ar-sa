---
title: إزالة مثيل
description: توضح هذه المقالة عملية إزالة محرك اختبار أو بيئة إنتاج لشركة Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178456"
---
# <a name="remove-an-instance"></a>إزالة مثيل

_**ينطبق علي:** الموارد البشرية في البنية التحتية المستقلة_ 

> [!NOTE]
> بدءا من 2022 يوليو ، لا يمكن توفير بيئات الموارد البشرية الجديدة علي البنية الأساسية المستقلة للموارد البشرية ، ولا يمكن إنشاء مشاريع جديده Microsoft Dynamics لخدمات دوره الحياة (LCS) عليها. يمكن للعملاء نشر بيئات الموارد البشرية على البنية التحتية للتمويل والعمليات. لمزيد من المعلومات ، راجع [توفير الموارد البشرية في البنية الأساسية للعمليات والتمويل](/hr-admin-setup-provision-fo.md) .

> [!IMPORTANT]
> تدعم البنية الأساسية للتطبيق المالي والعمليات حذف بيئة. لمزيد من المعلومات حول كيفية حذف بيئة، راجع [احذف بيئة](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

توضح هذه المقالة عملية إزالة بيئة إنتاج أو تجربة إصدار جديدة لتطبيق Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>إزالة بيئة محرك أقراص اختبار

يتم توفير محركات أقراص اختبارات Human Resources باستخدام سياسة انتهاء صلاحية مدتها 60 يومًا. ومع ذلك، يتوفر لمالكي بيئات محركات أقراص الاختبار خيار إنهاء الخدمة التجريبية الخاصة بها بواسطة إكمال الخطوات التالية. 

1. الانتقال إلى مركز إدارة [Power Apps ](https://admin.businessplatform.microsoft.com/).
2. حدد **بيئات**.
3. حدد بيئة الإصدار التجريبي، ذات نمط تسمية مماثل للنمط التالي: TestDrive - alias@domain
4. حدد **حذف** وقم بتأكيد القرار. 

ستتم إزالة بيئة محرك أقراص الاختبار الموجودة. عندما تتم إزالتها، يمكنك تسجيل الاشتراك في بيئة محرك أقراص اختبار جديدة. 

## <a name="remove-a-production-environment"></a>إزالة بيئة إنتاج

يفترض هذا المقال أنك قمت بشراء Human Resources من خلال اتفاقية هندسة مؤسسة (EA) أو موفر حلول مجموعة (CSP). 

لأن بيئة موارد بشرية واحدة موجودة في ملف واحد Power Apps البيئة ، هناك خياران يجب مراعاتهما عند إزالة بيئة: 
- **حذف Power Apps البيئة بشكل كلي.** يُفضل هذا الخيار عندما يكون ملف Power Apps تم إنشاء البيئة لغرض توفير الموارد البشرية ، أو بدأ التنفيذ للتو ، أو لم يكن لديك أي عمليات تكامل ثابتة.  
- **إزالة الموارد البشرية فقط.** يكون هذا الخيار مناسبًا عندما يكون هناك بيئة Power Apps مثبتة التي يتم ملؤها بالبيانات المستخدمة فيها Microsoft Power Apps و Power Automate.


> [!Important]
> قبل إزالة بيئة Power Apps ، تأكد من عدم استخدامها لتكامل البيانات الثرية خارج نطاق الموارد البشرية. كما تجدر الإشارة إلى أنه لا يمكن إزالة بيئات Power Apps الافتراضية. 

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
7. حدد المثيل الذي ترغب في إزالته، والذي يجب تمييزه بحالة النشر **محذوف**.
8. حدد **إزالة مثيل** وقم بتأكيد قرارك. 

## <a name="recover-a-soft-deleted-environment"></a>استرداد بيئة محذوفة بشكل مبدئي

إذا قمت بحذف بيئة Power Apps البيئة التي ترتبط بها بيئة الموارد البشرية الخاصة بك ، ستكون حالة بيئة الموارد البشرية في LCSLifecycle Services **محذوفة مبدئيًا** . في هذه الحالة، سيتعذر على المستخدمين الاتصال بـ Human Resources.

لاستعاده البيئة:

1. اتبع الإرشادات في [استرداد بيئة Power Apps](/power-platform/admin/recover-environment).

2. اتصل بالدعم لاستعاده بيئة Human Resources. لمزيد من المعلومات، راجع [الحصول على الدعم](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> يتم حفظ بيئات Power Apps لسبعة أيام فقط بعد الحذف. يجب استرداد البيئة خلال فترة السبعة أيام.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
