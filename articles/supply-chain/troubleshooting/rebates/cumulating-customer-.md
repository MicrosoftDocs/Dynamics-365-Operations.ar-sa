---
title: يفشل تراكم خصومات العميل عند استخدام مجموعات الخصم للأصناف
description: عند استخدام اتفاقيات الخصم للعميل مع مجموعات خصم الصنف، يتم حساب الخصومات، ولكن يفشل التراكم.
author: sherry-zheng
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PdsRebateTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: fc3381dab77cf80c0fd65f3bc27c11b814e72368631bd0e2145aac0be4f4fba4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760360"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>يفشل تراكم خصومات العميل عند استخدام مجموعات الخصم للأصناف

رقم KB: 4611372

## <a name="symptoms"></a>العلامات

عند استخدام اتفاقيات الخصم للعميل(لنوع *المبلغ*) مع مجموعات خصم الصنف، يتم حساب الخصومات، ولكن يفشل التراكم.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. تقوم مجموعات الأصناف فقط بتجميع الأصناف التي لها نفس شرط الحد. يتم تعيين شرط الخصم (الحد) مقابل المبلغ لكل صنف، وليس مقابل المبلغ المتراكم لأي صنف في مجموعة الصنف.
