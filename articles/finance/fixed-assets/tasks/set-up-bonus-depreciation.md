---
title: إعداد إهلاك إضافي
description: يوضح هذا الإجراء كيفية إنشاء بدل إهلاك خاص وإقرانه بدفتر أصول ثابتة.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetGroup, AssetGroupBookSetup, AssetGroupSetupBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788cddf4d822fe3d3d6a33e83d7b30f32f4b6b9c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176197"
---
# <a name="set-up-bonus-depreciation"></a>إعداد إهلاك إضافي

[!include [task guide banner](../../includes/task-guide-banner.md)]

يوضح هذا الإجراء كيفية إنشاء بدل إهلاك خاص وإقرانه بدفتر أصول ثابتة. إنه يستخدم دور المحاسب وبيانات العرض التوضيحي في الكيان القانوني USMF.


## <a name="create-a-special-depreciation-allowance"></a>إنشاء بدل إهلاك خاص
1. انتقل إلى الأصول الثابتة > إعداد > بدل الإهلاك الخاص.
2. انقر فوق "جديد".
3. في الحقل "بدل الإهلاك الخاص"، اكتب قيمة.
4. في وصف الحقل، اكتب قيمة.
5. في الحقل "النسبة المئوية‬"، أدخل رقمًا.
    * إذا لم تتم الإشارة إلى نسبة مئوية، فعيّن مبلغًا.  

## <a name="associate-a-special-depreciation-allowance-with-a-fixed-asset-group-book"></a>إقران بدل إهلاك خاص بدفتر مجموعة الأصول الثابتة
1. انتقل إلى الأصول الثابتة > إعداد > مجموعات الأصول الثابتة‬.
2. في القائمة، حدد مجموعة الأصول الثابتة المقترنة ببدل الإهلاك الخاص.
3. انقر فوق "الدفاتر".
4. في القائمة، حدد الدفتر المقترن ببدل الإهلاك الخاص.
5. انقر فوق "بدل الإهلاك الخاص".
6. انقر فوق "جديد".
7. في الحقل "بدل الإهلاك الخاص"، أدخل قيمة أو حددها.
    * يأتي المبلغ الافتراضي لمبلغ النسبة المئوية من إعداد بدل الإهلاك الخاص.‬  
8. في حقل "الأولوية"، أدخل رقمًا.
