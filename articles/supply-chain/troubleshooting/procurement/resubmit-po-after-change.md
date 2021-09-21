---
title: خطأ عند إعادة إرسال أمر شراء إلى سير عمل بعد تغيير
description: خطأ عند إعادة إرسال أمر شراء إلى سير عمل بعد تغيير
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475519"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>خطأ عند إعادة إرسال أمر شراء إلى سير عمل بعد تغيير


## <a name="symptoms"></a>العلامات

يحدث الخطأ التالي في سير العمل عند إعادة إرسال أمر الشراء بعد إجراء تغيير:

> متوقف (خطـ): استثناء X++: يُسمح بإدخال تغييرات على أمر الشراء PO0000569 فقط بالحالة "مسودة" عند تنشيط إدارة التغييرات عند<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

تحدث هذه المشكلة فقط إذا كانت حالة أمر الشراء *مؤكد* قبل إجراء التغييرات المطلوبة. إذا طلبت تغييرات بينما حالة أمر الشراء *موافق عليه*، فيمكن معالجة سير العمل بنجاح.

## <a name="resolution"></a>الحل

قد تحدث هذه المشكلة بسبب عدم الاتساق في توزيعات أمر الشراء.

لحل هذه المشكلة وإعادة تعيين أمر الشراء إلى الحالة *مسودة*، انتقل إلى **التدبير والتوريد \> المهام الدورية \> تنظيف \> إعادة تعيين توزيع أمر الشراء**. لمزيد من المعلومات، راجع منشور المدونة التالي: [حل أخطاء توزيع أمر الشراء في Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

سيتم حل هذه المشكلة من خلال [مقالة قاعدة معارف (KB)‏ Microsoft هذه](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
