---
title: .الإبلاغ كمنتهٍ إلى موقع غير خاضع للتحكم من جهاز بطاقة الوظيفة
description: يصف هذا الموضوع عملية إكمال المنتجات المنتهية في أمر إنتاج إلى المخزون عندما تتحكم لوحة الترخيص في الموقع.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211159"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>.الإبلاغ كمنتهٍ إلى موقع غير خاضع للتحكم من جهاز بطاقة الوظيفة 

تُكمل العملية التي يُطلق عليها الإبلاغ كُمنتهي المنتجات المنتهية في أمر إنتاج إلى المخزون. إذا تم تمكين المنتج المنتهي لعمليات المستودع المتقدمة، يتم الإبلاغ عن المنتج كُمنتهي إلى موقع يٌسمى موقع مُخرجات الإنتاج. للحصول على معلومات حول إعداد موقع مُخرجات الإنتاج، راجع [موقع مُخرجات الإنتاج](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

إذا كان موقع إخراج المنتج عبارة عن موقع يتم التحكم فيه بواسطة لوحة ترخيص، فإنه يجب توفير لوحة ترخيص عند الإبلاغ كمنته. يكون حقل **لوحة الترخيص** مرئيًا في مطالبة **تقرير التقدم** على صفحة **جهاز بطاقة الوظيفة**. يكون الحقل مرئيًا فقط في مطالبة **تقرير التقدم** عند تقديم تقرير عن العملية الأخيرة لأمر الإنتاج ويتم تمكين صنف أمر الإنتاج لعمليات إدارة المستودع. 

هناك خياران لتوفير لوحة الترخيص
- يقوم المستخدم بتحديد لوحة ترخيص موجودة في حقل لوحة الترخيص.
- يتم إنشاء لوحة الترخيص تلقائيًا من تسلسل رقمي ويتم تعيينها افتراضيًا إلى حقل لوحة الترخيص.

يتم تكوين خيار الحصول على لوحة الترخيص التي تم إنشاؤها تلقائيًا عن طريق تحديد الخيار **إنشاء لوحة ترخيص** في الصفحة **تكوين بطاقة الوظيفة للأجهزة**.
