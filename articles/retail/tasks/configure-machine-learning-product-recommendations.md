---
title: " تكوين توصيات المنتجات المدعومة بنظام التعلم الآلي"
description: يقوم هذا الإجراء بتحديث البيانات في مخزن الكيانات المستخدم من قبل نظام التعلم الآلي الذي يدعم التوصيات، ثم يمكّن توصيات المنتجات على عملاء نقطة البيع.
author: ashishmsft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BIMeasurementDeployManagementEntityStore, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 700af913f18e23c66db53a92033def06818af1ec
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "348516"
---
# <a name="configure-machine-learning-powered-product-recommendations"></a> تكوين توصيات المنتجات المدعومة بنظام التعلم الآلي

[!include[task guide banner](../includes/task-guide-banner.md)]

يقوم هذا الإجراء بتحديث البيانات في مخزن الكيانات المستخدم من قبل نظام التعلم الآلي الذي يدعم التوصيات، ثم يمكّن توصيات المنتجات على عملاء نقطة البيع. ويستخدم هذا الإجراء شركة USRT في بيانات العرض التوضيحي.

1. انتقل إلى إدارة النظام > الإعداد > متجر الكيانات‬.
2. في القائمة، ابحث عن السجل "RetailSales" وحدده.
3. انقر فوق "تحديث".
4. انقر فوق "موافق".
5. قم بإغلاق الصفحة.
6. انتقل إلى البيع بالتجزئة والتجارة > إعداد المراكز الرئيسية > المعلمات > معلمات البيع بالتجزئة‬.
7. انقر فوق علامة التبويب "التعلم الآلي".
8. حدد "نعم" في حقل "تمكين توصيات المنتجات‬".
    * إذا تلقيت الرسالة "تعذر استرداد نماذج التوصية"، فسبب ذلك يعود إلى تحديث مخزن الكيانات مؤخرًا دون أن ينتهي النظام من استيعاب البيانات الجديدة. انتظر من ساعتين إلى ثلاث ساعات وحاول مرة أخرى.  
9. انقر فوق "حفظ".
10. قم بإغلاق الصفحة.

