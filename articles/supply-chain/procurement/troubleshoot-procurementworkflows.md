---
title: استكشاف أخطاء عمليات سير عمل التدبير والتوريد وإصلاحها
description: يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع سير عمل التدبير والتوريد.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: e8274890c581fffc7330538430c9b2ba060041bc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999093"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>استكشاف أخطاء عمليات سير عمل التدبير والتوريد وإصلاحها

يوضح هذا الموضوع كيفية إصلاح المشكلات التي قد تواجهها أثناء العمل مع سير عمل التدبير والتوريد.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>حدث خطأ عند إعادة إرسال أمر شراء إلى سير العمل بعد التغيير: "يُسمح بإجراء تغييرات على أمر الشراء X فقط في حالة المسودة عند تنشيط إدارة التغييرات"

تحدث هذه المشكلة فقط إذا كانت حالة أمر الشراء *مؤكد* قبل إجراء التغييرات المطلوبة. إذا طلبت تغييرات بينما حالة أمر الشراء *موافق عليه*، فيمكن معالجة سير العمل بنجاح.

### <a name="error-description"></a>وصف الخطأ

يحدث الخطأ التالي في سير العمل عند إعادة إرسال أمر الشراء بعد إجراء تغيير:

> متوقف (خطـ): استثناء X++: يُسمح بإدخال تغييرات على أمر الشراء PO0000569 فقط بالحالة "مسودة" عند تنشيط إدارة التغييرات عند<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>حل المشكلة

قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.

لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**. لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

سيتم حل هذه المشكلة من خلال [مقالة قاعدة معارف (KB)‏ Microsoft هذه](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>هناك زيادة أو نقص في التوزيع في توزيع محاسبي واحد أو أكثر.

قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.

لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**. لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>إذا تم إلغاء كمية متبقية من التسليم على أمر شراء تم فيه تشغيل إدارة التغييرات، ينتقل أمر الشراء إلى الحالة "مؤكد".

### <a name="issue-description"></a>وصف المشكلة

بالنسبة لأمر شراء يخضع لإدارة التغييرات، إذا كان التغيير الوحيد المطلوب إلغاء كمية متبقية من التسليم على بند أو أكثر، فسينتقل أمر الشراء بشكل مباشر إلى الحالة *مؤكد* عندما يكون موافقًا عليه، ولن يتم إنشاء دفتر يومية.

### <a name="issue-resolution"></a>حل المشكلة

لا يؤثر إلغاء الكمية المتبقية من التسليم على محتويات دفتر يومية التأكيد. يجب استخدام هذه الوظيفة عند استلام البند بشكل جزئي، ويجب إلغاء جودة الكمية المتبقية في خطوة المعالجة بعد تأكيد أمر الشراء مع المورّد.

إذا كان يجب أني ينعكس ذلك على تأكيد أمر الشراء، فيجب تعديل الكمية في بند أمر الشراء حتى يكون التأكيد مطلوبًا. بدلاً من ذلك، إذا لم يتم استلام أي شيء على البند، فيمكن إزالة الكمية. في هذه الحالة، ستكون إعادة التأكيد مطلوبة.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>تظهر أوامر الشراء الملغاة في قائمة مسودة في مساحة عمل تجهيز أمر الشراء.

### <a name="issue-description"></a>وصف المشكلة

بعد إلغاء أوامر الشراء التي كانت في الحالة *مؤكد*، يستمر ظهور أوامر الشراء الملغاة في قائمة أوامر الشراء في حالة المسودة في مساحة عمل **تجهيز أمر الشراء**.

### <a name="issue-resolution"></a>حل المشكلة

تحدث هذه المشكلة فقط مع أوامر الشراء التي تخضع لإدارة التغييرات. وهي تحدث لأن الإلغاء يُعتبر كتغيير يجب الموافقة عليه. يمكن إجراء الموافقة بشكل تلقائي بواسطة النظام. وبالتالي، تقضي العملية بأن يتم إرسال أمر الشراء الملغى إلى سير عمل الموافقة بحيث يمكنه الانتقال إلى الحالة *موافق عليه*. وفي هذه المرحلة، سيتوقف ظهور أمر الشراء في قائمة أوامر الشراء بحالة المسودة في مساحة عمل **تجهيز أمر الشراء**.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]