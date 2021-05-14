---
title: لا يمكنك إلغاء العمل الذي يتم تشغيله على أحد المستخدمين
description: لا يمكنك إلغاء العمل الذي يتم تشغيله على أحد المستخدمين
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
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924391"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a>لا يمكنك إلغاء العمل الذي يتم تشغيله على أحد المستخدمين

رمز الخطأ: WAX708

## <a name="symptoms"></a>العلامات

يعرض النظام رسالة الخطأ التالية:

> لا يمكن إلغاء عمل موجود للمستخدم.

## <a name="cause"></a>السبب

العمل مغلق من قبل مستخدم ولا يمكن إلغاؤه. لتأكيد ذلك، افتح معرّف العمل ثم افتح علامة التبويب **عام**. إذا تم قفل العمل، فسيتم تعيين حقل **حالة العمل** إلى *قيد التقدم*، وسيتم تعيين حقل **تم القفل بواسطة** إلى معرف المستخدم.

## <a name="resolution"></a>الدقة

لإلغاء العمل، اتبع الخطوات التالية.

1. انتقل إلى **إدارة المستودع \> المهام الدورية \> تنظيف \> إلغاء العمل**.
1. في حقل **معرف العمل**، حدد معرف العمل الذي ترغب في إلغائه.
1. حدد **موافق**.
1. حدد **نعم** لتأكيد رغبتك في إلغاء العمل.

لمزيد من المعلومات، راجع [إلغاء عمل المستودع لمعالجة الاستثناء](../../warehousing/cancel-warehouse-work.md).
