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

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="cc1f7-103">.الإبلاغ كمنتهٍ إلى موقع غير خاضع للتحكم من جهاز بطاقة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="cc1f7-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="cc1f7-104">تُكمل العملية التي يُطلق عليها الإبلاغ كُمنتهي المنتجات المنتهية في أمر إنتاج إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="cc1f7-105">إذا تم تمكين المنتج المنتهي لعمليات المستودع المتقدمة، يتم الإبلاغ عن المنتج كُمنتهي إلى موقع يٌسمى موقع مُخرجات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="cc1f7-106">للحصول على معلومات حول إعداد موقع مُخرجات الإنتاج، راجع [موقع مُخرجات الإنتاج](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="cc1f7-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="cc1f7-107">إذا كان موقع إخراج المنتج عبارة عن موقع يتم التحكم فيه بواسطة لوحة ترخيص، فإنه يجب توفير لوحة ترخيص عند الإبلاغ كمنته.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-107">If the production output location is license plate controlled, then a license plate must be provided when reporting as finished.</span></span> <span data-ttu-id="cc1f7-108">يكون حقل **لوحة الترخيص** مرئيًا في مطالبة **تقرير التقدم** على صفحة **جهاز بطاقة الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-108">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="cc1f7-109">يكون الحقل مرئيًا فقط في مطالبة **تقرير التقدم** عند تقديم تقرير عن العملية الأخيرة لأمر الإنتاج ويتم تمكين صنف أمر الإنتاج لعمليات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-109">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order and the item for the production order is enabled for the warehouse management processes.</span></span> 

<span data-ttu-id="cc1f7-110">هناك خياران لتوفير لوحة الترخيص</span><span class="sxs-lookup"><span data-stu-id="cc1f7-110">There are two options for providing the license plate</span></span>
- <span data-ttu-id="cc1f7-111">يقوم المستخدم بتحديد لوحة ترخيص موجودة في حقل لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-111">The user is selecting an existing license plate in the license plate field.</span></span>
- <span data-ttu-id="cc1f7-112">يتم إنشاء لوحة الترخيص تلقائيًا من تسلسل رقمي ويتم تعيينها افتراضيًا إلى حقل لوحة الترخيص.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-112">The license plate is automatically generated from a number sequence and defaulted to the license plate field.</span></span>

<span data-ttu-id="cc1f7-113">يتم تكوين خيار الحصول على لوحة الترخيص التي تم إنشاؤها تلقائيًا عن طريق تحديد الخيار **إنشاء لوحة ترخيص** في الصفحة **تكوين بطاقة الوظيفة للأجهزة**.</span><span class="sxs-lookup"><span data-stu-id="cc1f7-113">The option to have the license plate generated automatically is configured by selecting the option **Generate license plate** on the **Configure job card for devices** page.</span></span>
