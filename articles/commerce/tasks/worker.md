---
title: " تكوين عامل"
description: يوضح هذا الإجراء كيفية تكوين عامل كمندوب مبيعات مؤهل للحصول على عمولة على المبيعات في نقطة البيع.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 73c200f7f6ff0aa5672e50c539bfaa5e30213185
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003593"
---
# <a name="configure-a-worker"></a> تكوين عامل

[!include [banner](../includes/banner.md)]

يوضح هذا الإجراء كيفية تكوين عامل كمندوب مبيعات مؤهل للحصول على عمولة على المبيعات في نقطة البيع. يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.


## <a name="create-a-commission-sales-group-for-the-worker"></a>إنشاء مجموعة مبيعات العمولة‬ للعامل
1. انتقل إلى المبيعات والتسويق > العمولات > مجموعات المبيعات.
    * يمكن تعيين العاملين إلى مجموعة مبيعات واحدة أو أكثر. في نقطة البيع، يمكنك اختيار أي مجموعة مبيعات تحتوي على عاملين من دفتر العناوين الخاص بالمتجر.  
2. انقر فوق "جديد".
3. في الحقل "المجموعة"، اكتب قيمة.
4. في حقل "الاسم"، اكتب قيمة.
5. انقر فوق "حفظ".
6. في جزء "الإجراءات"، انقر فوق "عام".
7. انقر فوق "مندوب المبيعات".
    * يمكن أن تحتوي مجموعة مبيعات على عامل واحد أو أكثر. يمكن تقسيم العمولات‬ بين العمال استنادًا إلى كيفية تعريف حصة العمولة.  
8. في الحقل "الاسم"، أدخل قيمة أو حددها.
9. في الحقل "حصة العمولة‬"، أدخل رقمًا.
10. انقر فوق "حفظ".
11. قم بإغلاق الصفحة.
12. قم بإغلاق الصفحة.

## <a name="assign-the-workers-default-sales-group"></a>تعيين مجموعة المبيعات الافتراضية إلى العاملين
1. انتقل إلى البيع بالتجزئة والتجارة > الموظفون > العامون.
2. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
3. في القائمة، انقر فوق الارتباط في الصف المحدد.
4. انقر فوق علامة التبويب Commerce.
    * يمكن تعيين عامل إلى مجموعة مبيعات افتراضية. ستُضاف مجموعة المبيعات الافتراضية تلقائيًا إلى بنود المبيعات في نقطة البيع إذا تم تمكين الخيار في ملف تعريف الوظائف الخاص بالمتجر.  
5. انقر فوق "تحرير".
6. في حقل "المجموعة الافتراضية"، أدخل قيمة أو حددها.
7. انقر فوق "حفظ".



[!INCLUDE[footer-include](../../includes/footer-banner.md)]