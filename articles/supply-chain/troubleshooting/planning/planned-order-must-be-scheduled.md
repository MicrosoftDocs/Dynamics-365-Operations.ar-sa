---
title: يجب جدولة أمر الإنتاج المخطط قبل أن يتم تأكيده
description: عند محاولة تأكيد أمر مخطط، فإنك تتلقى رسالة خطأ تنص على أنه يجب جدولة الأمر قبل أن يتم تأكيده.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294006"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>يجب جدولة أمر الإنتاج المخطط قبل أن يتم تأكيده

رمز الخطأ: SYS309802

## <a name="symptoms"></a>العلامات

عند محاولة تأكيد أمر مخطط، تظهر رسالة الخطأ التالية:

> يجب جدولة أمر الإنتاج المخطط قبل التمكن من تأكيده.

## <a name="cause"></a>السبب

لا يمكن أن يكون تواريخ البدء والانتهاء المجدولة فارغة.

## <a name="resolution"></a>الحل

لتحديد تواريخ البدء والانتهاء للأمر المخطط، اتبع الخطوات التالية.

1. انتقل إلى **التخطيط الرئيسي \> التخطيط الرئيسي \> الطلبات المخططة**.
1. افتح الأمر المخطط المتعلق.
1. في علامة التبويب السريعة **عام**، في القسم **مجدول**، حدد التواريخ في الحقلين **تاريخ البدء** و **تاريخ الانتهاء**.
