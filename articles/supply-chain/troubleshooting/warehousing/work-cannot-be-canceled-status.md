---
title: لا يمكن إلغاء العمل بسبب حالته
description: لا يمكن إلغاء العمل بسبب حالته
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 60b4da44ca5e6790302e0797640317cef8493db7
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924245"
---
# <a name="work-cant-be-canceled-because-of-its-status"></a>لا يمكن إلغاء العمل بسبب حالته

رمز الخطأ: WAX2190

## <a name="symptoms"></a>العلامات

يعرض النظام رسالة الخطأ التالية:

> لا يمكنك إلغاء العمل %1 لأن حالته %2.

## <a name="cause"></a>السبب

لا يمكن إلغاء العمل في حالته الحالية.

لا يحتوي رأس العمل أو بنود العمل على قيمة **حالة العمل** المتوقعة. لم يتم تعيين حقل **حالة العمل** في رأس العمل إلى *مفتوح* أو *قيد التقدم*.

## <a name="resolution"></a>الدقة

لإلغاء العمل، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.
1. في حقل **معرف العمل**، حدد معرف العمل الذي ترغب في إلغائه.
1. حدد **موافق**.
1. حدد **نعم** لتأكيد رغبتك في إلغاء العمل.

لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).