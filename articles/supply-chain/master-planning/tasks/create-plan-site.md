---
title: إنشاء خطة للموقع
description: يحسب مخطط الإنتاج متطلبات المواد والقدرة لإنتاج صنف معين.
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c8330fc15074eb59762dac73d0b176bd7faadc
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469494"
---
# <a name="create-a-plan-for-a-site"></a>إنشاء خطة للموقع

[!include [banner](../../includes/banner.md)]

يحسب مخطط الإنتاج متطلبات المواد والقدرة لإنتاج صنف معين. بعد أن يتم إنشاء اقتراحات التوريد، فإنه يجد الطلبات في الموقع الذي يتم به التخطيط للطلبات وتأكيدها، بدءًا من الطلبات العاجلة. وتكون الطلبات الأكثر إلحاحًا هي تلك التي يجب تأكيدها في التاريخ الحالي. استخدم شركة بيانات العرض التوضيحي USMF لتنفيذ هذه المهام.


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a>إنشاء مواد وخطة القدرة لصنف ما
1. انقر فوق "التخطيط الرئيسي‬".
    * أنت بحاجة إلى الانتقال إلى لوحة المعلومات الافتراضية.  
2. انقر فوق "تشغيل".
3. وسّع المقطع "السجلات المطلوب تضمينها‬".
4. انقر فوق "عامل التصفية".
5. في القائمة، قم بوضع علامة للصف المحدد.
6. في الحقل "المعايير"، اكتب قيمة.
    * على سبيل المثال: D0001  
7. انقر فوق "موافق".
8. انقر فوق "موافق".
    * قد تستغرق بضع دقائق.  
9. قم بتحديث الصفحة.

## <a name="identify-the-urgent-planned-orders-for-the-item"></a>تعريف الطلبات العاجلة المخططة للصنف
1. افتح عامل تصفية عمود "رقم الصنف".
2. طبّق عامل تصفية على الحقل "رقم الصنف" بقيمة "D0001"، باستخدام عامل التصفية "يبدأ بـ".
3. افتح عامل تصفية تاريخ الطلب.
4. استخدم عامل تصفية في حقل "تاريخ الطلب"، بقيمة التاريخ الحالي، باستخدام مشغل عامل التصفية "تمامًا مثل".

## <a name="firm-all-the-urgent-orders-for-the-item"></a>تأكيد كل الطلبات العاجلة للصنف
1. في القائمة، قم بوضع علامة أو إلغاء علامة كل الصفوف.
2. انقر فوق "تأكيد".
3. انقر فوق "موافق".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]