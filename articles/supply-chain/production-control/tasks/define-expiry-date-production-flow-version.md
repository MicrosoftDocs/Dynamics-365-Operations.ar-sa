---
title: تحديد تاريخ انتهاء صلاحية لإصدار تدفق الإنتاج
description: إنهاء الصلاحية ومعالجة إصدار تدفق الإنتاج في تاريخ معين، أو للتخطيط لاستبدال إصدار نشط بإصدار جديد، يجب عليك تعيين تاريخ انتهاء صلاحية على الإصدار.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d942f54b2739f2ca3dcc3e8b8a497166a8edb42
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212079"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="f7974-103">تحديد تاريخ انتهاء صلاحية لإصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="f7974-103">Define an expiry date for a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7974-104">إنهاء الصلاحية ومعالجة إصدار تدفق الإنتاج في تاريخ معين، أو للتخطيط لاستبدال إصدار نشط بإصدار جديد، يجب عليك تعيين تاريخ انتهاء صلاحية على الإصدار.</span><span class="sxs-lookup"><span data-stu-id="f7974-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="f7974-105">ليس من الضروري إلغاء تنشيط الإصدار.</span><span class="sxs-lookup"><span data-stu-id="f7974-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="f7974-106">تعيين تاريخ انتهاء صلاحية لإنهاء إصدار تدفق الإنتاج</span><span class="sxs-lookup"><span data-stu-id="f7974-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="f7974-107">انتقل إلى عنصر التحكم بالإنتاج > الإعداد > تدفق الإنتاج محدود الفاقد > تدفقات الإنتاج.</span><span class="sxs-lookup"><span data-stu-id="f7974-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="f7974-108">في القائمة، قم بالبحث عن السجل المطلوب وحدده.</span><span class="sxs-lookup"><span data-stu-id="f7974-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f7974-109">حدد أي تدفق إنتاج ذي إصدار معرف مسبقًا.</span><span class="sxs-lookup"><span data-stu-id="f7974-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="f7974-110">في القائمة، انقر فوق الارتباط في الصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f7974-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f7974-111">انقر فوق "تحرير".</span><span class="sxs-lookup"><span data-stu-id="f7974-111">Click Edit.</span></span>
5. <span data-ttu-id="f7974-112">في القائمة، قم بوضع علامة للصف المحدد.</span><span class="sxs-lookup"><span data-stu-id="f7974-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f7974-113">في الحقل "تاريخ انتهاء الصلاحية"، أدخل تاريخاً ووقتًا.</span><span class="sxs-lookup"><span data-stu-id="f7974-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="f7974-114">فيما يتعلق بتاريخ انتهاء الصلاحية، لن يبدأ تشغيل إصدار جديد أو يصبح غير نشط.</span><span class="sxs-lookup"><span data-stu-id="f7974-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="f7974-115">كما أن إنشاء مهام لتدفق الإنتاج هذا أو بدء تشغيله لن يعود ممكنًا.</span><span class="sxs-lookup"><span data-stu-id="f7974-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="f7974-116">ومع ذلك، يبقى باستطاعتك إتمام المهام التي بدأتها بعد تاريخ انتهاء الصلاحية.</span><span class="sxs-lookup"><span data-stu-id="f7974-116">You can still complete started jobs after the expiration date.</span></span>  

