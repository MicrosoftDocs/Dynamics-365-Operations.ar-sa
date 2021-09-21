---
title: يتعذر تحديد تغيير حالة المخزون كنوع عمل
description: لا يمكنك إنشاء بند قالب عمل لتغيير حالة المخزون لأنه يتم استخدام نوع العمل فقط بواسطة عمليات النظام. حدد نوع عمل مختلف.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475506"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>يتعذر تحديد تغيير حالة المخزون في العمود نوع العمل

## <a name="symptoms"></a>العلامات

عند تكوين Microsoft Dynamics 365 Supply Chain Management، قد تستلم رسالة الخطأ التالية:

> لا يمكنك إنشاء بند قالب عمل لتغيير حالة المخزون لأن نوع العمل غير صالح. حدد نوع عمل مختلف.

## <a name="resolution"></a>الحل

يتم هذا السلوك بسبب التصميم. يتم استخدام نوع العمل *تغيير حاله المخزون* فقط من قبل عمليات النظام. لا يمكن تكوينها. ونظرا لان قائمه أنواع العمل قد تم إصلاحها علي انها قائمه تعداد ، لا يمكن تصفيه الإدخالات الاضافيه خارج القائمة المنسدلة **نوع العمل**.
