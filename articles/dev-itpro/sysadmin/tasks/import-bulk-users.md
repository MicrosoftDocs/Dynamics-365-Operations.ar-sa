--- 
title: "استيراد المستخدمين بشكل مجمع"
description: "يمكن استخدام هذا الإجراء من قبل مسؤولي النظام لاستيراد عدد كبير من المستخدمين من خدمة Azure Active Directory."
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.contentlocale: ar-sa
ms.lasthandoff: 05/08/2018

---
# <a name="import-users-in-bulk"></a><span data-ttu-id="73d99-103">استيراد المستخدمين بشكل مجمع</span><span class="sxs-lookup"><span data-stu-id="73d99-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73d99-104">يمكن استخدام هذا الإجراء من قبل مسؤولي النظام لاستيراد عدد كبير من المستخدمين من خدمة Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="73d99-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="73d99-105">يمكن تشغيله كوظيفة دفعية‬</span><span class="sxs-lookup"><span data-stu-id="73d99-105">Run as a batch job</span></span>
1. <span data-ttu-id="73d99-106">انتقل إلى إدارة النظام > المستخدمين > المستخدمين.</span><span class="sxs-lookup"><span data-stu-id="73d99-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="73d99-107">انقر فوق "استيراد دُفعة‬".</span><span class="sxs-lookup"><span data-stu-id="73d99-107">Click Batch import.</span></span>
3. <span data-ttu-id="73d99-108">وسّع المقطع "تشغيل في الخلفية‬‬".</span><span class="sxs-lookup"><span data-stu-id="73d99-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="73d99-109">حدد "نعم" في حقل "معالجة الدُفعات‬".</span><span class="sxs-lookup"><span data-stu-id="73d99-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="73d99-110">في حقل "وصف المهمة"، اكتب قيمة.</span><span class="sxs-lookup"><span data-stu-id="73d99-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="73d99-111">في الحقل "مجموعة الدُفعات‬"، أدخل قيمة أو حددها.</span><span class="sxs-lookup"><span data-stu-id="73d99-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="73d99-112">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="73d99-112">This is an optional step.</span></span>  
7. <span data-ttu-id="73d99-113">حدد "نعم" في الحقل "خاص‬".</span><span class="sxs-lookup"><span data-stu-id="73d99-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="73d99-114">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="73d99-114">This is an optional step.</span></span>  
8. <span data-ttu-id="73d99-115">حدد "نعم" في حقل "وظيفة هامة‬‬".</span><span class="sxs-lookup"><span data-stu-id="73d99-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="73d99-116">هذه خطوة اختيارية.</span><span class="sxs-lookup"><span data-stu-id="73d99-116">This is an optional step.</span></span>  
9. <span data-ttu-id="73d99-117">في الحقل "فئة المراقبة‬"، حدد خيارًا.</span><span class="sxs-lookup"><span data-stu-id="73d99-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="73d99-118">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="73d99-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="73d99-119">التشغيل في بيئة وضع الحماية</span><span class="sxs-lookup"><span data-stu-id="73d99-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="73d99-120">انقر فوق "استيراد دُفعة‬".</span><span class="sxs-lookup"><span data-stu-id="73d99-120">Click Batch import.</span></span>
2. <span data-ttu-id="73d99-121">انقر فوق "موافق".</span><span class="sxs-lookup"><span data-stu-id="73d99-121">Click OK.</span></span>


