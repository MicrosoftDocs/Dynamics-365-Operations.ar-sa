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
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fc935b346adfe9548b024f22a2fbfb5af9a802d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/16/2020
ms.locfileid: "4421764"
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

