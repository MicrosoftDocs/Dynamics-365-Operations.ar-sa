---
title: "تكوينات طلب المورّد"
description: "يصف هذا الموضوع الحقول المطلوبة تعبئتها في طلب مورد جديد."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: e45f8698e69a2a870c7c00f91622216deb4cb38a
ms.contentlocale: ar-sa
ms.lasthandoff: 12/14/2017

---

# <a name="vendor-request-configurations"></a>تكوينات طلب المورّد
[!include[banner](../includes/banner.md)]

لإكمال طلب مورد، يجب على جهة اتصال المورد إكمال معالج تسجيل المورد المتوقع.

في نموذج **‏‫تكوينات طلب المورّد‬**، يمكنك إنشاء ملفات تعريف تحدد الحقول المطلوبة والحقول المرئية في معالج تسجيل المورد المتوقع.

سيتم بدء تشغيل معالج المورد بطلب مستخدم المورد المتوقع في البلد/المنطقة التي يقوم المورد بمباشرة أعماله فيها. تحدد هذه المعلومات التكوين القابل للتطبيق. إذا يتم تحديد أي تكوين محدد لبلد/منطقة، فسيتم استخدام تكوين افتراضي.

### <a name="set-up-a-vendor-request-configuration"></a>إعداد تكوين طلب المورّد

بشكل افتراضي، يتوفر تكوين مورد في نموذج تكوينات طلب المورد.

يتعذر تحديد البلد/المناطق للتكوين الافتراضي، وبالتالي لا يمكن تغيير قسم **البلاد/المناطق**.

1.  انقر فوق **‬‏‫التدبير وتحديد الموارد‬‏‫** > **الإعداد** > **الموردون**، ثم انقر فوق **تكوينات طلب المورد**.
2.  انقر فوق علامة التبويب **الحقول** لتعيين حالة الحقول المسرودة.
-   مخفي (غير مرئي)
-   معروض (مرئي لكن ليس إلزامياً)
-   مطلوب (مرئي وإلزامي)
3.  انقر فوق علامة التبويب **المحتوى** لتحديد إذا كان سيتم عرض النص في المعالج، وإذا كان سيقر مستخدم المورد المتوقع بالموافقة على هذا قبل الانتقال إلى الخطوة التالية في المعالج. ستتم المطالبة بالإقرار بأي بنود وشروط يجب أن يقبلها المستخدم للمتابعة.

يمكنك أيضا إدخال رسالة تأكيد ستظهر عند الانتهاء من المعالج، ويمكنك إضافة استبيان أو أكثر.

### <a name="create-a-vendor-configuration-for-a-specific-countryregion"></a>إنشاء تكوين مورد لبلد/منطقة محددة
1.  انقر فوق **‬‏‫التدبير وتحديد الموارد‬‏‫** > **الإعداد** > **الموردون**، ثم انقر فوق **تكوينات طلب المورد**.
2.  انقر فوق **جديد** لإنشاء تكوين جديد وقم بتوفير اسمًا للتكوين.
3.  انقر فوق **حفظ**.
4.  افتح علامة التبويب **البلاد/المناطق** لتحديد البلد/المنطقة التي ستستخدم في التكوين.
5.  أكمل التكوين باتباع الإرشادات الخاصة بالتكوين الافتراضي.

