---
title: .الإبلاغ كمنتهٍ إلى موقع غير خاضع للتحكم من جهاز بطاقة الوظيفة
description: يوضح هذا الموضوع عملية إكمال المنتجات المنتهية في أمر إنتاج إلى المخزون عندما تتحكم لوحة الترخيص في الموقع.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995132"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>.الإبلاغ كمنتهٍ إلى موقع غير خاضع للتحكم من جهاز بطاقة الوظيفة 

تُكمل العملية التي يُطلق عليها الإبلاغ كُمنتهي المنتجات المنتهية في أمر إنتاج إلى المخزون. إذا تم تمكين المنتج المنتهي لعمليات المستودع المتقدمة، يتم الإبلاغ عن المنتج كُمنتهي إلى موقع يٌسمى موقع مُخرجات الإنتاج. للحصول على معلومات حول إعداد موقع مُخرجات الإنتاج، راجع [موقع مُخرجات الإنتاج](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

يجب عليك تحديد رقم لوحة الترخيص الحالية لإنهاء هذه المهمة. إذا تم إعداد موقع مُخرجات الإنتاج ليتم تعقبه بواسطة لوحة الترخيص، فمن ثم يجب تضمين رقم لوحة الترخيص عندما يتم الإبلاغ عن موقع مُخرجات الإنتاج كمُنتهِ. يكون حقل **لوحة الترخيص** مرئيًا في مطالبة **تقرير التقدم** على صفحة **جهاز بطاقة الوظيفة**. ولا يظهر هذا الحقل إلا في مطالبة **تقرير التقدم** عند الإبلاغ عن آخر عملية لأمر الإنتاج. ويظهر هذا الحقل فقط إذا تم تمكين الصنف الخاص بأمر الإنتاج لعمليات إدارة المستودع. 