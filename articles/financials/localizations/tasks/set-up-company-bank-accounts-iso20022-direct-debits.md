---
title: إعداد الحسابات البنكية للشركة للديون المباشرة ISO20022
description: تنقلك هذه المهمة عبر عملية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملفات دفع العميل.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89c4a8d3cb504df97bad5679bf12b3cdb5931d95
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852564"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>إعداد الحسابات البنكية للشركة للديون المباشرة ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

تنقلك هذه المهمة عبر عملية إعداد المعلومات المحددة الخاصة بالحساب البنكي للشركة والمطلوبة لإنشاء ملفات دفع العميل. يستخدم هذا الإجراء تنسيق الدين المباشر ISO 20022 كمثال. قد تتطلب تنسيقات أخرى معلومات إعداد إضافية، مثل "معرف الشركة" أو "كود الفرز".



تم إنشاء هذه المهمة باستخدام شركة بيانات العرض التوضيحي DEMF.



هذا هو الإجراء الثاني من ضمن خمسة إجراءات هدفها توضيح عملية معالجة مدفوعات العميل باستخدام تكوينات التقارير الإلكترونية.


## <a name="set-up-the-iban-and-swift-codes"></a>إعداد أكواد IBAN والتحويل الإلكتروني‬
1. انتقل إلى إدارة النقد والبنوك > الحسابات البنكية.
2. استخدم عامل التصفية السريع لإجراء التصفية على الحقل "الحساب البنكي‬" بالقيمة "DEMF OPER''.
3. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * على سبيل المثال، انقر فوق 'DEMF OPER' لفتح تفاصيل الحساب البنكي.  
4. انقر فوق "تحرير".
5. ‏‫قم بتوسيع المقطع "تعريف إضافي" أو طيّه.
6. في الحقل "IBAN‬"، اكتب قيمة.
    * على سبيل المثال، أدخل "DE89370400440532013000".  
7. في الحقل "كود التحويل الإلكتروني‬"، اكتب قيمة.
    * على سبيل المثال، أدخل "DEUTDEFF".    لاحظ أن SWIFT \ BIC غير إلزامي للعديد من تنسيقات الدفع، لكن من المستحسن أن يتم تسجيله لحساب بنكي.  
8. انقر فوق "حفظ".

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>إعداد حساب بنكي للكيان القانوني
1. انتقل إلى إدارة المؤسسة > المؤسسات > الكيانات القانونية.
2. انقر فوق "تحرير".
3. ‏‫قم بتوسيع المقطع "معلومات الحساب البنكي‬" أو طيّه.
4. في الحقل "الحساب البنكي"، انقر فوق زر القائمة المنسدلة لفتح البحث.
5. في القائمة، انقر فوق الارتباط في الصف المحدد.
    * على سبيل المثال، حدد الحساب البنكي "DEMF OPER".  
6. انقر فوق "حفظ".

