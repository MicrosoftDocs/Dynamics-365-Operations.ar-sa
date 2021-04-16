---
title: إنشاء قناة على الإنترنت وتحديد سمات القناة
description: يتناول هذا الإجراء إنشاء قناة جديدة عبر الإنترنت وإضافتها إلى التدرج الهرمي للمؤسسات.
author: jashanno
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e28e717dcf594c5079b4b6987331115356b6bdbc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798503"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>إنشاء قناة على الإنترنت وتحديد سمات القناة

[!include [banner](../includes/banner.md)]

يتناول هذا الإجراء إنشاء قناة جديدة عبر الإنترنت وإضافتها إلى التدرج الهرمي للمؤسسات. يجب إنشاء التدرج الهرمي للمؤسسات قبل أن تتمكن من إنشاء قناة جديدة عبر الإنترنت. يستخدم هذا الإجراء شركة بيانات العرض التوضيحي USRT.


## <a name="create-a-new-online-channel"></a>إنشاء قناة جديدة عبر الإنترنت
1. انتقل إلى البيع بالتجزئة والتجارة > القنوات > المتاجر على الإنترنت.
2. انقر فوق جديد.
3. في حقل "الاسم"، اكتب قيمة.
4. في الحقل "المستودع"، أدخل قيمة أو حددها.
5. في حقل "‏‫المنطقة الزمنية للمتجر‬"، حدد خيارًا.
6. في حقل "العميل الافتراضي"، أدخل قيمة أو حددها.
7. في حقل "‏‫دفتر عناوين العميل"، أدخل قيمة أو حددها.
8. في حقل "‏‫شروط الدفع"، أدخل قيمة أو حددها.
9. في الحقل "أسلوب الدفع"، أدخل قيمة أو حددها.
10. في حقل "‏‫ملف تعريف الإخطار بالبريد الإلكتروني"، أدخل قيمة أو حددها.
11. قم بتوسيع قسم الأبعاد المالية.
12. في حقل "BusinessUnit"، أدخل قيمة أو حددها.
    * تعيين القيمة لكافة الأبعاد الافتراضية الأخرى بالمثل.  
13. انقر فوق "حفظ".

## <a name="add-the-online-channel-to-organization-hierarchy"></a>إضافة القناة عبر الإنترنت إلى التدرج الهرمي للمؤسسات
1. قم بإغلاق الصفحة.
2. انتقل إلى إدارة المؤسسة > المؤسسات > التدرجات الهرمية للمؤسسات.
3. في القائمة، قم بالبحث عن السجل المطلوب وحدده.
4. انقر فوق "عرض".
5. انقر فوق "تحرير".
    * يمكنك تحديد أي عقدة تدرج هرمي تقوم من خلالها بإدراج القناة الجديدة التي تريدها.  
6. انقر فوق إدراج.
7. انقر فوق قناة التجارة.
8. انقر فوق موافق.
9. انقر فوق "نشر" لفتح مربع حوار الإسقاط‬.
10. في الحقل "تاريخ السريان"، أدخل تاريخًا ووقتًا.
11. انقر فوق "نشر".

## <a name="configure-orders-for-near-real-time-notification"></a>تكوين الأوامر لاقرب إخطار في الوقت الحقيقي
1. انتقل إلى البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية > المعلمات > معلمات التجارة.
2. قم بتعيين استخدام الخدمة في الوقت الحقيقي لإنشاء أمر التجارة الإلكترونية إلى "نعم".
3. قم بتشغيل جدول توزيع 1070 لمزامنة التغييرات لقاعدة بيانات القناة. 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]