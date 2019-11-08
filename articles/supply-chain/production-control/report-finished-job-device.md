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
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572119"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="9488b-103">.الإبلاغ كمنتهٍ إلى موقع غير خاضع للتحكم من جهاز بطاقة الوظيفة</span><span class="sxs-lookup"><span data-stu-id="9488b-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="9488b-104">تُكمل العملية التي يُطلق عليها الإبلاغ كُمنتهي المنتجات المنتهية في أمر إنتاج إلى المخزون.</span><span class="sxs-lookup"><span data-stu-id="9488b-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="9488b-105">إذا تم تمكين المنتج المنتهي لعمليات المستودع المتقدمة، يتم الإبلاغ عن المنتج كُمنتهي إلى موقع يٌسمى موقع مُخرجات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="9488b-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="9488b-106">للحصول على معلومات حول إعداد موقع مُخرجات الإنتاج، راجع [موقع مُخرجات الإنتاج](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="9488b-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="9488b-107">يجب عليك تحديد رقم لوحة الترخيص الحالية لإنهاء هذه المهمة.</span><span class="sxs-lookup"><span data-stu-id="9488b-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="9488b-108">إذا تم إعداد موقع مُخرجات الإنتاج ليتم تعقبه بواسطة لوحة الترخيص، فمن ثم يجب تضمين رقم لوحة الترخيص عندما يتم الإبلاغ عن موقع مُخرجات الإنتاج كمُنتهِ.</span><span class="sxs-lookup"><span data-stu-id="9488b-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="9488b-109">يكون حقل **لوحة الترخيص** مرئيًا في مطالبة **تقرير التقدم** على صفحة **جهاز بطاقة الوظيفة**.</span><span class="sxs-lookup"><span data-stu-id="9488b-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="9488b-110">ولا يظهر هذا الحقل إلا في مطالبة **تقرير التقدم** عند الإبلاغ عن آخر عملية لأمر الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="9488b-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="9488b-111">ويظهر هذا الحقل فقط إذا تم تمكين الصنف الخاص بأمر الإنتاج لعمليات إدارة المستودع.</span><span class="sxs-lookup"><span data-stu-id="9488b-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
