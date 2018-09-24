---
title: "إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)"
description: "يشرح هذا الموضوع كيفية إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: ar-sa
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a>إدارة التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN)

[!include [banner](../includes/banner.md)]

تؤدي عملية التحقق من صحة حساب رقم الحساب البنكي الدولي (IBAN) إلى زيادة مقدار عملية التحقق من الصحة التي يتم تنفيذها عند إضافة IBAN إلى حساب بنكي.

يتم تخزين بنية IBAN في Microsoft Dynamics 365 for Finance and Operation، ويتم تحميلها تلقائيًا عندما تستخدم IBAN للمرة الأولى على الحسابات البنكية. يعتبر رقم الحساب البنكي جزءًا من البنية المعرفة لرقم IBAN. استنادًا إلى هذه البنية، إذا كان موضع وطول رقم الحساب في IBAN غير متطابق مع الموضع المحدد في البنية الخاصة بكل بلد أو منطقة، فستتلقى رسائل تحذير.

## <a name="set-up-iban-structures"></a>إعداد بنى IBAN‬

1. انتقل إلى **إدارة النقد والبنك \> الإعداد \> بنى IBAN**.
2. لاحظ أن إعداد بنى IBAN لكل بلد أو منطقة قم تم بشكل تلقائي.
3. إذا كان يجب تخصيص البنى لبلد أو منطقة معينة، فيمكنك تحريرها.
4. ستكون تعريفات البنية جزءًا من كل إصدار جديد. يمكنك استخدام القائمة **إعادة تعيين البنى‬** لتحميل أحدث التعريفات بعد كل تحديث.

## <a name="validate-the-iban-structure-in-a-bank-account"></a>التحقق من صحة IBAN في بنية الحساب

1. انتقل إلى **إدارة النقد والبنوك \> الحسابات البنكية \> الحسابات البنكية**.
2. أنشئ حسابًا بنكيًا.
3. على علامة التبويب السريعة **معلومات إضافية**، أدخل IBAN.

    إذا كان موضع وطول رقم الحساب في IBAN غير متطابق مع الموضع المحدد في البنية الخاصة بكل بلد أو منطقة، فستتلقى رسالة تحذير. لا يمكنك المتابعة إذا كان طول IBAN غير متوافق مع الطول في بنية IBAN.

    تتأكد أيضًا عملية من الصحة من أن رقم الحساب البنكي يتطابق مع جزء IBAN الذي يمثل رقم الحساب البنكي. إذا لم يكن رقم الحساب البنكي مطابقًا، تتلقى رسالة تحذير. هذه الرسالة عبارة عن تحذير فقط. يمكنك المتابعة حتى لو لم يكن رقم الحساب البنكي متطابقًا.

