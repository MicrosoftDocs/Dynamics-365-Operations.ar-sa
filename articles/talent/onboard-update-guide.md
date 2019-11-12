---
title: تحديث أدلة الإعداد في Dynamics 365 Talent - Onboard
description: يشرح هذا الموضوع كيفية تحديث أدلة الإعداد في Microsoft Dynamics 365 Talent - Onboardوكيفية دفع التغييرات إلى الأدلة الموجودة.
author: andreabichsel
manager: ''
ms.date: 06/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-21
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 071aa79ea75e9a94187dd74dabab940e2cce0f92
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551946"
---
# <a name="update-onboarding-guides-in-dynamics-365-talent---onboard"></a>تحديث أدلة الإعداد في Dynamics 365 Talent - Onboard

[!include [banner](includes/banner.md)]

إذا كان يتعين عليك إجراء تغييرات في أدلة الإعداد في Microsoft Dynamics 365 Talent: Onboard، فيمكنك تحديثها ودفع التغييرات، حتى لو سبق لك إرسال الأدلة. هناك خياران لتحديث دليل الإعداد:

- تحرير دليل الإعداد مباشرةً، ثم حفظ التغييرات.
- تحرير قالب الإعداد، ثم دفع التغييرات إلى جميع أدلة الإعداد التي تم إنشاؤها منه.

## <a name="edit-an-onboarding-guide-directly"></a>تحرير دليل الإعداد مباشرة

1. في القائمة اليمنى، حدد **الأدلة**.
2. حدد الدليل الذي تريد تحريره.
3. أدخل جميع التغييرات المطلوبة، ثم حدد الزر **حفظ** (رمز القرص).

    ![[حفظ التغييرات إلى دليل إعداد](./media/onboard-save.png)](./media/onboard-save.png)

يرسل Onboard بشكل تلقائي إلى الموظف الجديد رسالة إلكترونية تشرح التغييرات. تظهر علامة حمراء **جديد** إلى جانب كل تغيير لتسهيل التعرف عليه.

## <a name="update-multiple-guides-by-editing-the-onboarding-template"></a>تحديث أدلة إعداد متعددة عن طريق تحرير قالب الإعداد

1. في القائمة اليمنى، حدد **القوالب**.
2. ضمن **القوالب الخاصة بي**، حدد القالب الذي تريد تحريره.
3. أدخل جميع التغييرات المطلوبة، ثم حدد الزر **حفظ** (رمز القرص).
4. لدفع التغييرات إلى جميع الأدلة التي تستند إلى القالب، حدد **دفع هذه التغييرات**.

    ![[دفع التغييرات في قالب إعداد إلى كافة الأدلة التي تم إنشاؤها منه](./media/onboard-push-changes.png)](./media/onboard-push-changes.png)

ستكون التغييرات مرئية للمستخدمين الجدد الذين يفتحون أدلة الإعداد. ومع ذلك، لن يرسل Onboard تنبيهات البريد الإلكتروني إلى الموظفين الجدد لإعلامهم بأن دليل الإعداد قد تغير. تظهر علامة حمراء **جديد** إلى جانب كل تغيير لتسهيل التعرف عليه. 
