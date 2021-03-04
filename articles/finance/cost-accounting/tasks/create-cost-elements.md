---
title: 'إنشاء عناصر تكلفة  '
description: هناك عدة طرق لإنشاء عناصر تكلفة في محاسبة التكاليف.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87f93fd7c1c42045274d6b89847b27e93614d9a4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/13/2020
ms.locfileid: "4440084"
---
# <a name="create-cost-elements"></a>إنشاء عناصر تكلفة   

[!include [banner](../../includes/banner.md)]

هناك عدة طرق لإنشاء عناصر تكلفة في محاسبة التكاليف. يوضح هذا الإجراء كيفية إنشاء عناصر التكلفة عن طريق استيراد الحسابات الرئيسية عبر موصل بيانات. تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء. يتم استخدام هذا الإجراء لميزة محاسبة التكاليف‬ التي تمت إضافتها في Dynamics 365 for Operations، الإصدار 1611.


## <a name="create-new-cost-elements"></a>إنشاء عناصر تكلفة جديدة
1. انتقل إلى محاسبة التكاليف > الأبعاد > أبعاد عنصر التكلفة.
2. انقر فوق "جديد".
3. في حقل "الاسم"، اكتب قيمة.
4. في الحقل "موصل البيانات لأعضاء البُعد‬"، أدخل قيمة أو حددها.
5. في وصف الحقل، اكتب قيمة.
6. انقر فوق "حفظ".

## <a name="configure-the-data-connector"></a>تكوين موصل البيانات
1. انقر فوق "تكوين موفر عضو البُعد".
2. في الحقل "دليل الحسابات"، أدخل قيمة أو حددها.
    * حدد "مشترك" لاستخدام دليل الحسابات المشترك.  
3. انقر فوق "جديد".
4. في القائمة، قم بوضع علامة للصف المحدد.
    * يمكنك تطبيق عوامل التصفية على الحسابات للوفاء بالمعايير.  
5. في الحقل "من الحساب الرئيسي‬‬"، أدخل قيمة أو حددها.
6. في الحقل "إلى الحساب الرئيسي‬‬‬‬"، أدخل قيمة أو حددها.
7. انقر فوق "موافق".

## <a name="import-main-accounts"></a>استيراد الحسابات الرئيسية
1. انقر فوق "استيراد أعضاء الأبعاد".
    * سيتم استيراد الحسابات الرئيسية إلى محاسبة التكاليف وسيتم استخدامها كعناصر تكلفة.  
2. انقر فوق "موافق".

## <a name="view-the-imported-accounts-as-cost-elements"></a>عرض الحسابات المستوردة كعناصر تكلفة
1. انقر فوق "عرض أعضاء الأبعاد".
    * اعرض حسابات دفتر الأستاذ التي تم استيرادها كعناصر تكلفة في شركتك والتي يمكن للتكاليف أن تتدفق إليها.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]