--- 
title: "إنشاء أمر شراء لمورد مرة واحدة"
description: "يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 580dfe3680c36a32a24999bc8c266a38a07177fd
ms.contentlocale: ar-sa
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>إنشاء أمر شراء لمورد مرة واحدة

[!include[task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة. يتم إنشاء المورّد مع أمر الشراء بشكل تلقائي، بدلاً من إنشاء حساب المورّد يدويًا. وعادة ما يتم إنشاء أوامر الشراء عن طريق وكيل شراء. يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF. يجب إعداد حساب مورّد لمرة واحدة في صفحة "محددات الحسابات الدائنة".


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>إنشاء أمر شراء لمورد مرة واحدة
1. انتقل إلى التدبير وتحديد الموارد > أوامر الشراء > كل أوامر الشراء.
2. انقر فوق "جديد".
3. حدد "نعم" في الحقل "مورد مرة واحدة‬".
    * يتم إنشاء حساب مورّد وتعيينه إلى أمر الشراء تلقائيًا. يتم إنشاء حساب المورّد استنادًا إلى القالب المحدد في علامة التبويب "عام" في صفحة "محددات الحسابات الدائنة‬".  
4. في حقل "الاسم"، اكتب اسمًا للمورّد.
5. انقر فوق "موافق".
    * يمكنك الآن إكمال أمر الشراء ومعالجته كأي أمر آخر. لا توجد أية سمات خاصة تتعلق بكيفية إجراء ذلك. ستحسب الفاتورة حركة مستحقة على حساب المورّد الذي تم إنشاؤه باستخدام الأمر، وستتم معالجة الدفع عندئذٍ. عند الانتهاء من ذلك، يمكن حذف حساب المورّد. يقوم قسم الحسابات الدائنة عادةً بتنفيذ هذه العملية.  


