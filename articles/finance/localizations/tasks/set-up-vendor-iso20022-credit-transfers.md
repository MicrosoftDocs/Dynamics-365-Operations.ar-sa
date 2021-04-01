---
title: إعداد المورّدين والحسابات البنكية للمورّدين لتحويلات الائتمان ISO20022
description: يوضح هذا الإجراء كيفية إعداد المورّد والمعلومات المحددة الخاصة بالحساب البنكي للمورّد والمطلوبة لتحويل الائتمان ISO20022 أو أي عملية أخرى لإنشاء ملف دفع المورّد.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8b3a16d614efed0aafbf13fc59c17ab568811d82
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222029"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>إعداد المورّدين والحسابات البنكية للمورّدين لتحويلات الائتمان ISO20022

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إعداد المورّد والمعلومات المحددة الخاصة بالحساب البنكي للمورّد والمطلوبة لتحويل الائتمان ISO20022 أو أي عملية أخرى لإنشاء ملف دفع المورّد. 

شركة بيانات العرض التوضيحي التي تم استخدامها لإنشاء هذا الإجراء هي DEMF.
هذا هو الإجراء الرابع من ضمن الإجراءات الخمسة، هدفه توضيح عملية معالجة مدفوعات المورّد باستخدام تكوينات التقارير الإلكترونية. يتم استخدام هذا الإجراء لميزة تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="set-up-bank-details"></a>إعداد تفاصيل البنك
1. انتقل إلى الحسابات الدائنة > الموردون > كافة الموردين.
2. استخدم عامل التصفية السريع للبحث عن السجلات. على سبيل المثال، قم بإجراء التصفية على حقل "حساب المورّد" بقيمة "DE-001".
3. انقر فوق DE-001 لفتح تفاصيل المورّد.
4. في جزء الإجراءات، انقر فوق "المورّد".
5. انتقل إلى "الحسابات البنكية".
6. انقر فوق "تحرير".
    * إذا لم يتوفر أي حساب بنكي، فتحتاج إلى إنشاء واحد جديد.  
7. في الحقل "كود التحويل الإلكتروني‬"، اكتب "COBADEFFXXX".
8. في الحقل "IBAN"، اكتب ''DE36200400000628808808".
9. قم بإغلاق الصفحة.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>إعداد طريقة دفع للمورّد
1. انقر فوق "تحرير".
2. قم بتوسيع أو طي قسم الدفع.
3. في الحقل "طريقة الدفع"، انقر فوق زر القائمة المنسدلة لفتح البحث.
4. في القائمة، انقر فوق الارتباط في الصف سيبا CT.
5. انقر فوق "حفظ".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]