--- 
title: "إنشاء خطة للموقع"
description: "يحسب مخطط الإنتاج متطلبات المواد والقدرة لإنتاج صنف معين."
author: ShylaThompson
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-plan-for-a-site"></a>إنشاء خطة للموقع

[!include [task guide banner](../../includes/task-guide-banner.md)]

يحسب مخطط الإنتاج متطلبات المواد والقدرة لإنتاج صنف معين. بعد أن يتم إنشاء اقتراحات التوريد، فإنه يجد الطلبات في الموقع الذي يتم به التخطيط للطلبات وتأكيدها، بدءاً من الطلبات العاجلة. وتكون الطلبات الأكثر إلحاحًا هي تلك التي يجب تأكيدها في التاريخ الحالي. استخدم شركة بيانات العرض التوضيحي USMF لتنفيذ هذه المهام.


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


