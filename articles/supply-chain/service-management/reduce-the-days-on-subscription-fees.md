---
title: تقليل الأيام على رسوم الاشتراك
description: لتخفيض عدد الأيام في رسم اشتراك موجود، يمكنك إنشاء حركة جديدة تقوم فيها بإزالة الفترة الزمنية التي لم تعد جزءًا من فترة رسم الاشتراك.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd76e30b14d0fd21617e0ab7d892ba5ea3e89f2f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217300"
---
# <a name="reduce-the-days-on-subscription-fees"></a>تقليل الأيام على رسوم الاشتراك 

[!include [banner](../includes/banner.md)]


لتخفيض عدد الأيام في رسم اشتراك موجود، يمكنك إنشاء حركة جديدة تقوم فيها بإزالة الفترة الزمنية التي لم تعد جزءًا من فترة رسم الاشتراك.

## <a name="reduce-the-days-on-a-subscription-fee"></a>تخفيض الأيام ف رسم اشتراك

1.  انقر فوق **إدارة الخدمة** \> **عام** \> **اشتراكات الخدمة** \> **جميع اشتراكات الخدمة**. حدد اشتراك الخدمة، ثم في جزء الإجراءات، انقر فوق **رسوم الاشتراك**

2.  في حقل **نوع الاشتراك**، حدد **أيام التخفيض**.

3.  استخدم حقل **تاريخ من** وحقل **تاريخ إلى** لتحديد فترة التاريخ الخاصة برسوم الاشتراك التي تريد إزالتها من فترة رسوم الاشتراك، ثم انقر فوق **موافق**.

لعرض الحركة التي تم إنشاؤها، في النموذج **الاشتراك**، انقر فوق **حركات الرسوم**.

## <a name="example"></a>مثال

إذا كانت فترة حركة الاشتراك تبدأ من 1 يناير إلى 31 يناير، وأنت ترغب في تخفيض المدة 15 يومًا، فقم بإنشاء حركة جديدة تبدأ فيها فترة التخفيض من 1 يناير إلى 10 يناير. (يُمكن أيضًا أن تكون فترة التخفيض من 5 يناير إلى 15 يناير، أو أي فترة عشرة أيام أخرى).

أيضًا إذا كان **من تاريخ** في فترة التخفيض هو 21 يناير (بطرح 10 من 31)، فيُمكنك تعيين **إلى تاريخ** على أي تاريخ بعد 31 يناير، ومع ذلك ستتم إزالة 10 أيام من فترة حركة الرسوم.

## <a name="see-also"></a>راجع أيضًا

[مثال أيام التخفيض](reduction-days-example.md)

  


