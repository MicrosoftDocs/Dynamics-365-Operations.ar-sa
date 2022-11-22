---
title: 'إنشاء عناصر تكلفة  '
description: هناك عدة طرق لإنشاء عناصر تكلفة في محاسبة التكاليف.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779679"
---
# <a name="create-cost-elements"></a>إنشاء عناصر تكلفة   

[!include [banner](../../includes/banner.md)]

هناك عدة طرق لإنشاء عناصر تكلفة في محاسبة التكاليف. يوضح هذا الإجراء كيفية إنشاء عناصر التكلفة عن طريق استيراد الحسابات الرئيسية عبر موصل بيانات. تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء. يتم استخدام هذا الإجراء لميزة محاسبة التكاليف‬ التي تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="create-new-cost-elements"></a>إنشاء عناصر تكلفة جديدة
1. انتقل إلى **محاسبة التكاليف > الأبعاد > أبعاد عنصر التكلفة**.
2. انقر فوق **جديد**.
3. في الحقل **الاسم**، اكتب قيمة.
4. في الحقل **موصل البيانات لأعضاء البُعد**، أدخل قيمة أو حددها.
5. في حقل **الوصف**، اكتب قيمة.
6. انقر فوق **حفظ**.

## <a name="configure-the-data-connector"></a>تكوين موصل البيانات
1. انقر فوق **تكوين موفر عضو البُعد**.
2. في حقل **مخطط الحسابات**، أدخل قيمة أو حددها.
    * حدد **مشترك** لاستخدام مخطط الحسابات المشترك.  
3. انقر فوق **جديد**.
4. في القائمة، قم بوضع علامة للصف المحدد.
    * يمكنك تطبيق عوامل التصفية على الحسابات للوفاء بالمعايير.  
5. في حقل **من الحساب الرئيسي‬‬**، أدخل قيمة أو حددها.
6. في حقل **إلى الحساب الرئيسي‬‬‬‬**، أدخل قيمة أو حددها.
7. انقر فوق **موافق**.

## <a name="import-main-accounts"></a>استيراد الحسابات الرئيسية
1. انقر فوق **استيراد أعضاء الأبعاد**.
    * سيتم استيراد الحسابات الرئيسية إلى محاسبة التكاليف وسيتم استخدامها كعناصر تكلفة.  
2. انقر فوق **موافق**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>عرض الحسابات المستوردة كعناصر تكلفة
1. انقر فوق **عرض أعضاء الأبعاد**.
    * اعرض حسابات دفتر الأستاذ التي تم استيرادها كعناصر تكلفة في شركتك والتي يمكن للتكاليف أن تتدفق إليها.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
