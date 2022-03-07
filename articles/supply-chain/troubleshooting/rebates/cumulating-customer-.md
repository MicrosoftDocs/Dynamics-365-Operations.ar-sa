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
ms.openlocfilehash: 5222d5a52a34ecfa4a1eac96a2cb561f257f17ea
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026225"
---
# <a name="cumulation-of-customer-rebates-fails-when-item-rebate-groups-are-used"></a>يفشل تراكم خصومات العميل عند استخدام مجموعات الخصم للأصناف

رقم KB: 4611372

## <a name="symptoms"></a>العلامات

عند استخدام اتفاقيات الخصم للعميل(لنوع *المبلغ*) مع مجموعات خصم الصنف، يتم حساب الخصومات، ولكن يفشل التراكم.

## <a name="resolution"></a>الدقة

يعمل النظام كما هو مصمم. تقوم مجموعات الأصناف فقط بتجميع الأصناف التي لها نفس شرط الحد. يتم تعيين شرط الخصم (الحد) مقابل المبلغ لكل صنف، وليس مقابل المبلغ المتراكم لأي صنف في مجموعة الصنف.
