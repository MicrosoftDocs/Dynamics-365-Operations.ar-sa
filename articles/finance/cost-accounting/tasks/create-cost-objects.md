---
title: 'إنشاء كائنات تكلفة  '
description: يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة إلى محاسبة التكاليف عبر موصل بيانات.
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88196ea19488cd8572bf0e7883298317c9c84696
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734119"
---
# <a name="create-cost-objects"></a>إنشاء كائنات تكلفة   

[!include [banner](../../includes/banner.md)]

يوضح هذا الإجراء كيفية إنشاء كائنات التكلفة عن طريق استيراد البُعد المالي لمركز التكلفة إلى محاسبة التكاليف عبر موصل بيانات. تم استخدام شركة بيانات العرض التوضيحي USMF لإنشاء هذا الإجراء. 


## <a name="create-new-cost-objects"></a>إنشاء كائنات تكلفة جديدة
1. انتقل إلى **محاسبة التكاليف > الأبعاد > أبعاد كائن التكلفة**.
2. انقر فوق **جديد**.
3. في الحقل **الاسم**، اكتب قيمة.
4. في الحقل **موصل البيانات لأعضاء البُعد**، أدخل قيمة أو حددها.
5. في حقل **الوصف**، اكتب قيمة.
6. انقر فوق **حفظ**.

## <a name="configure-the-data-connector"></a>تكوين موصل البيانات
1. انقر فوق **تكوين موفر عضو البُعد**.
    * حدد CostCenter لاستيراد بُعد CostCenter إلى محاسبة التكاليف.  
2. حدد "مركز التكلفة" في حقل **اسم البُعد**.
3. انقر فوق **موافق**.

## <a name="import-cost-centers"></a>استيراد مراكز التكلفة
1. انقر فوق **استيراد أعضاء الأبعاد**.
2. انقر فوق **موافق**.

## <a name="view-the-imported-cost-centers"></a>عرض مراكز التكلفة المستوردة
1. انقر فوق **عرض أعضاء الأبعاد**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
