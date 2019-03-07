---
title: تحديد تاريخ انتهاء صلاحية لإصدار تدفق الإنتاج
description: إنهاء الصلاحية ومعالجة إصدار تدفق الإنتاج في تاريخ معين، أو للتخطيط لاستبدال إصدار نشط بإصدار جديد، يجب عليك تعيين تاريخ انتهاء صلاحية على الإصدار.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa0bde90273f9392a36732ed79afdad2eea8bf86
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 01/29/2019
ms.locfileid: "323515"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="c99e6-103">تحديد تاريخ انتهاء صلاحية لإصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="c99e6-103">Define an expiry date for a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c99e6-104">إنهاء الصلاحية ومعالجة إصدار تدفق الإنتاج في تاريخ معين، أو للتخطيط لاستبدال إصدار نشط بإصدار جديد، يجب عليك تعيين تاريخ انتهاء صلاحية على الإصدار.</span><span class="sxs-lookup"><span data-stu-id="c99e6-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="c99e6-105">ليس من الضروري إلغاء تنشيط الإصدار.</span><span class="sxs-lookup"><span data-stu-id="c99e6-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="c99e6-106">تعيين تاريخ انتهاء صلاحية لإنهاء إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="c99e6-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="c99e6-107">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="c99e6-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="c99e6-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="c99e6-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c99e6-109">حدد أي تدفق إنتاج ذي إصدار معرف مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="c99e6-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="c99e6-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c99e6-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c99e6-111">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="c99e6-111">Click Edit.</span></span>
5. <span data-ttu-id="c99e6-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="c99e6-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c99e6-113">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="c99e6-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="c99e6-114">فيما يتعلق بتاريخ انتهاء الصلاحية، لن يبدأ تشغيل إصدار جديد أو يصبح غير نشط.</span><span class="sxs-lookup"><span data-stu-id="c99e6-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="c99e6-115">كما أن إنشاء مهام لتدفق الإنتاج هذا أو بدء تشغيله لن يعود ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="c99e6-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="c99e6-116">ومع ذلك، يبقى باستطاعتك إتمام المهام التي بدأتها بعد تاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="c99e6-116">You can still complete started jobs after the expiration date.</span></span>  

