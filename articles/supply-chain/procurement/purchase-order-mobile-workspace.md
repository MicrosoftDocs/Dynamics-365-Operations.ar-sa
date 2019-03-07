---
title: مساحة العمل المحمولة "الموافقة على أمر الشراء"
description: يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة "الموافقة على أمر الشراء"، التي تسمح لك بعرض أوامر الشراء والاستجابة لها من خلال الإجراءات. على سبيل المثال، يمكنك الموافقة على أمر شراء أو رفضه.
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 75a38b99fe0aee7d4dd386191be236e54097e867
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "348838"
---
# <a name="purchase-order-approval-mobile-workspace"></a>مساحة العمل المحمولة "الموافقة على أمر الشراء"

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

يوفر هذا الموضوع معلومات حول مساحة العمل المحمولة **الموافقة على أمر الشراء**. تسمح لك مساحة العمل هذه بعرض أوامر الشراء والاستجابة إليها من خلال الإجراءات. على سبيل المثال، يمكنك الموافقة على أمر شراء أو رفضه.
 
## <a name="overview"></a>نظرة عامة 
تمر أوامر الشراء التي تحتاج إلى موافقة على سير عمل الموافقة. باستطاعة سير العمل أن يتضمن خطوات مختلفة تتطلب قيام شخص أو أكثر باتخاذ الإجراءات اللازمة. على سبيل المثال، قد يتعين على شخص ما إكمال مهمة أو الموافقة على أمر الشراء. 

تسمح لك مساحة العمل المحمولة **الموافقة على أمر الشراء** بعرض أوامر الشراء والاستجابة لها بسهولة من جهازك المحمول. وتسمح لك أيضًا مساحة العمل هذه باتخاذ إجراءات سير العمل نفسها التي يمكنك اتخاذها من Microsoft Dynamics 365 for Finance and Operations، عميل ويب.

## <a name="prerequisites"></a>المتطلبات الأساسية
تختلف المتطلبات الأساسية، بالاستناد إلى إصدار Finance and Operations الذي تم نشره لمؤسستك.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a>المتطلبات الأساسية عند استخدام Microsoft Dynamics 365 for Finance and Operations 
إذا تم نشر Microsoft Dynamics 365 for Finance and Operations لمؤسستك، فيتعين على مسؤول النظام نشر مساحة العمل المحمولة **الموافقة على أمر الشراء​‬**. للاطلاع على الإرشادات، راجع [نشر مساحة العمل المحمولة ](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>المتطلبات الأساسية إذا كنت تستخدم الإصدار 1611 من Microsoft Dynamics 365 for Operations مع Platform update 3 أو إصدار لاحق
إذا تم نشر الإصدار 1611 من Microsoft Dynamics 365 for Operations مع Platform update 3 أو إصدار أحدث لمؤسستك، فيجب على مسؤول النظام إكمال المتطلبات الأساسية التالية. 

<table>
<thead>
<tr class="header">
<th>المتطلب الأساسي</th>
<th>الدور</th>
<th>‏‏الوصف</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>تطبيق قاعدة المعارف 4017918.</td>
<td>مسؤول النظام</td>
<td>إن KB 4017918 عبارة عن تحديث X++ أو إصلاح عاجل لبيانات التعريف يحتوي على مساحة العمل المحمولة <strong>الموافقة على أمر الشراء</strong>. لتطبيق KB 4017918، يجب أن يتبع مسؤول النظام الخطوات التالية.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">تنزيل الإصلاح العاجل لبيانات التعريف من Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">تثبيت الإصلاح العاجل لبيانات التعريف</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">إنشاء حزمة قابلة للنشر</a> تحتوي على نموذج <strong>SCMMobile</strong>، ثم تحميل الحزمة القابلة للنشر إلى LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">تطبيق الحزمة القابلة للنشر</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>نشر مساحة العمل المحمولة <strong>الموافقة على أمر الشراء</strong>.</td>
<td>مسؤول النظام</td>
<td>راجع <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">نشر مساحة عمل محمولة</a></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>تحميل وتثبيت تطبيق الجوال
تنزيل وتثبيت تطبيق Microsoft Dynamics 365 for Unified Operations Mobile:

- [لهواتف Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [لهواتف iPhone](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a>تسجيل الدخول إلى تطبيق الهاتف الجوال

1. ابدأ تشغيل التطبيق على جهازك المحمول.
2. أدخل عنوان URL لـ Microsoft Dynamics 365.
3. في المرة الأولى التي تقوم بتسجيل الدخول فيها، تتم مطالبتك باسم المستخدم وكلمة المرور الخاصة بك. أدخل بيانات اعتمادك.
4. بعد تسجيل الدخول، تظهر مساحات العمل المتوفرة لشركتك. تجدر الإشارة إلى أنه في حال قيام مسؤول النظام بنشر مساحة عمل جديدة في وقت لاحق، فسوف يكون عليك تحديث قائمة مساحات العمل المحمولة.

![مساحة عمل الموافقة على أمر الشراء في قائمة مساحات العمل المتاحة](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a>عرض الأوامر التي تم تعيينها لك
1. على جهازك المحمول، حدد مساحة العمل **الموافقة على أمر الشراء‬**.
2. حدد **الأوامر التي تم تعيينها إلىّ‬** لعرض كافة أوامر الشراء التي تمت مطالبتك باتخاذ إجراء بشأنها في سير عمل الموافقة على أمر الشراء.
3. حدد أمرًا. في صفحة **تفاصيل الأمر**، سوف ترى معلومات رأس الأمر وبنوده. يمكنك أيضًا العثور على إرشادات من مهمة سير العمل.
4. حدد **التوزيعات المحاسبية** لفتح صفحة **التوزيع المحاسبي للرأس‬**.
5. عد إلى صفحة **تفاصيل الأمر** ، ثم حدد بندًا. من تفاصيل بند الأمر، يمكنك أيضًا اكتشاف التوزيعات المحاسبية الخاصة بالبند.

## <a name="complete-an-action-on-the-purchase-order"></a>إكمال إجراء في أمر الشراء
بعد عرض أمر الشراء الذي تم تعيينه لك وقراءة إرشادات سير العمل، يجب أن تكون جاهزًا لاتخاذ الإجراء المطلوب.

1. على جهازك المحمول، حدد مساحة العمل **الموافقة على أمر الشراء‬**.
2. حدد **الأوامر التي تم تعيينها إلىّ‬** لعرض كافة أوامر الشراء التي تمت مطالبتك باتخاذ إجراء بشأنها في سير عمل الموافقة على أمر الشراء.
3. حدد أمرًا واعرض صفحة التفاصيل.
4. حدد **الإجراءات** لإظهار الإجراءات المتوفرة. تعتمد الإجراءات المتوفرة على المهمة التي تم تعيينها لك.

    | إجراء المهمة    | إجراء الموافقة  |
    |----------------|------------------|
    | مكتمل       | موافقة          |
    | إرجاع         | رفض           |
    | تغيير الطلب | تغيير الطلب   |
    | التفويض       | التفويض         |

5. حدد الإجراء المناسب.
6. في صفحة **إكمال المهمة**، قم بإدخال تعليق. لاحظ أنك إذا قمت بتحديد الإجراء **تفويض**، يجب تحديد مستخدم لتفويض المهمة إليه.
7. حدد **تم**. بعد أن تقوم بتحديث مساحة العمل، سيتوقف أمر الشراء عن الظهور في قائمتك. 
