---
title: إنشاء أمر شراء لمورد مرة واحدة
description: يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 76915772809d736cac9e8a9439d9e693a4490eec
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204897"
---
# <a name="create-a-purchase-order-for-a-one-time-supplier"></a>إنشاء أمر شراء لمورد مرة واحدة

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إنشاء أمر شراء لمورّد لمرة واحدة. يتم إنشاء المورّد مع أمر الشراء بشكل تلقائي، بدلاً من إنشاء حساب المورّد يدويًا. وعادة ما يتم إنشاء أوامر الشراء عن طريق وكيل شراء. يمكن استخدام المثال المعروض في هذا الدليل في شركة بيانات العرض التوضيحي USMF. يجب إعداد حساب مورّد لمرة واحدة في صفحة "محددات الحسابات الدائنة".


## <a name="create-a-purchase-order-for-a-one-time-supplier"></a>إنشاء أمر شراء لمورد مرة واحدة
1. انتقل إلى التدبير وتحديد الموارد > أوامر الشراء > كل أوامر الشراء.
2. انقر فوق "جديد".
3. حدد "نعم" في الحقل "مورد مرة واحدة‬".
    * يتم إنشاء حساب مورّد وتعيينه إلى أمر الشراء تلقائيًا. يتم إنشاء حساب المورّد استنادًا إلى القالب المحدد في علامة التبويب "عام" في صفحة "محددات الحسابات الدائنة‬".  
4. في حقل "الاسم"، اكتب اسمًا للمورّد.
5. انقر فوق "موافق".
    * يمكنك الآن إكمال أمر الشراء ومعالجته كأي أمر آخر. لا توجد أية سمات خاصة تتعلق بكيفية إجراء ذلك. ستحسب الفاتورة حركة مستحقة على حساب المورّد الذي تم إنشاؤه باستخدام الأمر، وستتم معالجة الدفع عندئذٍ.

