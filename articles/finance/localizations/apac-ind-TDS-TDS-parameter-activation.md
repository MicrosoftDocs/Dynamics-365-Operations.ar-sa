---
title: إعداد معلمات TDS
description: يشرح هذا الموضوع كيفية تعيين المعلمات لتنشيط وظيفة الضريبة المخصومة في المصدر (TDS) في حركات محددة. هذه الخطوة ضرورية لاستخدام ميزة الضريبة المخصومة في المصدر TDS.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: dda276b7d634317aae26728f7d9f51af9ccfb896
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022996"
---
# <a name="set-the-tds-parameters"></a>إعداد معلمات TDS

[!include [banner](../includes/banner.md)]

يشرح هذا الموضوع كيفية تعيين المعلمات لتنشيط وظيفة الضريبة المخصومة في المصدر (TDS) في حركات محددة. هذه الخطوة ضرورية لاستخدام ميزة الضريبة المخصومة في المصدر TDS.

1. انتقل إلى **دفتر الأستاذ العام \> إعداد دفتر الأستاذ‬ \> معلمات دفتر الأستاذ العام**.
2. في علامة التبويب **الضرائب المباشرة**، في القسم **الضريبة المخصومة في المصدر**، قم بتعيين الخيار **تنشيط TDS** إلى **نعم** لتنشيط وظيفة TDS، والصفحات والحقول التي يتم استخدامها له.
3. قم بتعيين الخيار **الفاتورة** على **نعم** لتنشيط الحقول المستخدمة في حساب وخصم TDS على مستوى الفاتورة.
4. قم بتعيين الخيار **المدفوعات** على **نعم** لتنشيط الحقول المستخدمة في حساب وخصم TDS على مستوى المدفوعات.

    [![علامة التبويب الضرائب المباشرة](./media/apac-ind-TDS-1.png)](./media/apac-ind-TDS-1.png)

5. من علامة التبويب **التسلسلات الرقمية**، ابحث عن الصف الذي يتم تعيين الحقل **المرجع** فيه إلى **دفع ضريبة الخصم**. ثم في الحقل **كود التسلسل الرقمي**، كود التسلسل الرقمي. يتم استخدام كود التسلسل الرقمي لإنشاء أرقام إيصالات لعملية تسوية TDS الدورية.

    > [!NOTE]
    > لتشغيل عملية تسوية TDS الدورية، انتقل إلى **الضريبة \> الإقرارات \> ضريبة الخصم \> دفع ضريبة الخصم**.

    [![علامة التبويب التسلسلات الرقمية](./media/apac-ind-TDS-2.png)](./media/apac-ind-TDS-2.png)

6. قم بإغلاق الصفحة.