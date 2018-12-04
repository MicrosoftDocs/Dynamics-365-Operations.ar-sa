--- 
title: "إنشاء أمر شراء لمورد مرة واحدة"
description: "يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2d4dabaf6e1d79cbd626294ee4e327f2725a5e43
ms.contentlocale: ar-sa
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>إنشاء أمر شراء لمورد مرة واحدة

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة. يتم إنشاء المورّد مع أمر الشراء بشكل تلقائي، بدلاً من إنشاء حساب المورّد يدويًا. وعادة ما يتم إنشاء أوامر الشراء عن طريق وكيل شراء. يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF. يجب إعداد حساب مورّد لمرة واحدة في صفحة "محددات الحسابات الدائنة".


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>إنشاء أمر شراء لمورد مرة واحدة
1. انتقل إلى التدبير وتحديد الموارد > أوامر الشراء > كل أوامر الشراء.
2. انقر فوق "جديد".
3. حدد "نعم" في الحقل "مورد مرة واحدة‬".
    * يتم إنشاء حساب مورّد وتعيينه إلى أمر الشراء تلقائيًا. يتم إنشاء حساب المورّد استنادًا إلى القالب المحدد في علامة التبويب "عام" في صفحة "محددات الحسابات الدائنة‬".  
4. في حقل "الاسم"، اكتب اسمًا للمورّد.
5. انقر فوق "موافق".
    * يمكنك الآن إكمال أمر الشراء ومعالجته كأي أمر آخر. لا توجد أية سمات خاصة تتعلق بكيفية إجراء ذلك. ستحسب الفاتورة حركة مستحقة على حساب المورّد الذي تم إنشاؤه باستخدام الأمر، وستتم معالجة الدفع عندئذٍ. عند الانتهاء من ذلك، يمكن حذف حساب المورّد. يقوم قسم الحسابات الدائنة عادةً بتنفيذ هذه العملية.  


